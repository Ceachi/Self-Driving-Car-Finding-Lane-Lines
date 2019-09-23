# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project you will detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  

To complete the project, two files will be submitted: a file containing project code and a file containing a brief write up explaining your solution. We have included template files to be used both for the [code](https://github.com/udacity/CarND-LaneLines-P1/blob/master/P1.ipynb) and the [writeup](https://github.com/udacity/CarND-LaneLines-P1/blob/master/writeup_template.md).The code file is called P1.ipynb and the writeup template is writeup_template.md 

To meet specifications in the project, take a look at the requirements in the [project rubric](https://review.udacity.com/#!/rubrics/322/view)


Creating a Great Writeup
---
For this project, a great writeup should provide a detailed response to the "Reflection" section of the [project rubric](https://review.udacity.com/#!/rubrics/322/view). There are three parts to the reflection:

1. Describe the pipeline

2. Identify any shortcomings

3. Suggest possible improvements

We encourage using images in your writeup to demonstrate how your pipeline works.  

All that said, please be concise!  We're not looking for you to write a book here: just a brief description.

You're not required to use markdown for your writeup.  If you use another method please just submit a pdf of your writeup. Here is a link to a [writeup template file](https://github.com/udacity/CarND-LaneLines-P1/blob/master/writeup_template.md). 


The Project
---

## If you have already installed the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) you should be good to go!   If not, you should install the starter kit to get started on this project. ##

**Step 1:** Set up the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) if you haven't already.

**Step 2:** Open the code in a Jupyter Notebook

You will complete the project code in a Jupyter notebook.  If you are unfamiliar with Jupyter Notebooks, check out [Udacity's free course on Anaconda and Jupyter Notebooks](https://classroom.udacity.com/courses/ud1111) to get started.

Jupyter is an Ipython notebook where you can run blocks of code and see results interactively.  All the code for this project is contained in a Jupyter notebook. To start Jupyter in your browser, use terminal to navigate to your project directory and then run the following command at the terminal prompt (be sure you've activated your Python 3 carnd-term1 environment as described in the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) installation instructions!):

`> jupyter notebook`

A browser window will appear showing the contents of the current directory.  Click on the file called "P1.ipynb".  Another browser window will appear displaying the notebook.  Follow the instructions in the notebook to complete the project.  

**Step 3:** Complete the project and submit both the Ipython notebook and the project writeup

## How to write a README
A well written README file can enhance your project and portfolio.  Develop your abilities to create professional README files by completing [this free course](https://www.udacity.com/course/writing-readmes--ud777).



# **Finding Lane Lines on the Road** 

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Objectives

The concepts used from Computer Vision to implement this projects are: Color Selection, Grayscaling, Gaussian smoothing, Canny Edge Detection, Region of Interest Mask, Implementing a Hough Transform on Edge Detected Image.<br/>

My pipeline consisted of 7 steps: <br/>
* STEP 1: I converted the images to gray scale; 
* STEP 2: To reduce the noise in the image, I applied Gaussian Blur method, using kernel_size = 5; 
* STEP 3: To find the edges of the lane lines in an image of the road, I used Canny Edge Detection algorithm;
* STEP 4: Then I marked the region of interest inside the image (4 vertices polygon, based on the dimensions of the image); 
* STEP 5: I applied Hough Transform to extract the lines that we want in the image; 
* STEP 6: I draw the lines in the image; <br/>
* STEP 7: I test the algorithm on a video with the road. <br/>

Some simple code examples, vor every step: <br/>
(https://github.com/Ceachi/Self-Driving-Car-Finding-Lane-Lines/tree/master/computer_vision_concepts) <br/>

Links:
1. Why do we convert RGB to GrayScale: (https://www.quora.com/In-image-processing-applications-why-do-we-convert-from-RGB-to-Grayscale)
2. Finding Edges: (https://www.youtube.com/watch?v=uihBwtPIBxM)
3. Canny Edge Detector: (https://www.youtube.com/watch?v=sRFM5IEqR2w)
4. Gaussian Blur: (https://www.youtube.com/watch?v=C_zFhWdM4ic)
5. Hough Transform: (https://www.youtube.com/watch?v=4zHbI-fFIlI)
6. Other: (https://medium.com/@c.ramprasad273/self-driving-car-nanodegree-udacity-project-1-finding-lane-lines-on-the-road-6b3c208aeada)

### 2. Results:

Program results: In folder: "test_videos_output/solidWhiteRight.mp4"

### 3. Potential shortcomings with your current pipeline

* One potential shortcoming would be what would happen when the color of lines are not white;
* Another shortcoming could be the detection of lines when is night.


### 4. Suggest possible improvements to your pipeline

* A possible improvement would be to use another efficient detection algorithm and to study how to find white/yellow color
more efficiently.
* Another potential improvement could be to implement a parallel/distributed algorithm for this pipeline algorithm.


