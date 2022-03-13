---
title: "Advanced Graphics @UU"
date: 2022-02-01
draft: false
featured_image: '/images/detailed_thin.png'
---

This course was one of the major reasons why I wanted to do my master's at Utrecht University, and it delivered. For the first time I could work on a ray tracer with the help of a very good and dedicated lecturer, namely [Jacco Bikker](https://twitter.com/j_bikker). During the course we first implemented a Whitted style raytracer (on the CPU). I was pleasantly surprised with the performance as I thought nothing could be rendered (let alone ray traced) on the CPU. In the scene below you see most of the implemented effects, reflection, refraction, directional lights, point lights, beer's law, vignetting, anti aliasing, gamma correction and chromatic aberration.

![whitted](/images/whitted_ray_tracer.png)

For the second assignment of the course I added a Bounding Volume Hierarchy to allow for complex models to be traced. These BVH's used the surface area heuristic and instancing to allow for many copies to be traced. Below are a visualization of a BVH and a scene containing a total of 1087474000 triangles (which was rendered in 11 seconds).


![bvh](/images/bvh.png)
![bvh](/images/buddhas.png)

For the third assignment I started using my ray tracer as a path tracer (instead of Whitted style) and moved to a wavefront design implemented in openCL. Unfortunately I did not have time to optimize it all too well, and there are some artifacts which should have been resolved (the bounce direction is not correctly distributed which can be seen clearly in the bottom image). Below are two images rendered using this version of the path tracer. 

![bvh](/images/sheep.png)
![bvh](/images/detailed.png)

Overall I probably invested the most amount of time into this course compared to any other, and it was a very fun ride. It also inspired me to continue looking into ray tracing.