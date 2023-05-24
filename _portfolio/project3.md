---
title: Robotic Painting Quality Control
subtitle: How do you tell if two paintings are the same? 
image: "assets/img/portfolio/compare_mona.jpg"
alt: Paint picture

caption:
  title: Computer Vision Painting
  subtitle: Computer Vision
  thumbnail: "assets/img/portfolio/compare_mona.jpg"
---

<style> 
.noPadding { 
  margin: 0px !important;
  border: 0px solid brown; 
} 
</style> 

Museum curators spend millions of dollars every where to determine fake paintings from the real ones. <a href="https://news.harvard.edu/gazette/story/2017/06/teaching-tomorrows-curators-how-to-spot-a-fake/"> Teaching curators to spot fake paintings</a> and determine real stroke marks has always been a major challenge even with carbon dating. Utilizing computer vision to devise a method to compare painting stroke types or to perform some preliminary sweeps before a human will need to go in and look at the paintings, similar to applicant tracking systems and filtering resumes and cover letters before they are ever seen by a real person.

<h5>Some questions that needed to be answered were:</h5> 
1. Are there methods to infer what paint brush was used for a specific paint stroke? 
2. What is the best way to tell between two brush strokes with the exact same colour, and the exact same brush?

Starting with creating a pipeline to set up data base and data segmentation. Developing a dataset of paintings and individual paint strokes for comparison.
<figure style="text-align: center;">
<img src="assets/img/portfolio/compare_mona.jpg" alt="Comparing paintings" width="700" class="noPadding"><figcaption>
    <em> How do you tell if a painting is the same?</em>
  </figcaption>
</figure>

                                    
Multiple comparison scores are developed using OpenCV2. Colour matching, skeletoning, and texture detection are all run through the library to compare two paint strokes. Produced visual reports and comparison data to give an overall score on painting stroke types.

Skeletionization of stroke types using basic morphological operations
<figure style="text-align: center;">
<img src="assets/img/portfolio/skeleton_border.png" alt="Skeletonization Example" width="700"  class="noPadding"> <figcaption>
    <em>Example of skeletonization</em>
  </figcaption>
</figure>

Performing thresholding, first converting an image to grayscale then into a binary image. Choosing a specific threshold, and pixels with values greater than the threshold will be white (255), and similar will be converted to black (0).

<figure style="text-align: center;">
<img src="assets/img/portfolio/thresholding.png" alt="Thresholding Example" width="700" class="noPadding"> <figcaption>
    <em>Example of thresholding</em>
  </figcaption>
</figure>

With thresholding only, there are parts of the image that might not be what we are looking for. In the example above notice that there are pixels between the cell images that we are not interested in. To remove these unwanted pixels, running basic morphological operations on the thresholded images.

<h5>Dilating and Erosion:</h5>
Dilating adds pixels to the boundaries of objects while erosion removes pixels on the object boundaries.

<figure style="text-align: center;">
<img src="assets/img/portfolio/dilation.png" alt="Dilation Example" width="500" class="noPadding"><figcaption>
    <em>Example of Dilation</em>
  </figcaption>
</figure> 

<figure style="text-align: center;">
<img src="assets/img/portfolio/erosion.png" alt="Erosion Example" width="500" class="noPadding"><figcaption>
    <em>  Example of Erosion</em>
  </figcaption>
</figure>

Performing simple morphological operations after thresholding to get skeletonized images of paint strokes. Then running comparison of the skeletonized images by pixel values to compare paint strokes.

This was one of the many techniques used to compare images. Multiple additional processes done to compare the strokes provided a numerical percentage value of likeness. The full repository is private for company usage but this was simply an example of the operatons completed.

Potential future work is the utilization of GANs to create and mimic the paintings, then have the algorithm compare between the original paining the GAN created painting.

<br />
<br />
<h4>Libraries:</h4>
Some of the tools required to make this project work: 
<br>
<a href="https://pypi.org/project/opencv-python/">OpenCV2</a> - An open source computer vision and machine learning software library.<br>
<a href="https://scikit-learn.org/stable/">Scikit-Learn</a> - An open source Machine learning library in python used for data preprocessing, classification, regression, etc... <br>
<a href="https://jupyter.org/">Jupyter Notebooks</a> - web-based interactive development environment for notebooks, code, and data.<br>
                                    