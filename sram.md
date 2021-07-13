---
layout: page
title: In-Memory Computing SRAM with Xnor CNN
---

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

