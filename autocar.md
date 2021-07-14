---
layout: default
title: Intelligent Model Car competition
---
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


Following vedio is result

<!--iframe width="480" height="360" style="float:left; margin-right:2px" src="https://drive.google.com/file/d/16QfK1wCPetp34UF6whwQUNx0rrHLa6rU/preview" frameborder="0" allowfullscreen="">
</iframe>

<iframe width="480" height="360" style="float:left" src="https://drive.google.com/file/d/1Ds5f1gfT0gVwPCYufanFA7me8Jjs1t9R/preview" frameborder="0" allowfullscreen="">
</iframe-->
<video class = "mvideo" style="float:left; margin-right:2px" controls src="https://drive.google.com/uc?export=download&id=16QfK1wCPetp34UF6whwQUNx0rrHLa6rU" frameborder="0" allowfullscreen="">
</video>

<video class = "mvideo" style="float:left" controls src="https://drive.google.com/uc?export=download&id=1Ds5f1gfT0gVwPCYufanFA7me8Jjs1t9R" frameborder="0" allowfullscreen="">
</video>
