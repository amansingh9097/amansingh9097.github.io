---
title: "Teaching AI to generate pickup lines for you"
layout: post
date: 2019-12-05
tag: 
- GenerativeModelling
- DeepLearning
- LSTM
- ArtificialIntelligence
- PickupLines
image: https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/ai-pickup-lines/walle.jpg
headerImage: false
description: "AI that generates Pickup Lines for you."
category: deep-learning
author: Aman Singh

---

# Teaching AI to generate pickup lines for you

So I decided to generate pickup lines using neural networks, to be specific its a [char-rnn](http://karpathy.github.io/2015/05/21/rnn-effectiveness/) model, a multi layer Recurrent Neural Network (LSTM, GRU, RNN) for character-level language models.<br>
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/ai-pickup-lines/char-rnn.PNG">

Why pickup lines you ask? Well, honestly its nothing new people have been generating names for the pokemon and recepies using the char-rnn models, its the same thing and I was curious to see it generate phrases and not just names.

Gathering the dataset was actually the most painful part. 
I scrapped more than 30 sites continuously for couple of days to finally come up with a dataset of roughly about 3800+ pickup lines.

Now the machine on its own doesn't understands the human language or the way we form sentences so it was pretty obvious that not everything that comes out of this model may make sense to any human. But it was still a fun to watch it form some of the words correctly.

Some of the pickup lines were really absurd, inappropriate, some are kind of cute while some don't make any sense at all and this was majorly because most of the pickup lines on the internet have word-plays or word puns which makes it really difficult for a machine to interpret.

I trained the model on my 16GB RAM core-i5 2.3Ghz CPU 1GB GPU machine for 3 complete days (my entire weekend Fri till Sun night) and it took me a solid 50 epochs after which the loss function converged to a point where it wasn't reducing any more.

Some of the lines generated after 10, 20 and 40 epochs looked something like this,
```
# after 10 epochs:
mooe a cou toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe toe

# after 20 epochs:
iete a picce of the poneet of the pay in the roiee of the pay in the roiee of the coeee of the poneet of the poeee of the pone of the poneet of the poeee of the coeee of the poneet of the poeee of the pone of the poneet of the poeee of the coeee of the poneet

# after 40 epochs: 
because you're she only hirl i want to sreal you to  the say wonen on your poccers. if you were a crink, i'd like to be your  dearty i'm not a thine, but i can tell you the soy of the partins of the  partins of the partins of the partins of the part of your poccer?
```

Finally, after 50 epochs these were some of the pickup lines generated:
```
    you have a map? because i want to take you
    i was wondering if you want to have my hand out of me.
    i was wondering if you want to have my hand put of my hand drive?
    i was wondering if you want to have my hand drome in your pants?
    you look like the most beautiful girl in the dark
    i love you like a pooder loves a sookel
    would you like to be the girl out?
    i wish i was a beautiful and i want to be my hine.
    i got and is hot and see my world
    want to take you to my place and watch me would be the best a cat io?
    i can tell you to my place and i look at tile all night.
    hi i have a vag
    i put u and i together.
    i want to be my hiart.
    in the poetteer in the brines loves the poetteer lover to me.
    u r a q t
    if i could
```
Clearly, the winner has to be the "you look like the most beautiful girl in the dark". This AI is gonna steal your girl.

<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/ai-pickup-lines/example.jpg">

--- 

If you liked this project, please consider buying me a coffee<br>
<style>.bmc-button img{height: 34px !important;width: 35px !important;margin-bottom: 1px !important;box-shadow: none !important;border: none !important;vertical-align: middle !important;}.bmc-button{padding: 7px 10px 7px 10px !important;line-height: 35px !important;height:51px !important;min-width:217px !important;text-decoration: none !important;display:inline-flex !important;color:#ffffff !important;background-color:#FF813F !important;border-radius: 5px !important;border: 1px solid transparent !important;padding: 7px 10px 7px 10px !important;font-size: 28px !important;letter-spacing:0.6px !important;box-shadow: 0px 1px 2px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;margin: 0 auto !important;font-family:'Cookie', cursive !important;-webkit-box-sizing: border-box !important;box-sizing: border-box !important;-o-transition: 0.3s all linear !important;-webkit-transition: 0.3s all linear !important;-moz-transition: 0.3s all linear !important;-ms-transition: 0.3s all linear !important;transition: 0.3s all linear !important;}.bmc-button:hover, .bmc-button:active, .bmc-button:focus {-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;text-decoration: none !important;box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;opacity: 0.85 !important;color:#ffffff !important;}</style><link href="https://fonts.googleapis.com/css?family=Cookie" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/amansingh"><img src="https://cdn.buymeacoffee.com/buttons/bmc-new-btn-logo.svg" alt="Buy me a coffee"><span style="margin-left:15px;font-size:28px !important;">Buy me a coffee</span></a>