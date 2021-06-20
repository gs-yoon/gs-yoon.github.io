---
layout: page
title: Projects
---
This section describe my projects befor graduate. 
All of the projects are not related to school lecture.

## Intelligent Model Car competition
<hr width="100%" color="black" size="5">

Goal of the competition is to design autonomous model car that trace correct lines and avoid obstacles. 
I desinged object detection with image processing and steer controller with stanely method


$\displaystyle\sum_{i=alpha}^{\beta}{(y_i-t_i)^2}$

<img src = "https://user-images.githubusercontent.com/57785895/122672393-3ffb4280-d206-11eb-9e8d-1c44e09e85e4.png" width = "20%" height ="20%">

<img src = "https://user-images.githubusercontent.com/57785895/122672323-03c7e200-d206-11eb-88c2-b643210ec317.png" width = "90%" height ="90%">

<img src = "https://user-images.githubusercontent.com/57785895/122672160-0fff6f80-d205-11eb-86a9-d0687071178c.png" width = "75%" height ="75%">

# Indoor Guide Robot for Visually Impaired Person
<hr width="100%" color="black" size="5">

Using ROS, I implemented a indoor guide robot application into mobile robot. 
  It was designed for blind person to visit huge building that has several floors.
  A very short paper was submitted in The 15th Korea Robotics Society Annual Conference (KRoC 2020)
<img src = "https://user-images.githubusercontent.com/57785895/122672101-c747b680-d204-11eb-98a2-559da425baa7.png" width = "35%" height= "35%">



# In-Memory Computing SRAM with Xnor CNN
<hr width="100%" color="black" size="5">

I developed a system accelerate CNN. It was organized with computable SRAM and optimized xnor-network CNN.  

![image](https://user-images.githubusercontent.com/57785895/122672672-ca907180-d207-11eb-9151-dd5e3029a643.png)


Sequence : Convolution → BatchNormalize → Binarize Input & Weight of other layers
Activation : tanh (can't use RELU for XNOR NET)
![image](https://user-images.githubusercontent.com/57785895/122672560-1989d700-d207-11eb-9c7a-a633b143a9e1.png)


![image](https://user-images.githubusercontent.com/57785895/122672518-d2034b00-d206-11eb-854b-2a701d50788e.png)

![image](https://user-images.githubusercontent.com/57785895/122672596-4938df00-d207-11eb-9aa8-111f5744af34.png)

![image](https://user-images.githubusercontent.com/57785895/122672631-93ba5b80-d207-11eb-99f4-86e4df5a0fc4.png)


![image](https://user-images.githubusercontent.com/57785895/122672608-62da2680-d207-11eb-8cba-6eda388ff9e0.png)


# Learning Based Kalman Filter
<hr width="100%" color="black" size="5">

To automatically determine parmeters of the Kalman filter Using machine learning and convex optimization. In other words, learing the parameters of kalmanfiter

Kalman filtering problem of a dynamic system can be expressed as convex optimization form like below.   
![image](https://user-images.githubusercontent.com/57785895/100961621-1595b080-3566-11eb-9f52-dbb18d07e178.png)


Goal is obtain proper value of **τ** and **Q** using machine learning

 
**Result animation** (blue = Groundtruth, orange = estimated position of robot)
![kf_animaint_1](https://user-images.githubusercontent.com/57785895/99908174-6dd9e080-2d24-11eb-841c-63a924860943.gif)


# Quadruped Spider Robot
<img src = "https://user-images.githubusercontent.com/57785895/122671822-6ec3e980-d203-11eb-96cf-5beb25e27908.png" width="50%" height="50%">

# Blitzcrank Robot
<img src = "https://user-images.githubusercontent.com/57785895/122671813-62d82780-d203-11eb-8aae-cf9e5e14d6d4.png" width="35%" height="35%">

