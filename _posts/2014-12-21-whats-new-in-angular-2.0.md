---
published: true
layout: post
---

- Templates 
	- Syntaxes are changing a little, but will look familiar
	- Binding is to attributes properties instead of element attributes.  Properties give more flexibility such as being able to bind to objects instead of just strings and properties have a larger API.
- Directives become classes under the “component” name
- Controllers, services all become just another component
- $scope goes away
	- Components are now the execution context for the template
	- Components will also cover other $scope functions such as watches and events
	- Broadcast events will be more direct with the targeted children
- EM6 modules will replace Angular modules
j- qLite is going away because there is no need anymore.  DOM in the various browsers has advanced so much that there is no longer a need for the compatibility features provided by jqLite in the form of its DOM wrappers.  Angular will now deal the the DOM directly which will improve preformance.
- A new router will be introduced.

In short, Angular 2.0 will stay familiar but is changes for two reasons
- Angular 2.0 is modernizing towards emerging standards in WebComponents and JavaScipt.  
- The team is questioning every aspect of Angular and, as a result, new designs are being implemented to make the framework more consistent and simple.

####Additional Resources:
- Ng-europe's [Angular 2.0 Presentation](https://www.youtube.com/watch?v=gNmWybAyBHI&index=2&list=PLhc_bKwZngxW_ZlY0NkaGkvKpiA_pzcZ-)


