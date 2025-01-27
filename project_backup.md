---
layout: none
title: Projects
---
This page describes my projects before graduate.
All of the projects are not performed in school lectures.

# Learning Based Kalman Filter
<hr width="100%" color="black" size="5">

To automatically determine parameters of the Kalman filter Using machine learning and convex optimization. In other words, learning the parameters of the Kalman filter

### Dynamic System Modeling
A discrete-time linear dynamical system consists of a sequence of state vectors <strong>x<sub>t</sub> ∈ R<sup>2</sup></strong>  , indexed by time  <strong>t∈{0,…,N−1}</strong>  and dynamics equations

<p align="center">
<img src ="https://user-images.githubusercontent.com/57785895/122776180-d5213880-d2e5-11eb-99c5-2aba3c7032d1.png" alt = "modeling">
</p>

where <strong>w<sub>t</sub> ∈ R<sup>m</sup></strong>  is an input to the dynamical system (say, a drive force on the vehicle),  <strong>y<sub>t</sub> ∈R<sup>r</sup></strong>  is a state measurement,  <strong>v<sub>t</sub> ∈R<sup>r</sup></strong>  is noise,  **A**  is the drift matrix,  **B**  is the input matrix, and  **C**  is the observation matrix.
Given  **A ,  B ,  C ,** and  <strong> y<sub>t</sub>  for  t=0,…,N−1 </strong>, the goal is to estimate  <strong>x<sub>t</sub>  for  t=0,…,N−1</strong> .

We'll apply standard and Kalman filtering to a vehicle tracking problem with state  <strong>x<sub>t</sub>∈R<sup>4</sup></strong> , where the first two states are the position of the vehicle in two dimensions, and the last two are the vehicle velocity. The vehicle has unknown drive force  <strong>w<sub>t</sub></strong> , and we observe noisy measurements of the vehicle's position,  <strong>y<sub>t</sub>∈R<sup>2</sup></strong> .

Then the following matrices the above dynamics.

<p align="center">
<img src="https://user-images.githubusercontent.com/57785895/122776239-e2d6be00-d2e5-11eb-965c-82a498fdd6cc.png" alt = "Matrices">
</p>


### Solving Equations

Kalman filtering problem of a dynamic system can be expressed as convex optimization form 
A Kalman filter estimates   <strong>x<sub>t</sub></strong>  by solving the optimization problems with some tuning parameters **τ** or **Q**

**Problem 1**
<p align="center">
<img src = "https://user-images.githubusercontent.com/57785895/122758793-2cb6a880-d2d4-11eb-918c-3833247ce5f9.png" alt ="cvxoptform1">
</p>

**Problem 2**
<p align="center">
<img src = "https://user-images.githubusercontent.com/57785895/122758803-2f190280-d2d4-11eb-90b7-91cd48cc0545.png" alt="cvxoptform2">
</p>

The proper value of **τ** and **Q** can be obtained with convex optimization  and machine learning. I used cvxpy and cvxpylayers that are python libraries to solve this problem. So, the result is shown as follows.

### Result

**result of problem 1 : Learning tau**
 
![image](https://user-images.githubusercontent.com/57785895/100963280-63f87e80-3569-11eb-856f-c0785c1e3500.png)

![tau](https://user-images.githubusercontent.com/57785895/122778310-da7f8280-d2e7-11eb-8630-1c2a8c428d45.png)

**result of problem 2 : Learning Q matrix**


![image](https://user-images.githubusercontent.com/57785895/100959769-58ee2000-3562-11eb-8c1f-27387b962be5.png)

![QQQ](https://user-images.githubusercontent.com/57785895/122778341-e1a69080-d2e7-11eb-997d-52ba855d7de8.png)


### **Result animation** 
<span style="color:blue">blue = Groundtruth</span> <br>
<span style="color:orange">orange = Estimated position of robot</span>

![kf_animaint_1](https://user-images.githubusercontent.com/57785895/99908174-6dd9e080-2d24-11eb-841c-63a924860943.gif)

# Intelligent Model Car competition
<hr width="100%" color="black" size="5">

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

