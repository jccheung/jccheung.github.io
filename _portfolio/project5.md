---
title: Dog Breed Identification
subtitle: Prediction and Detection of Different Dog Classes
image: "assets/img/portfolio/01-thumbnail.jpg"
alt: Dog Image

caption:
  title: Dog Breed Identification
  subtitle: Computer Vision
  thumbnail: "assets/img/portfolio/01-thumbnail.jpg"
---

<style> 
.noPadding { 
  margin: 0px !important;
  border: 0px solid brown; 
} 
</style> 
Image classification has many excellent datasets for determining all types of classes, from humans, to airplanes to cats. VOC2012, a competition known as the Visual Object Classes Challenge to build a image database that has 20 clases ranging from persons, animals, vehicles and indoor furnitures. There is a classification for dogs, but not for dogs, so building upon this competition I wanted to train my own model to predict dog breeds.
<br />
<br />
This paper is built off of <a href ="https://arxiv.org/abs/1506.01497">[R-CNN: Towards Real-Time Object Detection with Region Proposal Networks] </a>written in PyTorch to determine the bounding boxes and prediction values for the dog breeds. 
<br />
<br />
<h5>Some questions that needed to be answered were:</h5>

1. How many dog breeds are trained? <br>
2. How is the data stored and organized, how are the features extracted. <br>

<br>
The dataset used was collected from the <a href ="http://vision.stanford.edu/aditya86/ImageNetDogs/main.html">[Stanford Dogs Dataset] </a>with total of 120 categories, with annotations for class labels and bounding boxes in PASCAL VOC format. This meant the data needed to be in XML and JPG files like the following. 
<br />
<br />

<figure style="text-align: center">
<img src="assets/img/portfolio/file_direc.JPG" alt="Comparing data folders" width="700" class="noPadding"> 
 <figcaption style="text-align: center"><em>Data Directory style</em>
 </figcaption>
</figure>

For each image, there is an XML file that defines the size of the image, the class name as well as the bounding box location.
<br />
<br />

<figure style="text-align: center">
<img src="assets/img/portfolio/XML_file.JPG" alt="xml file contents" width="500" class="noPadding"> 
  <figcaption style="text-align: center">
    <em>XML file contents, notice the coordinates xmin, xmax and ymin, ymax showing the coordinates of the bounding boxes </em>
  </figcaption>
</figure>

The data was then run through simple preprocessing morphological operations such as rotating, shifting as well as mirroring the images, to increase the size of the dataset and provide the algorithm with even more input data.
<br />
<br />
The machine learning algorithm is trained with the new dog breed classes and is compiled to learn and write the bounding boxes as an output. Postman is used as the testing and API call as it is upload to a localhost web server to try to receive POST calls from the server. 
<br />
<br />

<figure style="text-align: center">
<img src="assets/img/portfolio/terminal.png" alt="local terminal" width="700" class="noPadding">
  <figcaption  style="text-align: center">
    <em>Localhost</em>
  </figcaption>
</figure>

<figure style="text-align: center">
<img src="assets/img/portfolio/start_up_border.JPG" alt="Webpage start" width="700" class="noPadding">
<figcaption>
    <em>Webpage startup</em>
  </figcaption>
</figure>

<br />
Here we can see the output result, the dog breed, as well as the prediction result in a tensor. The algorithm is 75% certain that this is an image of a Tibetan Mastiff, which is correct. This project was a demonstration of creating and replicated an algorithm from a journal article, as well as usage of an API platform for building a machine learning API in the future. 
<br>

<figure style="text-align: center;">
<img src="assets/img/portfolio/output.png" alt="Output Example" width="700" class="noPadding"> <figcaption>
    <em>Sad looking doggo</em>
  </figcaption>
</figure>

<br />
Additional work would be to include much more dog classes to the algorithm for training as well as work on the accuracy of the model to have higher certainty of the prediction. In addition, making the webpage look alittle better than a blank page with text. The github will continue to be updated to make these changes.
<br />
<br />
<br />
<h4>Libraries:</h4>
Some of the tools required to make this project work: 
<br>
<a href="https://pypi.org/project/opencv-python/">OpenCV2</a> - An open source computer vision and machine learning software library.<br>
<a href="https://scikit-learn.org/stable/">Scikit-Learn</a> - An open source Machine learning library in python used for data preprocessing, classification, regression, etc... <br>
<a href="https://www.postman.com/">Postman</a> - Postman is an API platform for building and using APIs. Postman simplifies each step of the API lifecycle and streamlines collaboration <br>
<a href="https://jupyter.org/">Jupyter Notebooks</a> - web-based interactive development environment for notebooks, code, and data.<br>
