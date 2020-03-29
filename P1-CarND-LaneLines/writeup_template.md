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

My pipeline (lane line function) consisted of 5 steps. First, I converted the images to grayscale.  Then I done a gaussian blur with a kernel size of 7 to remove  noise of the image. After that, I do edge detect using canny with low threshold of 100 and high threshold of 250. Then I mask the image to only show the region of interest withich is the area of the right and left lane the car follows. finally, I convert the pixel point to a line using hough transform with weight_img to add the lines to the orignial image 

In order to draw a single line on the left and right lanes,  I modified the draw_lines() function by first finding the x & y points that belongs to the left or right side of the image. the I calculate the slope and intercept of each lane and find the maximum and minim points. then fined the proper x y point using the liner line function y = Xm+b 



### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what it can not run well in very noise images our curved roads.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use advanced lane detection 
 
