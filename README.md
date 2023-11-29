# JoTyMo.github.io

Welcome to the JoTyMo.github.io wiki!

<img width="494" alt="github" src="https://github.com/Whitewolfef138/JoTyMo.github.io/assets/80634197/9f68432a-616f-4df9-94f9-c846767219b3">


This is a brief introduction on how to work with JoTyMo.

You need to first preprocess the images. You can take these images either from the Sapiens PartNet-Mobility dataset or you can ask TaarLab to share the images with you.

There are two types of preprocess, one being the preprocess for joint classification and other being for joint movement detection. Both these are needed before training the networks.

After preprocessing is done, simply have a network be trained on the data. You can train from the scratch using CNN_classify and CNN_movement, or you can load the .h or .keras files and use JoTyMo weights a preprocessor for your own system. Other files were written for the paper and are for testing or visualization of the results and don't have any type of commercial usage.

If you have any questions, ask me here on GitHub and I'll get back to you as soon as possible.

The rest of this Read me talks about the paper it self. 

This paper presents a CNN-based network architecture
aimed to classify and detect joint types within Articulated
objects, specifically the Push-P joints, P-joints, R-joints and
objects lacking joints. The movement modeling of the detected
objects is explored by processing pre and post interaction RGB
images within the SAPIEN PartNet-Mobility dataset. In order to
achieve this, an architecture is proposed to leverage consecutive
CNN encoders based on the VGG architecture, in order to classify
joints based on pre and post-interaction images. Additionally,
in order to detect the effect-point and movement vector, a
convolutional encoder is applied for each joint type. Moreover, extensive
evaluation is made to showcase the results, achieving 96%
accuracy in joint classification and 94% accuracy in regression
on the considered dataset.

The proposed method introduced in this work aims at
determining whether an object possesses joints, identify the
specific type of joint, understand its range of motion, and
pinpoint the possible grasping point for effective joint manipulation
of Articulated obejcts available in PartNet-Mobility
dataset.
[examples.pdf](https://github.com/Whitewolfef138/JoTyMo.github.io/files/13500773/examples.pdf)

