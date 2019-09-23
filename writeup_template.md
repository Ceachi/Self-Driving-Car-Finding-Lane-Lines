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

### 1. Objectives

My pipeline consisted of 7 steps:
STEP 1: I converted the images to gray scale;
STEP 2: To reduce the noise in the image, I applied Gaussian Blur method, using kernel_size = 5;
STEP 3: To find the edges of the lane lines in an image of the road, I used Canny Edge Detection algorithm;
STEP 4: Then I marked the region of interest inside the image (4 vertices polygon, based on the dimensions of the image);
STEP 5: I applied Hough Transform to extract the lines that we want in the image;
STEP 6: I draw the lines in the image;
STEp 7: I test the algorithm on a video with the road.

### 2. Results:

Video 1: In folder: "test_videos_output/solidWhiteRight.mp4"

### 3. Potential shortcomings with your current pipeline

* One potential shortcoming would be what would happen when the color of lines are not white;
* Another shortcoming could be the detection of lines when is night.


### 4. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
