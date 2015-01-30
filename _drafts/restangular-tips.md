---
published: false
layout: post
title: Restangular 1.0 Tips
---

# Restangular Tips

Instead of this:
```
Restagular.one('someVariable').get({someParameter: $stateParams.someParameter}).then(function(result){
    $scope.someVariable = result;
});
```

You can write this:
```
$scope.someVariable = Restagular.one('someVariable').get({someParameter: $stateParams.someParameter});
```


##Misc Resources

[Restangular's author on StackOverflow](http://stackoverflow.com/users/385982/mgonto)
[Restangular's author's sample code sniplets](https://gist.github.com/mgonto)
[ng-newsletter article](http://www.ng-newsletter.com/posts/restangular.html)
[Restangular in Services and Tests](http://ath3nd.wordpress.com/2013/08/05/15/)