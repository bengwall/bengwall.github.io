---
published: false
---

I'm not a big fan of clever code, because sometimes it makes code less obvious.  Sometimes they make the code more readable, especially when they are generally accepted.  Here are a few of the clever conventions available in JavaScript which will save you time and shorten your code by removing duplication.

##1. Short Circuits Evaluations
I use this all the time because it is so useful.  Take a look at the following code:

```javascript
var aaa;
if (bbb) {
	aaa = bbb;
} else {
	aaa = ccc;
}
```

This can be written much more concisely the double pipe (||) default operator.  In this case `ccc` is the Fallback option.

```javascript
var aaa = bbb || ccc;
```

Interesting enough, you can use the && (logical And) handle the truthy case.  Instead of this:

```javascript
if (bbb) {
	doFunction1();
} else {
	doFunction2();
}
```

Use this:

```javascript
var ddd = bbb && doFunction1() || doFunction2();
```

##Ternary Notiation, Example #1
This take a little getting used to, but will also become a favorite of yours.  Instead of this:

```javascript
var aaa;
if (ddd === eee) {
	aaa = bbb;
} else {
	aaa = ccc;
}
```

Use this:

```javascript
var aaa = (ddd === eee) ? bbb : ccc;
```

##Ternary Notiation, Example #2
Here is a little trick you can do within the syntax:

```javascript
var aaa;
if (ddd+eee === fff) {
	aaa = ddd+eee;
} else {
	aaa = ccc;
}
```

This can be written much more consiscly the double pipe (||) default operator.

```javascript
var aaa = ((_ref = ddd+eee) === fff) ? _ref : ccc;
```

##Array Shortcut Notation

```javascript
var messages = new Array();  // can be also written   var messages = [];
messages[0] = 'This is message 1';
messages[1] = 'MSG002':'This is message 2';
```

This is a little word.  This is better.

```javascript
var messages = [
	'This is message 1',
	'This is message 2'
];
```

Tip for adding to an array:

```javascript
messages.push('This is message 3');  	// Adds to the end of the array
messages.unshift('This is message 0');  // Adds to the beginning of the array
```

##Associative Arrays
Associative arrays are emply JavaScript objects that behave like arrays with a key value instead of a number.  Kind of like a key-value pair.  The value here can be a string, object, or anything else.

```javascript
var messages = {
	'MSG001':'This is message 1',
    'MSG002':'This is message 2'
}
console.log(messages['MSG001']);  ---> 'This is a message 1'
console.log(messages.MSG001);  ---> 'This is a message 1'
```


References:
http://www.grauw.nl/blog/entry/510


Other tips
1. === vs ==
2. Do not use global scope.  Always use `var`
3. Do not use () when passing a function as a parameter
4. You can add on to prototypes.

```String.prototype.trim = function(){return this.replace(/^\s+|\s+$/g, "");};```

5. Use logical AND/ OR for conditions

```var foo = 10;  
foo == 10 && doSomething(); // is the same thing as if (foo == 10) doSomething(); 
foo == 5 || doSomething(); // is the same thing as if (foo != 5) doSomething();```

The logical OR could also be used to set a default value for function argument.

```function doSomething(arg1){ 
	arg1 = arg1 || 10; // arg1 will have 10 as a default value if it’s not already set
}```

