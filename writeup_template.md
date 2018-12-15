# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consists of 6 steps. 
Step 1 - Converted the image to grayscale.
Step 2 - Applied Gaussian blur to the image. 
Step 3 - Applied the Canny Transform I've chosen a `low_threshold=40` and `high_threshold=`120`, keeping a ratio 1:3.
Step 4 - Limited the area in a polygon shape where the lanes are. 
Step 5 - Applying the Hough lines and tuning the parameters.
Step 6 - overlaying the original image with Hough lines.

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
