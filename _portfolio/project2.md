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

Private Repository for company usage.       

<b>Libraries:</b>
Some of the tools required to make this project work: 

<a href="https://pypi.org/project/opencv-python/">OpenCV2</a> - An open source computer vision and machine learning software library.<br><a href="https://scikit-learn.org/stable/">Scikit-Learn</a> - An open source Machine learning library in python used for data preprocessing, classification, regression, etc... <br>
<a href="https://jupyter.org/">Jupyter Notebooks</a> - web-based interactive development environment for notebooks, code, and data.<br>
                                    