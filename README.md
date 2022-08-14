# DeepLearning-Exploration
Some Deep Learning approaches in the areas of Image Generation, NLP and Music

# Idea and purpose of this project

As part of our studies, our goal was to explore the different areas of Deep Learning. For us, the main areas and benefits of Deep Learning architectures are processing  complex data structures such as images, audio and text.

We tried to cover some specific tasks and problems that we discovered while researching the areas.

# Generative Adversarial Networks
 GANs are the state-of-the-art in image generation and while researching them, we found out that some of the preceding work on them are very interesting to us and thus we arranged a little presentation about GANs and NVIDIAs inpainting research.
 You can watch the presentation in German here:
 https://www.youtube.com/watch?v=KkYoSRsQxEw
 
 After that we wanted to implement a little example code of GANs which you can find in the GAN folder. More specifically we found that CycleGANs are interesting in terms of switching up images and their styles. We used a landscaping dataset from tensorflow to switch up summer and winter seasons.
 You can see a result here:
 
<p align="center">
  <img width="550" height="420" src="https://user-images.githubusercontent.com/74551044/184554607-aba4db91-3f89-474a-aeb0-3274b513a56b.PNG">
</p>

Note that training with the notebook takes about 9 hours in google colab.


# NLP Text Classification with BERT

On the Text processing side of this project, we researched BERT to be the state-of-the-art in many tasks of NLP.
While researching about it we decided that a simple Text Classification is good for a basic understanding but not good enough for being interesting to our research. (because of the intuitive usage thanks to the Huggingface architecture)

While implementing the BERT Text-Classification, which you can see in the BERT folder, we asked ourselves what would happen if the texts we were training it with would have been classified wrongly in the first place, because the texts are rather long and might simply not be categorized by someone into the right category. This let us to experiment on training the model with different levels of noise, i.e. with 0%, 20%, 40% and 50% noise rates.

You can see the results of the accuracy measures on the train, validation and test data here:

<p Class="scaling" align="center">
  <img width="600" height="300" src="https://user-images.githubusercontent.com/74551044/184555330-6b36054e-11f3-4788-9282-46b7f0314dfe.PNG">
  <img width="600" height="300" src="https://user-images.githubusercontent.com/74551044/184555330-6b36054e-11f3-4788-9282-46b7f0314dfe.PNG">
</p> 

<p Class="scaling" align="center">
  <img width="200" height="130" src="https://user-images.githubusercontent.com/74551044/184555349-a6997b9c-d883-4030-9675-67aae3b57463.png">
</p>

# Audio Generation with GANs

After researching about Deep Learning with Audio Data we found out that this topic has not been researched very well as of yet.
The main topic of discussion in literature seems to be deciding whether to deal with Audio Data as sequential data or static data. Audio data in general seems to be more complicated than expected because it can seen as as complicated as video data, i.e. many complex data structures after another (sequence of images).
There seems to be a problem concerning models "getting the big picture" when trying to create music.

We didn't implement anything on this topic but we researched about GANs trying to generate music by handling it as static data.
This approach is called GANSynth and you can read about it here: https://magenta.tensorflow.org/gansynth
Another approach of music generation by handling it as sequential data and probably the most promising approach at the moment is an Autoregressive long-context music generator with Perceiver AR found here: https://magenta.tensorflow.org/perceiver-ar


In summary we found this research to be very enlightening and gave us a good insight on some state-of-the-art approaches for many different aspects of specific deep learning tasks and we encourage you to do your own reseach on them.
