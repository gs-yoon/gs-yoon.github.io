---
layout: page
title: Projects
---
<!--youtubeId: 16QfK1wCPetp34UF6whwQUNx0rrHLa6rU/view?usp=sharing-->
This page describes my projects before graduate.
All of the projects are not performed in school lectures.

<h1 class="post-title">
  <a href="{{ site.baseurl}}/kf/">
    Learning Based Kalman Filter
  </a>
</h1>

<hr width="100%" color="black" size="5">

<span style="color:blue">blue = Groundtruth</span>
<span style="color:orange">orange = Estimated position of robot</span> <br>
<img src = "https://user-images.githubusercontent.com/57785895/99908174-6dd9e080-2d24-11eb-841c-63a924860943.gif" alt=kf_animation_1 style="float:left">

To automatically determine parameters of the Kalman filter Using machine learning and convex optimization. In other words, learning the parameters of the Kalman filter

<a href="{{ site.baseurl}}/kf/"> More </a>
<p class=clearedText> </p>

# Intelligent Model Car competition
<hr width="100%" color="black" size="5">

<iframe width="480" height="360" style="float:left; margin-right:2px" src="https://drive.google.com/file/d/16QfK1wCPetp34UF6whwQUNx0rrHLa6rU/preview" frameborder="0" allowfullscreen="">
</iframe>

<iframe width="480" height="360" style="float:left" src="https://drive.google.com/file/d/1Ds5f1gfT0gVwPCYufanFA7me8Jjs1t9R/preview" frameborder="0" allowfullscreen="">
</iframe>

<p class=clearedText> </p>

The goal of the competition is to design autonomous model car that traces correct lines and avoid obstacles. 

I designed object detection with image processing and steering controller with the Stanely method. There are two key points of my algorithms. 
First, I had to make my own filter for line scan image. It was not able to detect with well-known filters because of extreme noise and the very low disparity between lines and not lines. So, I mainley made a filtering model that catches features of the line as the following formula. A following image is the result of filtering.

<span style="color:red">Red is raw line scan image.</span> <span style="color:blue">Blue is filtered image.</span>
<img src = "https://user-images.githubusercontent.com/57785895/122672323-03c7e200-d206-11eb-88c2-b643210ec317.png" width = "80%" height ="90%">

# Aircraft Detection
<hr width="100%" color="black" size="5">
<iframe style="float:left; margin-right:2.0em" src="https://drive.google.com/file/d/1X9ARlR9JzDUpHBmBsXHeoW046sgo9TZR/preview" frameborder="0" allowfullscreen="">
</iframe>

　It is aricraft detection without machine learning.<br>
Classical image processing is applied.<br>
Canny Edge and Feature Extraction is mainely used.

<p class=clearedText> </p>

# Indoor Guide Robot for Visually Impaired Person
<hr width="100%" color="black" size="5">

<iframe width="480" height="360" style="float:left; margin-right:2.0em" src="https://drive.google.com/file/d/1n0-PRGFu63LX4q9goHhdiZQJonWWWCRU/preview" frameborder="0" allowfullscreen="">
</iframe>

　Using ROS, I implemented an indoor guide robot application into a mobile robot with cartographer SLAM. <br>
It was designed for blind people to visit a huge building that has several floors.<br>
A very short paper was submitted at The 15th Korea Robotics Society Annual Conference (KRoC 2020)
  
<!--img src = "https://user-images.githubusercontent.com/57785895/122672101-c747b680-d204-11eb-98a2-559da425baa7.png" width = "35%" height= "35%"-->

<p class=clearedText> </p>

# In-Memory Computing SRAM with Xnor CNN
<hr width="100%" color="black" size="5">

<img src="https://user-images.githubusercontent.com/57785895/122672672-ca907180-d207-11eb-9151-dd5e3029a643.png" alt="image" width="500" style="float:left">
<img src="https://user-images.githubusercontent.com/57785895/122672560-1989d700-d207-11eb-9c7a-a633b143a9e1.png" alt="image" width="500" style="float:left")

It was written for Dissertation <br>
I developed a system accelerating CNN. It was implemented with computable SRAM and optimized xnor-network CNN.<br>
The first image is a cell of the computable-SRAM. It can do xnor computation to operate CNN.<br>
The second image is XNOR-CNN netwokr for Computable-SRAM.
My main part is to implement the network.
To implement internal calculation in SRAM, this xnor-network CNN is comprised of xnor computation. All values of weights and input images are quantized to +1 or -1. And the valuse are mapped to memory with differnt method from common. 

<p class=clearedText> </p>
# Quadruped Spider Robot
I made the robot to display in my robot club's exhibition

<img src = "https://user-images.githubusercontent.com/57785895/122671822-6ec3e980-d203-11eb-96cf-5beb25e27908.png" width="50%" height="50%">

# Blitzcrank Robot
I made the robot for Kyunghee SW Festival.

<img src = "https://user-images.githubusercontent.com/57785895/122671813-62d82780-d203-11eb-8aae-cf9e5e14d6d4.png" width="35%" height="35%">

