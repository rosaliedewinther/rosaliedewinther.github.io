---
title: "Voxels"
date: 2022-02-01
draft: false
featured_image: '/images/voxels_hills.png'
---

As quite some people do, I got inspired by [John Lin's voxel engine](https://www.youtube.com/watch?v=1R5WFZk86kE) and thus, got started researching how voxels work. At first, I started with a meshing based approach similar to minecraft and got some basic lighting going. One of the first real issues I encountered was with transparency, as I did not have much experience with graphics I did not realize it would be such a hassle to render transparent water for example.


When I started working on the renderer I used [glium](https://github.com/glium/glium), but quite quickly I wanted to try [wgpu](https://wgpu.rs/) and loved it ever since. It is not only quite fast, but also very user-friendly and takes very few lines of code to get working. To get started, I used [a very popular tutorial](https://sotrh.github.io/learn-wgpu/) by Benjamin R. Hansen. The following screenshots showcase the first version of my voxel engine.

![whitted](/images/voxels_hills.png)
![whitted](/images/voxels_mountains.png)

Now, after this meshing approach, I found out that ray tracing implementations had a lot more potential due to the way acceleration structures can be made very efficient for traversal. So I worked on a [DDA](https://www.shadertoy.com/view/4dX3zl) implementation for a bit. This was not faster than the meshing approach, but with additional optimizations (such as [brickmaps](https://github.com/stijnherfst/BrickMap) or [octrees](https://research.nvidia.com/publication/efficient-sparse-voxel-octrees)) could allow for much larger worlds compared to meshing. Screenshots below, the first one just showcases the traversal working and the second on the complexity of each ray, unfortunately this is only dependent on distance when doing standard DDA.

![whitted](/images/voxels_dda.png)
![whitted](/images/voxels_complexity.png)

Voxels are definitely very interesting, and it's very likely that more will be posted about them.