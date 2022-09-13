---
title: Robotic Painting Quality Control
subtitle: Computer Vision 
image: "assets/img/portfolio/01-thumbnail.jpg"
alt: Paint picture

caption:
  title: Computer Vision Painting
  subtitle: Computer Vision
  thumbnail: "assets/img/portfolio/01-thumbnail.jpg"
---

Utilizing computer vision to devise a method to compare painting stroke types. 

Some questions that needed to be answered were: Are there methods to infer what paint brush was used for a specific paint stroke? What is the best way to tell between two brush strokes with the exact same colour, and the exact same brush?

Created a pipeline to set up data base and data segmentation. Developed a dataset of paintings and individual paint strokes for comparison.

<img src="assets/img/portfolio/compare_mona.jpg" alt="Comparing paintings" width="700"> How do you tell if a painting is the same?
                                    
Multiple comparison scores are developed using OpenCV2. Colour matching, skeletoning, and texture detection are all run through the library to compare two paint strokes.

Produced visual reports and comparison data to give an overall score on painting stroke types.

Skeletionization of stroke types using basic morphological operations
<img src="assets/img/portfolio/skeleton.png" alt="Skeletonization Example" width="700"> Example of skeletonization

Performing thresholding, first converting an image to grayscale then into a binary image. Choosing a specific threshold, and pixels with values greater than the threshold will be white (255), and similar will be converted to black (0).

<img src="assets/img/portfolio/thresholding.png" alt="Thresholding Example" width="700"> Example of thresholding

With thresholding only, there are parts of the image that might not be what we are looking for. In the example above notice that there are pixels between the cell images that we are not interested in.

To remove these unwanted pixels, running basic morphological operations on the thresholded images.

Dilating and Erosion:
Dilating adds pixels to the boundaries of objects while erosion removes pixels on the object boundaries.

<img src="assets/img/portfolio/dilation.png" alt="Dilation Example" width="700"> Example of Dilation

<img src="assets/img/portfolio/erosion.png" alt="Erosion Example" width="700"> Example of Erosion

Performing simple morphological operations after thresholding to get skeletonized images of paint strokes. Then running comparison of the skeletonized images by pixel values to compare paint strokes.

This was one of the many techniques used to compare images. Multiple additional processes done to compare the strokes provided a numerical percentage value of likeness. The full repository is private for company usage but this was simply an example of the operatons completed.


<b>Libraries:</b>
Some of the tools required to make this project work: 

<a href="https://pypi.org/project/opencv-python/">OpenCV2</a> - An open source computer vision and machine learning software library.<br>
<a href="https://scikit-learn.org/stable/">Scikit-Learn</a> - An open source Machine learning library in python used for data preprocessing, classification, regression, etc... <br>
<a href="https://jupyter.org/">Jupyter Notebooks</a> - web-based interactive development environment for notebooks, code, and data.<br>
                                    