---
layout: default
title: kf
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
