# Convolutional neural networks for artistic style transfer

![Author credit and first slide page](notebooks/images/Author_front)

This repository contains (TensorFlow and Keras) code that goes along
with a [related blog post][blog-post] and [talk
(PDF)][talk-slides]. Together, they act as a systematic look at
convolutional neural networks from theory to practice, using artistic
style transfer as a motivating example. The blog post provides context
and covers the underlying theory, while working through the Jupyter
notebooks in this repository offers a more hands-on learning
experience.

## Contents

### iPython Notebooks

1. [A linear classifier for MNIST data][linear-mnist]
2. [A neural network-based classifier for MNIST data (Attempt 1)][neural-mnist-1]
3. [A neural network-based classifier for MNIST data (Attempt 2)][neural-mnist-2]
4. [A convolutional neural network-based classifier for MNIST data][convnet-mnist]
5. [VGG Net (16) on ImageNet, the easy way][vggnet-imagenet]
6. [Artistic style transfer with a repurposed VGG Net (16)][style-transfer]

### External Resources

1. [Related blog post][blog-post]
2. [Related talk slides][talk-slides]


[blog-post]: https://harishnarayanan.org/writing/artistic-style-transfer/
[talk-slides]: https://www.dropbox.com/s/969r7dj5nlboh7v/slides.pdf?dl=1
[support-issue]: https://github.com/hnarayanan/artistic-style-transfer/issues
[twitter]: https://twitter.com/copingbear
[linear-mnist]: notebooks/1_Linear_Image_Classifier.ipynb
[neural-mnist-1]: notebooks/2_Neural_Network-based_Image_Classifier-1.ipynb
[neural-mnist-2]: notebooks/3_Neural_Network-based_Image_Classifier-2.ipynb
[convnet-mnist]: notebooks/4_Convolutional_Neural_Network-based_Image_Classifier.ipynb
[vggnet-imagenet]: notebooks/5_VGG_Net_16_the_easy_way.ipynb
[style-transfer]: notebooks/6_Artistic_style_transfer_with_a_repurposed_VGG_Net_16.ipynb


## Run on FloydHub

First of all, create a new FloydHub project following [this guide](http://docs.floydhub.com/guides/basics/create_new/), then install the [Floyd-CLI](http://docs.floydhub.com/guides/basics/install/) and run the [login command](http://docs.floydhub.com/guides/basics/login/). After logged in, we are ready to get our hands dirty with this amazing tutorial which covers the basic concepts of Machine Learning, Deep Learning and style transfer.

I have chosen to split the tutorial in two parts: the first one which can be followed with a CPU-instance and the other one with a GPU instance to speed up the training.

### PART 1 - CPU INSTANCE

With a CPU instance you will be able to run the following Notebooks:

1. [Linear Image Classifier](notebooks/1_Linear_Image_Classifier.ipynb)
2. [Neural Network based Image Classifier](notebooks/2_Neural_Network-based_Image_Classifier-1.ipynb)
3. [Neural Network based Image Classifier-2](notebooks/3_Neural_Network-based_Image_Classifier-2.ipynb)

Floyd-CLI command:

```bash
floyd run --env tensorflow-1.0:py2 --data redeipirati/datasets/mnist/1:input --mode jupyter
```

Note:

I've already uploaded for you the [MNIST](https://www.floydhub.com/redeipirati/datasets/mnist) dataset if you want to play with it. FloydHub instances have an impressive internet connection, so you can omit the data parameter because the dataset will be download in a few milliseconds.


### PART 2 - GPU INSTANCE

I reccomend to run these notebook with a GPU instance(it should take about 5/4 minutes per training vs about an hour on a CPU instance):

4. [Convolutional Neural Network based Image Classifier](notebooks/4_Convolutional_Neural_Network-based_Image_Classifier.ipynb)
5. [VGG Net 16 the easy way](notebooks/5_VGG_Net_16_the_easy_way.ipynb)
6. [Artistic style transfer with a repurposed VGG Net 16](notebooks/6_Artistic_style_transfer_with_a_repurposed_VGG_Net_16.ipynb)

Floyd-CLI command:

```bash
floyd run --gpu --env tensorflow-1.0:py2 --data redeipirati/datasets/mnist/1:input --mode jupyter
```

Note:

Notebooks 5 and 6 will download the VGGnet pretrained models(about 800MB of data), but as i said before they will be download in a few seconds.


### Contribution

For any questions, bug(even typos) and/or features requests do not hesitate to contact me or open an issue!
