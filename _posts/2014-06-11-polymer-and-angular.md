---
published: true
layout: post
---


For those who have not heard of Polymer yet, get ready for the future.  [Polymer](https://www.polymer-project.org/) is one of Google's many projects.  From my limited understanding, Polymer seeks bring the future of Web Components to the present.  It seeks to do this by creating a base upon which each modern browers can use web components. 

Web Components are a HTML5 standard, but until all browsers support it and have implemented the underlying technologies, it will not be a viable solution.  Polymer is a layered client-side stack which uses polyfills for these underlying technologies missing in the various browsers.  They call this the Platform Layer.  This layer will ensure a stable and reliable foundation in which to build these components.  Polymer also contains a Core Layer provides a framework for orchestration between the underlying technologies.   This Core Layer is not in the standard, but provides a higher layer of abstraction and helper libraries.  

![Polymer](http://www.infoq.com/resource/news/2013/05/webcomponents/en/resources/polymer-architecture.png)

###Web Components vs Angular Directives
First of all Polymer will not replace Angular.  As a matter of fact, it Angular 2.0 may utilize the Web Components technology of Polymer.  The teams are talking regularly it seems.  Angular is a framework which provides many services and features not offered by Polymer.  I have developed in Angular for a few years now and things I wish were simple are Angular are validations and directives.  Web Components should simplify the ordeal.

Polymer components are just DOM, so you can use them with Angular now.

###My thoughts on Polymer
It looks great.  The demos look impressive.  The documentation and guides are nice.  The element creation techniques look relatively simple and well thought out.  Polymer does a nice job hiding the complexity involved in declaring bindings, and it seems fairly flexible.  Although I believe that it is still in beta, I heard that some sites are using it in production.

Polymer is not at the top of my list of technologies to learn, but it is a nice glimpse into where UI development is heading.  It is not too practical at this point.  Once Angular 2.0 is more established, I will give it a go. 

###References
- [https://www.polymer-project.org](https://www.polymer-project.org)
- [Polymer v Angular - Alex Mingoia](http://www.binpress.com/blog/2014/06/26/polymer-vs-angular)
- [Web Components in Action - Alex Komoroske, Matthew McNulty (Google I/O 2013)](http://www.youtube.com/watch?v=0g0oOOT86NY#t=220)
- [Unlock the next era of UI development with Polymer - Rob Dodson (Google I/O 2014)](http://www.youtube.com/watch?v=HKrYfrAzqFA)