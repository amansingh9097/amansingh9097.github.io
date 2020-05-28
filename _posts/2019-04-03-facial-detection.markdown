---
title: "Facial Detection"
layout: post
date: 2019-04-03
tag:
- DeepLearning
- ComputerVision
- FacialDetection
image: https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/facial-detection/still_image.PNG
headerImage: true
projects: true
description: "A quick helper module for detecting faces among images and videos."
category: python
author: Aman Singh
---

This is a simple yet quick implementation of facial detection using the pretrained `Caffe` model. I created this as a helper module to be used in future projects whereever there could be a need to write a module to detect faces among images and videos.
 
- the `prototxt` file contains the model architecture i.e. the layers
- the `ResNet caffemodel` file contains the weights of the actual layers of the SSD (Single Shot Detection) model.

# How to run?

**for still images:**
```python
python detect_faces.py --image your-image-file.jpg --prototxt deploy.prototxt.txt \
      --model res10_300x300_ssd_iter_140000.caffemodel
```
**for videos:**
```python
python detect_faces_video.py --prototxt deploy.prototxt.txt --model res10_300x300_ssd_iter_140000.caffemodel
```

![](https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/facial-detection/video.gif)

Check out the [GitHub](https://github.com/amansingh9097/facial-detection) repo to know more.

--- 

If you liked this project, please consider buying me a coffee<br>
<style>.bmc-button img{height: 34px !important;width: 35px !important;margin-bottom: 1px !important;box-shadow: none !important;border: none !important;vertical-align: middle !important;}.bmc-button{padding: 7px 10px 7px 10px !important;line-height: 35px !important;height:51px !important;min-width:217px !important;text-decoration: none !important;display:inline-flex !important;color:#ffffff !important;background-color:#FF813F !important;border-radius: 5px !important;border: 1px solid transparent !important;padding: 7px 10px 7px 10px !important;font-size: 28px !important;letter-spacing:0.6px !important;box-shadow: 0px 1px 2px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;margin: 0 auto !important;font-family:'Cookie', cursive !important;-webkit-box-sizing: border-box !important;box-sizing: border-box !important;-o-transition: 0.3s all linear !important;-webkit-transition: 0.3s all linear !important;-moz-transition: 0.3s all linear !important;-ms-transition: 0.3s all linear !important;transition: 0.3s all linear !important;}.bmc-button:hover, .bmc-button:active, .bmc-button:focus {-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;text-decoration: none !important;box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;opacity: 0.85 !important;color:#ffffff !important;}</style><link href="https://fonts.googleapis.com/css?family=Cookie" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/amansingh"><img src="https://cdn.buymeacoffee.com/buttons/bmc-new-btn-logo.svg" alt="Buy me a coffee"><span style="margin-left:15px;font-size:28px !important;">Buy me a coffee</span></a>