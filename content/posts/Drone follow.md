---
title: "Drone follow @HU"
date: 2020-07-01
draft: false
featured_image: '/images/Drone_follow_qr.png'
---

For this assignment, we were meant to use PID systems in some form to control movement in the real world. So me, being stuck in my room during a corona lock down, had no hardware in my house besides a [Tello drone](https://www.ryzerobotics.com/tello). Due to this, I was basically forced to implement a PID controller for each of the 4 degrees of freedom of the drone. This allowed for quite fine-grained control of the drone, even in small spaces, such as my room. To make it more interactive I decided to have it follow some object, and as a QR code can be well detected and is perfectly square, I decided to go with this. The distance from the drone to the QR code can be calculated when you know the size of the QR code on the screen and the field of view of the camera. The rotation can be measured using the difference in length of the left and right side of the qr code. These two, along with the offsets from the camera center, are the foundation of the PID input. Below is a video demonstrating the result.

{{< youtube W_Kfyqd4PiA >}}


Initially it was quite hard to wirelessly interface with the drone, but this was resolved after using some very nice libraries. Namely, [sfml](https://www.sfml-dev.org/) for the networking, [opencv](https://opencv.org/[) for the decoding of video and image operations, and [zbar](http://zbar.sourceforge.net/) for the detection of the QR code.