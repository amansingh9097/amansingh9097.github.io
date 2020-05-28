---
title: "What Do Neural Networks dream of ?"
layout: post
date: 2019-12-08
tag: 
- DeepLearning
- DeepDream
- NeuralNetworks
- Google
image: https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/deep-dream/paris-deepdream-2.gif
headerImage: false
description: "Implementation of Google's Deep Dream Paper "
category: deep-learning
author: Aman Singh
hidden: false

---

# Deep Dream

To start off let me first give you an idea of what exactly is [DeepDream](https://en.wikipedia.org/wiki/DeepDream)?
Simply put it is a fun algorithm to generate psychedelic-looking images.

Okay, so [Google](https://en.wikipedia.org/wiki/Google) as we all know has been leading the game of image recognition and classification with its state-of-the-art projects/papers since forever. When creating these image recognition/classification tools the super-brainers at Google came up with a technique to help them understand and visualize how excatly neural networks are able to carry out different classification tasks so as to make any improvements in the neural network if needed and to check what exactly the neural network has learned over the course of training. But who knew this would turn out to be a fun artistic project where you could generate a remix of a number of visual concepts.

Normally we train a classification model by feeding it a number of training examples and then gradually adjusting the network parameters until the model learns to classify the examples correctly. Each training example is fed into the input layer which passes it to other layer which in turn does some computations (weight-adjustments at the nodes) and then this goes on to the next layer with some more computations (some more weight adjustments) until the output layer is reached which finally tells you what the object is in the training example.

---
Now lets turn this neural network upside-down and give it an image and tell it to draw out an interpretation of anything that it could see.
While it does that lets also ask it to enhance the weights of the nodes in the present layer so as to closely resemble its interpretation and then later feed this as an input coupled with the original input image to the next layer in the neural nets. This goes on for some time and until its interpretation starts taking a form in the original input image and voila your input image has changed altogether into something the neural network thought it saw in the image.

Easier said than done. When you tell a machine to interpret anything it could see, it doesn’t really know what to look for and what not to, it just sees a number of features but to actually get a sense of what any particular layer has learned, we need to maximize the activations through that layer. The gradients of that layer are set equal to the activations from that layer, and then gradient ascent is done on the initial input image, thereby, maximizing the activations of that layer and we say okay may be the neural nets observed some squares or strokes of lines in that image.

[source: YouTube<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/deep-dream/deep-dream-illustration.PNG">](https://www.youtube.com/watch?v=ws-ZbiFV1Ms&index=21&list=PL9Hr9sNUjfsmEu1ZniY0XpHSzl5uihcXZ&t=143s)

---
This however isn’t enough to produce a cool and distinguishable figure in the images. On top of all this interpretation and weight adjustment in gradient descent process, a number of image smoothing techniques like Gaussian blurring, repeated down-scaling, down-scaling while applying gradient descent and merging all such combinations into the final output image of the layer, etc etc are also applied.

Now when you take hundreds of such transformed images generated from the initial input image, put them as frames and join them using some codec into a video, you get yourself a beautiful psychedelic transformation of an image that looks more like a dream. Hence the name Deep Dream.

If you followed till here, you’d surely be thinking okay but where do I get that trained classifier model that Google trained on a bunch of images to use in my neural network model for creating cooler deep-dreams? Well, Google has many such models each with its own advantages and disadvantages. I used the Google’s “Inception model 5h for tensorflow”. This variant of Inception models is easier to use for deep-dream and other imaging techniques as it allows the input images to be of any size and the optimized images are more smoother comparatively.

---
Although it is unclear what all images the Inception model was initially trained on because Google developers have (as usual) forgotten to document it. Following is from what I could observe and make out of training the neural nets step by step at different layers,<br>
layer 1: mostly wavy lines<br>
layer 2: a lot line-strokes<br>
layer 3: boxes<br>
layer 4: circles<br>
layer 5: eyes, lots of creepy eyes<br>
layer 6: dogs, cats, bears, foxes<br>
layer 7: faces, buildings<br>
layer 8: fishes, frogs, reptilian eyes<br>
layer 10: monkeys, lizards, snakes, ducks and<br>
by layer 11 it was all bizarre and horrifying to express in words.

---
Here are a few attempts of generating a deep-dream visualizations on different images:

![](https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/deep-dream/paris-deepdream-1.gif)

![](https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/deep-dream/starry_night_deepdream.gif)

![](https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/deep-dream/paris-deepdream-2.gif)

---

Link to actual Google's actual [white paper](https://www3.cs.stonybrook.edu/~cse352/T12talk.pdf)
Check out the actual [GitHub](https://github.com/amansingh9097/Deep-Dream-implementation) repo.

--- 

If you liked this project, please consider buying me a coffee<br>
<style>.bmc-button img{height: 34px !important;width: 35px !important;margin-bottom: 1px !important;box-shadow: none !important;border: none !important;vertical-align: middle !important;}.bmc-button{padding: 7px 10px 7px 10px !important;line-height: 35px !important;height:51px !important;min-width:217px !important;text-decoration: none !important;display:inline-flex !important;color:#ffffff !important;background-color:#FF813F !important;border-radius: 5px !important;border: 1px solid transparent !important;padding: 7px 10px 7px 10px !important;font-size: 28px !important;letter-spacing:0.6px !important;box-shadow: 0px 1px 2px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;margin: 0 auto !important;font-family:'Cookie', cursive !important;-webkit-box-sizing: border-box !important;box-sizing: border-box !important;-o-transition: 0.3s all linear !important;-webkit-transition: 0.3s all linear !important;-moz-transition: 0.3s all linear !important;-ms-transition: 0.3s all linear !important;transition: 0.3s all linear !important;}.bmc-button:hover, .bmc-button:active, .bmc-button:focus {-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;text-decoration: none !important;box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;opacity: 0.85 !important;color:#ffffff !important;}</style><link href="https://fonts.googleapis.com/css?family=Cookie" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/amansingh"><img src="https://cdn.buymeacoffee.com/buttons/bmc-new-btn-logo.svg" alt="Buy me a coffee"><span style="margin-left:15px;font-size:28px !important;">Buy me a coffee</span></a>