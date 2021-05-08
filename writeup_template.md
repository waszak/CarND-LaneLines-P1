# **Finding Lane Lines on the Road** 

## Writeup


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 8 steps.<br/> 
![image1](test_images/whiteCarLaneSwitch.jpg)

First I filtered white and yellow pixels<br/>
![image2](test_images_output/color_filter_whiteCarLaneSwitch.jpg)

then I converted the images to grayscale,<br/> 
![image3](test_images_output/gray_scale_whiteCarLaneSwitch.jpg)

then I applied gausian blur, <br/> 
![image4](test_images_output/gaussian_whiteCarLaneSwitch.jpg)

then I used canny transfor, <br/>
![image5](test_images_output/canny_whiteCarLaneSwitch.jpg)

then I set region of interest,<br/>
![image6](test_images_output/region_whiteCarLaneSwitch.jpg)

then I used hugh lines, divide lines to left and right, then I used linear regression to find lane lines,<br/>
then I drawed the line. 
![image7](test_images_output/hough_lines_whiteCarLaneSwitch.jpg)

Finally i used weighted image function to merge initial image with detected lanes.<br/> 
![image8](test_images_output/whiteCarLaneSwitch.jpg)


In order to draw a single line on the left and right lanes, <br/>
I modified the draw_lines() function by selecting left and right lines.<br/>
Then in draw_line() function i used linear regression to find best aproximation.<br/>




### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when someone drive at night, in snow, white cars <br/>

Another shortcoming could be glare on the road or some other reflections that could be detected as extra line.  <br/>

Another shortcoming would be patches on asphalt algorithm could detect some extra lines. <br/>

Distored images.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to focus more on images contating shadows like 
![image9](test_images/My_test.jpg)

Another potential improvement would be camera calibration. 
