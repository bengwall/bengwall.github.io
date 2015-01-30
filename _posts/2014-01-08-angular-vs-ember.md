---
published: true
layout: post
---

###My Experience:
- Angular was simple to quickly learn and start using.  I was in awe for the first few weeks while reading, watching videos, and using it.
- It became more difficult once I got into situations where I had issues and found myself needing to know how the Angular black box worked so I could figure out what I was doing wrong.  
- Directives, which are reusable components which manipulate the DOM and plug into the Angular binding, are very powerful but have a high learning curve to create correctly.

###Notes
- Angular seems to have more momentum at the time.  Part of that could be the Google “glow”.  I do not think it would have as much attention if it wasn’t a Google project.  
- Angular seems to have a broader toolset.
	- Animations are included (Ember is currently discussing how to add this)
	- Modularity and encapsulation are built in (Ember is also discussing this)
	- Dependency injection for testability.  (Ember has a testing library underway)
- Ember seems to be liked by more developers who like more precise code.  Embers code seems to be more exact which leads to more verbosity.
- There is strong support for Angular’s declarative syntax in HTML compared to Ember’s handlebar usage.  Ember’s current direction seems to work in code.  Angular works well better with HTML.  For this reason, it would be easier to translate designer’s HTML to an Angular application.
- Both are evolving and large laundry list of features to add and changes to make.
- I get the feeling that the Ember group is hurt that Angular is getting so much attention, almost defensively.  They reference Angular and off handedly poke at Angular, but the Angular team never references Ember.

###My Overall Veeling
- I like Embers coding style.  It may lead to better structure for larger and complex apps.  It may be more verbose, but I find that makes it more readable in complex examples.
- Angular is just so easy to use.
- Angular has more features, but I feel Ember has a better base.  If Ember had Angular’s features, it may be an easier choice.  Ember will probably catch up at some point, but Angular is not standing still either.
- Many people think that there is room for both.  Ember for the biggest applications and Angular for more basic uses.

###Bottom Line:
- Both Angular and Ember will speed up the development of client side applications.  Both are very good libraries and will continue to get even better.
- Choose Angular if 
	1. you need a toolkit that can speed up development of a heavy client side app or
    2. if the project is on a tight deadline and developers need to learn quickly. 
    
- Choose Ember if 
	1. you want a strict framework that provides a common structure to all your apps and
    2. if developers have time to learn the steeper learning curve.

<br>
<br>

#Comparisons:


| - | **Angular**  | **Ember** |
| :--- | :--- | :--- |
| Size | 35kb | 67kb |
| Established | 2009 | 2011 |
| Dependencies | None | Handlebars & jQuery |
| License | MIT |  MIT |
| Philosophy | "You want to do A? Here's everything you will need to do it, use it."<br><br>A toolset for building the framework most suited to your application development. | "You want to do A? Do it this way."<br><br>Makes a lot of the decisions for you. Some think it is excessively sophisticated and complex, and has unnecessary levels of abstractions. |
| Style | Declarative (more DOM) | Imperative (more code) |
| [Component Architecture](http://www.wintellect.com/blogs/nstieglitz/angular.js-vs-ember.js-star-rating-component-comparison) | Directives (fully reusable components) | Components + Views but not nearly as complete at Angular |
 | Performance | Faster rendering (4x faster with 10,000 elements because no observable overhead)<br><br>Hevery Misko (creator of Angular) comments on performance concerns: http://stackoverflow.com/questions/9682092/databinding-in-angularjs | Faster binding (much faster because of observables) |
| Mobile | Angular is focusing more on mobile and has dedicated staff to mobile | Not much out there. http://blangslet.com/post/55590279372/ember-js-mobile-animations-and-touch-gestures |

<br>


| **ARCHITECTURE** |  |
| :--- | --- |
| Separation of concerns | Tie |
| Modularization | Tie |
| Performance | Tie |
| Organization & Structure | Ember |
| Established conventions | Ember |
| <br> | <br> |
| **PRACTICALITY** |  |
| Longevity | Tie |
| Learning Curve | Angular |
| License | Tie (both MIT) |
| Size of library | Angular |
| Momentum | Tie (edge to Angular) |
| Dependencies | Angular |
| Compatible with other frameworks | Tie |
| <br> | <br> |
| **FEATURES** |  |
| Testability, DI, Mocking | Angular |
| MVC | Tie (edge to Ember) |
| Animations | Angular |
| Mobile | Tie |
| Reusable Components | Angular |
| Routing, Deep-linking, History | Tie |
| HTML5 Validation | Angular |
| Auto Binding | Tie (edge to Angular) |
| Template Support | Tie (edge to Angular) |
| Nested Template Support | Tie (edge to Angular) |
| Computed Properties | Ember |

<br>
<br>

#References

- Prefect [presentation](https://docs.google.com/presentation/d/1e0z1pT9JuEh8G5DOtib6XFDHK0GUFtrZrU3IfxJynaA/preview#slide=id.g177e4bd2b_0148) on both which sums up everything I’ve been reading (11/2013)
- Nice summary of some [differences](http://blog.nebithi.com/angularjs-vs-emberjs) (9/2012)
- Another nice and more complete [comparison](http://voidcanvas.com/why-angularjs-is-generally-better-than-emberjs-and-backbonejs/#.UtLSXZ5dXpw) (11/2013)   
- [Performance comparison](http://voidcanvas.com/emberjs-vs-angularjs-performance-testing/#.UtMib55dXpw) (12/2013) 
- Good [videos](http://emberfest.eu/munich) from EmberCast 2013
- Good [argument for Ember](http://robb.weblaws.org/2013/06/21/angularjs-vs-emberjs/)   
- Good [presentation from an Architecture point of view](http://www.slideshare.net/lrdesign/architecture-emberjs-and-angularjs)
- Another [philosophy post by Misko Hevery](http://www.quora.com/Client-side-MVC/Is-Angular-js-or-Ember-js-the-better-choice-for-Javascript-frameworks) (founder of Angular)