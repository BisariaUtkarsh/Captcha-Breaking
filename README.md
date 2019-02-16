# Captcha Breaking using Deep Learning

## Introduction

In this project a CNN model is trained to identify the letters in captcha and hence break the captcha. The problem in hand is training data had 4-letter CAPTCHAs using a random mix of four different fonts and characters "O" and "I" are not used to avoid confusion with "0" and "1". That leaves a total of 32 possible letters and numbers that we need to recognize.

## Toolset

<ul>
  <li>Python3</li>
  <li>OpenCV</li>
  <li>Jupyter Notebook</li>
  <li>Tensorflow</li>
  <li>Keras</li>
</ul>

## Creating Dataset

Captcha Images are made of 4 letters so we try to seperate the 4 characters in image using opencv. Using OpenCV we figure out the contours( collection of pixels) and mark the border around each character. In some cases there were overlapping letters so model may identify two characters as one for that simply compare the width to height ratio which is if unusally large then divide the contour into two equal halfs. Now for each character in an image save it to its designated folder.

## Building and the Training Model

Use the extracted images to create a list of data and labels and the create a sequential model having two convolution layers along with max pooling and two fully connected layers and train the model. In 10 epochs of training, almost 99% accuracy is achieved.

## Prediction using Trained Model
<ul>
<li>Break up the CAPTCHA image into four separate letter images using the same approach used to create the training dataset.</li>
<li>Ask neural network to make a separate prediction for each letter image.</li>
<li>Use the four predicted letters as the answer to the CAPTCHA.</li>
</ul>



![insample_acc](./Accuracy1.PNG)

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
