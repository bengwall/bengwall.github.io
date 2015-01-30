---
published: true
layout: post
title: Summary of What's new with Restangular 2.0
---

As developers we are rarely ever satisfied with the design of version 1.0 of projects.  Version 1.0 is almost a requirements gathering and design testing excursive.  We learn a lot and think of better and simpler design patterns.  The same holds true for Restangular 1.0 even though it is an excellent first iteration and provides an excellent abstraction from Angular's Http and Resource services.

####Models, models, models...!
- The central change is that Restangular is becoming much more model based.
- This will make all aspects of the framework much simpler to use and work with.
- The models are now based on JavaScript Prototype objects.  
- This will also remove the need for developers to roll out their own prototype designs which can be very complicated.  

Once configured, it will even handle nested resources coming from the REST service and automatically transform them into prototypes and collections of prototypes.  (Nested resources are such as a collection of Comment objects being included in a Post object coming back from the REST service.)

- This allows for some pretty cool encapsulation.  The model objects will now how to post/put themselves back to the REST api.
- Intercepters can now be at the model layer instead of having just one intercepter with “if” checks based on the api resource.

####Additional Resources:
- Git Hub summary (Sept 2014): https://github.com/mgonto/restangular/issues/890
- Ng-europe's [Restangular presentation](https://www.youtube.com/watch?v=fWar75R1NGo&index=5&list=PLhc_bKwZngxW_ZlY0NkaGkvKpiA_pzcZ-)

