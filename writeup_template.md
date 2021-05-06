# **Finding Lane Lines on the Road** 

## Writeup


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

![Image1](test_images_output/whiteCarLaneSwitch.jpg)
![image2](test_images_output/solidWhiteRight.jpg)
---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 8 steps. First I filtered white and yellow pixels, then I converted the images to grayscale,<br/> then I 
applied gausian blur, then I used canny transfor, then I set region of interest,<br/>
then I used hugh lines, divide lines to left and right, then I used linear regression to find lane lines,<br/>
then I drawed the line. 
Finally i used weighted image to merge initial image with detected lanes.<br/> 

In order to draw a single line on the left and right lanes, <br/>
I modified the draw_lines() function by selecting left and right lines.<br/>
Then in draw_line() function i used linear regression to find best aproximation.<br/>




### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when someone drive at night, in snow. 

Another shortcoming could be glare on the road or some other reflections that could be detected as extra line.

Another shortcoming would be patches on asphalt algorithm could detect some extra lines.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to optimize parameters

Another potential improvement could be to tune color filtering and region of interest. 

Another potential improvement could be to tune to diffrent wheather condition.
