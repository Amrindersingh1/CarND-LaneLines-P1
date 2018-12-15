# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images/solidWhiteCurve_res.jpg "DETECT LANE LINES"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consists of 6 steps. 
*Step 1 - Converted the image to grayscale.
*Step 2 - Applied Gaussian blur to the image. 
*Step 3 - Applied the Canny Transform I've chosen a `low_threshold=40` and `high_threshold=`120`, keeping a ratio 1:3.
*Step 4 - Limited the area in a polygon shape where the lanes are. 
*Step 5 - Applying the Hough lines and tuning the parameters.
*Step 6 - overlaying the original image with Hough lines.

![alt text][image1]: 


### 2. Identify potential shortcomings with your current pipeline


*One potential shortcoming would be the are is limited to a static polygon assuming our viewing area will be that but it wont work in case of curves or bent roads and a lot of other conditions.
*The lane line detection doesnt work as expected with change in lightning conditions and shadows.
*It can only indentify lane line in daylight at night it would be impossible to detect lane lines
*The line with gap in lane line flactuates as road moves not providing a completely perfect line
*what about when lane line color is faded away like on old roads ot would not identify lines there

### 3. Suggest possible improvements to your pipeline
*The biggest possible improvement would be playing around with parameters to find a perfect balance or even dynamically generate those parameters based on certain conditions.
*instead of just identifying lines, identifying lane area would be more useful
*dynamically generating polygon restrictions for our region of interest would help to identify in curved roads and changing prespective
