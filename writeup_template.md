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
6. Project references from the web: (https://medium.com/@c.ramprasad273/self-driving-car-nanodegree-udacity-project-1-finding-lane-lines-on-the-road-6b3c208aeada)

### 2. Results:

Video 1: In folder: "test_videos_output/solidWhiteRight.mp4"

### 3. Potential shortcomings with your current pipeline

* One potential shortcoming would be what would happen when the color of lines are not white;
* Another shortcoming could be the detection of lines when is night.


### 4. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
