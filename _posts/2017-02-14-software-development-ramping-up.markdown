---
layout: post
title:  "Software development ramping up"
date:   2017-02-14 20:00 -0000
categories: software update
---

Software development has begun ramping up, and here's a preview of a new feature that's been implemented.
As background, our system is using a Kinect as its main sensor for gathering depth and visual data.

We have integrated the OpenCV's [ArUco marker](https://www.uco.es/investiga/grupos/ava/node/26) detection functionality with our project,
which will allow us to track not only the location of people within the Kinect's scene (a functionality available though native Kinect APIs),
but also will allow us to track and distinguish between objects to which we affix these markers.


![Development screenshot]({{ site.url }}/assets/image/opencv_kinect_development.png)
<div class="caption">A screenshot of the development environment.</div>

The above image shows a snapshot of our development process.
My skeleton is being tracked by the Kinect APIs (shown in green) while the four corners of the AruCo marker are being tracked by OpenCV APIs (shown in RGBY).

OpenCV tracking is but one critical part of our system, and you can expect more updates as we develop and refine all of our project's features.