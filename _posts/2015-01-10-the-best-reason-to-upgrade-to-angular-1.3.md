---
published: true
layout: post
title: Angular.Copy fix - The best reason to upgrade to Angular 1.3
---

A big reason why I’m looking forward to building apps with Angular 1.3 is because of an issue fixed with angular.copy.

Angular 1.2 had an issue where angular.copy would not preserve the prototype of objects being copied.  I had to write manually code to reinstate these prototypes back into my clones objects.  Angular 1.3 has fixed this issue.  See [here](https://github.com/angular/angular.js/commit/b59b04f98a0b59eead53f6a53391ce1bbcbe9b57)

In the following example, the code defines a person prototype and an address prototype.  It creates a person instance called `p` which contains an instance of an address `a`.  It then does a deep clone/copy of `p` to `p2` with angular.copy.  With Angular 1.2, `p` and `a` would lose their prototype and just be a generic JavaScript Object.  With Angular 1.3, these prototypes are preserved.  Here is a [plunker](http://plnkr.co/edit/SXaDOCo2kMYp5NgfIryz?p=preview) of this code.

```
function Person(attrs){
    this._init(attrs);
};
Person.prototype={
    _init:function(obj){
        if(obj) angular.extend(this, obj); 
    }
};
Object.defineProperty(Person.prototype,"fullName",{
    get:function(){
        return this.firstName + ' ' + this.lastName;
    }
});


function Address(attrs){ 
    this._init(attrs);
};
Address.prototype={
    _init:function(obj){
        if(obj) angular.extend(this, obj);
    }
}; 
Object.defineProperty(Address.prototype,"fullAddress",{
    get:function(){
        return this.addressLine1 +(this.addressLine2?' '+this.addressLine2 :' ')+','+this.city+', '+this.stateCode+' '+this.zipCode;
    }
});

p = new Person({'firstName':'Brent', 'lastName':'Engwall'});
p.a = new Address({"addressLine1":"100 Main St"});

p2 = angular.copy(p);                  // make a clone

p.a.addressLine1 = "200 New St'";      // change the address of line 1 of the original person 
                                       //  to make sure the cloned person uses a different address

console.log(p2 instanceof Person);     // --> should be 'true', was 'false' in Angular 1.2
console.log(p2.a instanceof Address);  // --> should be 'true', was 'false' in Angular 1.2

console.log(p2.fullName);              // --> prototype properties should exist, was 'undefined' in Angular 1.2
console.log(p2.a.fullAddress);         // --> prototype properties should exist, was 'undefined' in Angular 1.2
```