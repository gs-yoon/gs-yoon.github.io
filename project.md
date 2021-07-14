---
layout: page
title: Projects
---
<!--youtubeId: 16QfK1wCPetp34UF6whwQUNx0rrHLa6rU/view?usp=sharing-->
This page describes my projects before graduate.
All of the projects are not performed in school lectures.

# Learning Based Kalman Filter
<hr width="100%" color="black" size="5">

<img src = "https://user-images.githubusercontent.com/57785895/99908174-6dd9e080-2d24-11eb-841c-63a924860943.gif" alt=kf_animation_1 style="float:left">

<span style="color:blue">blue = Groundtruth</span> <br>
<span style="color:orange">orange = Estimated position of robot</span>

To automatically determine parameters of the Kalman filter Using machine learning and convex optimization. In other words, learning the parameters of the Kalman filter

More
<p class=clearedText> </p>


# Intelligent Model Car competition
<hr width="100%" color="black" size="5">

# Embed Google Drive 

<!---
Include this next line in your .md file for Google Drive videos, make sure to put your video ID up there!

Example:     driveId: 0B7L_dMcaZknxVTRndmdSQ0F5OFE/preview

{% include googleDrivePlayer.html id=16QfK1wCPetp34UF6whwQUNx0rrHLa6rU/view?usp=sharing %}
{% include googleDrivePlayer.html id=1Ds5f1gfT0gVwPCYufanFA7me8Jjs1t9R/view?usp=sharing %}
-->

<div class="embed-container">
  <iframe width="640" height="480" src="https://drive.google.com/file/d/16QfK1wCPetp34UF6whwQUNx0rrHLa6rU/view?usp=sharing" frameborder="0" allowfullscreen="">
  </iframe>
</div>

<div class="embed-container">
  <iframe width="640" height="480" src="https://drive.google.com/file/d/1Ds5f1gfT0gVwPCYufanFA7me8Jjs1t9R/view?usp=sharing" frameborder="0" allowfullscreen="">
  </iframe>
</div>

The goal of the competition is to design autonomous model car that traces correct lines and avoid obstacles. 

I designed object detection with image processing and steering controller with the Stanely method. There are two key points of my algorithms. 
First, I had to make my own filter for line scan image. It was not able to detect with well-known filters because of extreme noise and the very low disparity between lines and not lines. So, I made a filtering model that catches features of the line as the following formula.

**α** means start pixel to apply filter.<br>
**β** means end pixel to apply filter.

<p align="center">
<img alt="sigma_s" src="https://user-images.githubusercontent.com/57785895/122916840-4b7e7300-d398-11eb-9cbd-eecc88ec80dd.png">
</p>

<span style="color:red">Red is raw line scan image.</span> <span style="color:blue">Blue is filtered image.</span>
<img src = "https://user-images.githubusercontent.com/57785895/122672323-03c7e200-d206-11eb-88c2-b643210ec317.png" width = "90%" height ="90%">


The second point is to adapt the Stanely method for steering. The formula that I used is expressed in below.

**δ** is angle to steer.<br>
**Ψ** is angle between direction of movement and tangent line of lane.<br>
**L** is distance between car and lane.

![stanely](https://user-images.githubusercontent.com/57785895/122923723-f0507e80-d39f-11eb-8ea7-c530278923f9.png)

# Indoor Guide Robot for Visually Impaired Person
<hr width="100%" color="black" size="5">

Using ROS, I implemented an indoor guide robot application into a mobile robot. 
  It was designed for blind people to visit a huge building that has several floors.
  A very short paper was submitted at The 15th Korea Robotics Society Annual Conference (KRoC 2020)
<img src = "https://user-images.githubusercontent.com/57785895/122672101-c747b680-d204-11eb-98a2-559da425baa7.png" width = "35%" height= "35%">


# In-Memory Computing SRAM with Xnor CNN
<hr width="100%" color="black" size="5">
It was written for Dissertation

I developed a system accelerating CNN. It was organized with computable SRAM and optimized xnor-network CNN.

### Computable SRAM

The below image is of computable-SRAM. And I will not describe hardware anymore. Other sections are explaining SoftWare. 

![image](https://user-images.githubusercontent.com/57785895/122672672-ca907180-d207-11eb-9151-dd5e3029a643.png)

**The below section is about software.**

### XNOR NET

I took the  **xnor network** CNN to compute in memory. 
Xnor-network CNN is comprised of xnor computation. Including weights and input images, all of values  are +1 or -1. It is very efficient for memory computation.
The key point is how to quantize values. A formula can be obtained after many complex calculations. But I will not describe all steps, I'm just showing the result.
The result formular is following.

![image](https://user-images.githubusercontent.com/57785895/122761471-3db4e900-d2d7-11eb-9dd6-253a834bfcf4.png)

![image](https://user-images.githubusercontent.com/57785895/122761623-676e1000-d2d7-11eb-9441-a9bd867a68ed.png)

![image](https://user-images.githubusercontent.com/57785895/122672518-d2034b00-d206-11eb-854b-2a701d50788e.png)

### Sequence and Acitvation

**Sequence** : Convolution → BatchNormalize → Binarize Input & Weight of other layers

**Activation** : tanh (can't use RELU for XNOR NET)

![image](https://user-images.githubusercontent.com/57785895/122672560-1989d700-d207-11eb-9c7a-a633b143a9e1.png)

### Mapping to memory
Following image explain how to mapping iamge and weights to memory. Data is mapped in each column. This is because sram operate xnor computation and average values for each column.
![image](https://user-images.githubusercontent.com/57785895/122672631-93ba5b80-d207-11eb-99f4-86e4df5a0fc4.png)


### Result

Best accuracy with optimal computable SRAM is **97.7%** about Mnist handwrite 
![image](https://user-images.githubusercontent.com/57785895/122672596-4938df00-d207-11eb-9aa8-111f5744af34.png)

Best accuracy with optimal computable SRAM is **86.5%** about Mnist fashion
![image](https://user-images.githubusercontent.com/57785895/122672608-62da2680-d207-11eb-8cba-6eda388ff9e0.png)





# Quadruped Spider Robot
I made the robot to display in my robot club's exhibition

<img src = "https://user-images.githubusercontent.com/57785895/122671822-6ec3e980-d203-11eb-96cf-5beb25e27908.png" width="50%" height="50%">

# Blitzcrank Robot
I made the robot for Kyunghee SW Festival.

<img src = "https://user-images.githubusercontent.com/57785895/122671813-62d82780-d203-11eb-8aae-cf9e5e14d6d4.png" width="35%" height="35%">

