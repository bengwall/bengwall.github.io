---
published: true
layout: post
---

## Description
Lo-Dash.js is a JavasScript library which provides utility functions for common JavaScript tasks.  It provides support for the functional constructs (each, map, reduce, filter...) without extending any core JavaScript objects.  

Some of these functional constructs are slowing making there way into the ECMA specifications, but they are at various stages of implementation across the browsers.  Lo-Dash provides abstractions that work everywhere.  If available, Lo-Dash falls back to native implementations.

## Reasons for Lo-Dash.js
* **Less Code:**  SPA and REST driven apps typically process many objects, arrays, and collections.  Lo-Dash provides functions to handle and manipulate these objects.  Lo-Dash can do these manipulations with less code.
* **Popularity:** [Google Trends](http://www.google.com/trends/explore#q=underscorejs%2C%20lodash&cmpt=q)
* **MIT License:** [GITHUB code](https://github.com/lodash/lodash/blob/master/lodash.js)
* **Compact:** 28k
* **Active:** [GITHUB activity](https://github.com/lodash/lodash/graphs)
* **Quality:** [100% code coverage](http://lodash.com/), [GITHUB Issues](https://github.com/lodash/lodash/issues)
* **No Overlap:** It does not overlap with existing approved libraries
* The Restangular library for AngularJS is dependent on Lo-Dash (or Underscore).

## Examples
Below are some before and after examples.  Here are some [additional examples](http://lodash.com/docs).

#### Example #1
The following code...

```
scope.pageActionHandlers = {};
for(i=0;i <options.flows.length;i++){
	scope.pageActionHandlers[options.flows[i].name] = options.flows[i].handlers;
}
```

...can be written as...

```
scope.pageActionHandlers = {};
_.each(options.flows, function(flow) {
    scope.pageActionHandlers[flows.name] = flows.handlers;
});

// or better yet...
scope.pageActionHandlers = _.map(options.flows, function(flow){
    return {flow.name: flow.andlers};
});
                            .
```

#### Example #2
The following code...

```
// get first flow where flow.name = flowName
var foundFlow = undefined;
for(i=0;i<flows.length;i++){
    if(flows[i].name == flowName){
		foundFlow = flows[i];
	}
}
```

...can be written as...

```
var foundFlow = _.find(flows, function(flow) {
    return flow.name: flowName;
});

// or better yet...
var foundFlow = _.findWhere(flows, {name : flowName});
```


## Alternatives
####Underscore.js
* **Popularity:** [Google Trends](http://www.google.com/trends/explore#q=underscorejs%2C%20lodash&cmpt=q)
* **MIT License:** [GITHUB code](https://github.com/jashkenas/underscore)
* **Compact:** 14k
* **Active:** [GITHUB activity](https://github.com/jashkenas/underscore/graphs)
* **Quality:** [Unit tests](http://underscorejs.org/test/), [GITHUB Issues](https://github.com/jashkenas/underscore/issues)
* Additional References
    * [Underscore on GITHUB](https://github.com/jashkenas/underscore)
    * [Getting Cozy With Underscore.js](http://code.tutsplus.com/tutorials/getting-cozy-with-underscorejs--net-24581)
* Comparison to Lo-Dash
    * Lo-Dash has more features
    * Lo-Dash has a more consistent API behavior
    * Lo-Dash has more thorough documentation
    * Lo-Dash has better code coverage
    * Lo-Dash and better performance.
    * Lo-Dash is larger (28k for Lo-Dash vs 14k for Underscore)
    * Lo-Dash has more community support
    * Lo-Dash has more momentum 
    

## LoDash.js References
* [http://lodash.com/](http://lodash.com/)
* [Preformance tests](http://jsperf.com/lodash-underscore)
* [Lo-Dash – Origins](http://vimeo.com/44154600) video
* [Underscore vs Lo-Dash vs Lazy](http://adamnengland.wordpress.com/2013/10/10/benchmarks-underscore-js-vs-lodash-js-vs-lazy-js/)
* [Stackoverflow - Difference between Lo-Dash and Underscore](http://stackoverflow.com/questions/13789618/differences-between-lodash-and-underscore.)
* [Lo-Dash Benchmarks](http://lodash.com/benchmarks)
* [Say Hello to Lo-Dash](http://kitcambridge.be/blog/say-hello-to-lo-dash/)
