# Learning to Segment Using Overlap Score
#### Deep Learning Project 2018-19
[![Oxford Engineering Science](https://www.eng.ox.ac.uk/images/logo.svg)](https://www.eng.ox.ac.uk/)

This repository is the top level repository for my 4th year project. The submodules are as follows:
* [code](https://github.com/HMellor/4YP_code) - The code written and used to carry out the experiments of this project.
* [logger](https://github.com/oval-group/logger) - A high level API for easy graph plotting in [Visdom](https://github.com/facebookresearch/visdom).
* [report](https://github.com/HMellor/4YP_report) - The writeup of the project and it's findings.

The purpose of this project is to enable the application of 'Overlap' or 'Intersection over Union' (IoU) score as a directly learned objective function in the deep learning problem of semantic segmentation.

Semantic segmentation of images is the assigning of semantic classes, such as cat/road/tree, to each pixel of the image and, IoU score is the proportion of the prediction that matches the ground truth, which is illustrated below: 

![](https://www.pyimagesearch.com/wp-content/uploads/2016/09/iou_equation.png)

## Acknowledgments

Thank you to:
* [M. Pawan Kumar](http://mpawankumar.info/) for supervising and guiding me in this project when needed.
* [L. Berrada](https://github.com/lberrada) for helping when there were details I didn't understand at first.
* [Meet P. Shah](https://github.com/meetshah1995/pytorch-semseg) for the codebase on which this project was built on.
