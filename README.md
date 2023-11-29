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

For joint type detection and classifying Articulated objects,
two RGB images of the size 224 × 224 × 3 are resized into
96 × 96 × 3 images. These images are then inputted into a
convolutional layer separately, as depicted in the first half
of Fig. 3. The resulting shape of each smaller convolutional
layer is 21 × 21 × 96. Subsequently, these two outputs are
concatenated to produce a 21 × 21 × 192 vector, which in
turn is passed into another CNN for classification purposes.
Within each convolutional layer of JoTyMo, a design inspired
by VGG-16 was implemented. VGG based layers were chosen
to avoid complex structures, similar to the studies conducted. Each convolutional layer involved utilization of a
Conv2D layer, followed by a dropout layer, and then another
Conv2D layer. Subsequently, batch normalization was applied
for stable training, followed by max pooling. Moreover, the
ConvD layers employ kernel sizes of 3 × 3, while the pool
size in the MaxPooling layers is 2 × 2.
For the purpose of this study, SoftMax is employed after the dense layers in order to achieve
a classifier model, where probability of two images being in
each class is estimated. Additionally, in JoTyMo, Rectified
Linear Units (ReLU) are applied to the activation functions in
both CNN layers and fully-connected layers. The applied loss function is the Categorical
Cross Entropy, enabling the generation of output probabilities
for each grouped category. To summarize, the main goal of
the initial segment of the architecture seen in Fig. 3 consists
of obtaining a transformation function from two input images
to the class probability by extracting features from the input
images.

