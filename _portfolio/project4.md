---
title: UNet Image Segmentation
subtitle: Academic Research Project utilizing unet algorithm to conduct image segmentation aganist traffic light data
image: "assets/img/portfolio/03-thumbnail.jpg"
alt: Camera photo

caption:
  title: UNet Image Segmentation
  subtitle: Machine Learning
  thumbnail: "assets/img/portfolio/03-thumbnail.jpg"
---
This paper advances and builds on existing knowledge to introduce a novel solution with an already existing algorithm for detecting a traffic sign and estimate the boundary within and input image. Estimating the boundary of traffic signs within an image and classification of a shape class prediction, solved using a CNN. The proposed algorithm and method using a U-Net CNN is compared aganist existing CNN methods in terms of computational time, and accuracy of detection.

<img src="assets/img/portfolio/unet_result.png" alt="Traffic Sign Image Segmentation" width="600"><br/>
Traffic Sign Image Segmentation

Utilizing the UNet algorithm that is traditionally used for Medical Imaging, and utilizing it for image segmentation of traffic sign data. The Data sets were gathered from Kaggle opensource datasets and the training was done off a jupyter notebook.

The model was trained using tensorflow, building the model and tweaking the model configurations to maxmize model performance. I utilizied a Rectified Linear Unit Activation (ReLu) in between Convolution layers then trained for only 30 epochs as the model would reach reach maximum accuracy relatively quickly. 

<img src="assets/img/portfolio/unet_architecture.png" alt="UNet Model Architecture" width="600"><br/>
Unet Architecture

More details about the model can be found in the paper.


Research Project Final paper: 
<a href="assets/resu/EE8204_Final_Report.pdf" download="">
  <img src="assets/img/download_icon.png" style="width:60px; height:60px;">
</a>

<embed src="assets/resu/EE8204_Final_Report.pdf" type="application/pdf" class="col-lg-12" width="600" height="800" />
        

<b>Libraries:</b>
Some of the tools required to make this project work: 

<a href="https://www.mysql.com/">MySQL</a> - MySQL is a domain-specific language used in programming and designed for managing data held in a relational database management system. <br>
<a href="https://www.tensorflow.org/">TensorFlow</a> - TensorFlow is a free and open-source software library for machine learning and artificial intelligence. It can be used across a range of tasks but has a particular focus on training and inference of deep neural networks <br>
<a href="https://jupyter.org/">Jupyter Notebooks</a> - web-based interactive development environment for notebooks, code, and data.<br>
