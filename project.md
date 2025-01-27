---
layout: page
title: Projects
---
This page describes my project experiences before graduate.

<h1 class="post-title">
  <a href="{{ site.baseurl}}/kf/">
    Learning Based Kalman Filter
  </a>
</h1>

<hr width="100%" color="black" size="5">

　<span style="color:blue">　blue = Groundtruth</span>
<span style="color:orange">orange = Estimated position of robot</span> <br>
<img src = "https://user-images.githubusercontent.com/57785895/99908174-6dd9e080-2d24-11eb-841c-63a924860943.gif" alt=kf_animation_1 style="float:left">

　To automatically determine parameters of the Kalman filter with machine learning and convex optimization. In other words, learning the parameters of the Kalman filter.<br>
　That image(.gif) is an animation of the result. The animation show the estimated position of robot getting more similar to the groundtruth by learning parameters.

<a href="{{ site.baseurl}}/kf/"> More </a>
<p class=clearedText> </p>

<br>
<h1 class="post-title">
  <a href="{{ site.baseurl}}/autocar/">
    Intelligent Model Car competition
  </a>
</h1>
<hr width="100%" color="black" size="5">

<video class = "mvideo" style="float:left; margin-right:2px" controls src="https://drive.google.com/uc?export=download&id=16QfK1wCPetp34UF6whwQUNx0rrHLa6rU" frameborder="0" allowfullscreen="">
</video>

<video class = "mvideo" style="float:left" controls src="https://drive.google.com/uc?export=download&id=1Ds5f1gfT0gVwPCYufanFA7me8Jjs1t9R" frameborder="0" allowfullscreen="">
</video>

<p class=clearedText> </p>

The goal of the competition is to design autonomous model car that traces correct lines and avoid obstacles. 

First, I developed almost H/W ( power supply system, sensing system ) with Tri-core MCU.<br>
Sececond, I designed object detection with image processing and steering controller with the Stanely method.
Especially for image processing, I had to make my own filter for line scan image. It was not able to detect with well-known filters because of extreme noise and the very low disparity between lines and not lines. So, I mainley made a filtering model that catches features of the line as the following formula. A following image is the result of filtering.
<a href="{{ site.baseurl}}/autocar/"> 　More </a>

<span style="color:red">Red is raw line scan image.</span> <span style="color:blue">Blue is filtered image.</span>
<img src = "https://user-images.githubusercontent.com/57785895/122672323-03c7e200-d206-11eb-88c2-b643210ec317.png" width = "80%" height ="90%">

<br>
# Aircraft Detection
<hr width="100%" color="black" size="5">
<!--iframe class = "mvideo" style="float:left; margin-right:2.0em display:block" controls src="https://drive.google.com/file/d/1X9ARlR9JzDUpHBmBsXHeoW046sgo9TZR/preview" frameborder="0" allowfullscreen="">
</iframe-->

<video class="mvideo" style="margin-right:2.0em" controls src="https://drive.google.com/uc?export=download&id=1X9ARlR9JzDUpHBmBsXHeoW046sgo9TZR" frameborder="0" allowfullscreen="">
</video>

It is aricraft detection without machine learning.<br>
Classical image processing is applied.<br>
Canny Edge and Feature Extraction is mainely used.

<p class=clearedText> </p>

<br>
<h1 class="post-title">
  <a href="{{ site.baseurl}}/guiderobot/">
    Indoor Guide Robot for Visually Impaired Person
  </a>
</h1>
<hr width="100%" color="black" size="5">

<video class="mvideoNarrow" style="margin-right:2.0em" controls src="https://drive.google.com/uc?export=download&id=1n0-PRGFu63LX4q9goHhdiZQJonWWWCRU" frameborder="0" allowfullscreen="">
</video>

Using ROS, I implemented an indoor guide robot application into a mobile robot with cartographer SLAM. <br>
It was designed for blind people to visit a huge building that has several floors.<br>
A very short paper was submitted at The 15th Korea Robotics Society Annual Conference (KRoC 2020)


<a href="{{ site.baseurl}}/guiderobot/"> More </a>
<!--img src = "https://user-images.githubusercontent.com/57785895/122672101-c747b680-d204-11eb-98a2-559da425baa7.png" width = "35%" height= "35%"-->

<p class=clearedText> </p>

<br>
<h1 class="post-title">
  <a href="{{ site.baseurl}}/sram/">
    In-Memory Computing SRAM with Xnor CNN
  </a>
</h1>
<hr width="100%" color="black" size="5">

<img src="https://user-images.githubusercontent.com/57785895/122672672-ca907180-d207-11eb-9151-dd5e3029a643.png" alt="image" width="500" style="float:left">
<img src="https://user-images.githubusercontent.com/57785895/122672560-1989d700-d207-11eb-9c7a-a633b143a9e1.png" alt="image" width="500" style="float:left">

<p class=clearedText> </p>
I developed a system accelerating CNN for a dissertation. It was implemented with computable SRAM and optimized xnor-network CNN.

The first image is a cell of the computable-SRAM. It can do xnor computation to operate CNN.

The second image is XNOR-CNN netwokr for Computable-SRAM.
My main part is to implement the network.
To implement internal calculation in SRAM, this xnor-network CNN is comprised of xnor computation. All values of weights and input images are quantized to +1 or -1. And the valuse are mapped to memory with differnt method from common. 

<a href="{{ site.baseurl}}/sram/"> More </a>

<p class=clearedText> </p>

<br>
# Quadruped Spider Robot
<hr width="100%" color="black" size="5">
I made the robot to display at my robot club's exhibition

<img src = "https://user-images.githubusercontent.com/57785895/122671822-6ec3e980-d203-11eb-96cf-5beb25e27908.png" width="50%" height="50%">

<br>
# Blitzcrank Robot
<hr width="100%" color="black" size="5">
I made the robot to display at Kyunghee SW Festival.

<img src = "https://user-images.githubusercontent.com/57785895/122671813-62d82780-d203-11eb-8aae-cf9e5e14d6d4.png" width="35%" height="35%">

