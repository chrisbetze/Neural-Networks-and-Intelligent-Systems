# Image Classification with CIFAR-100 (Deep Learning)
Performance optimization of Deep Learning models in the CIFAR-100 dataset using the TensorFlow 2 library
![download](https://user-images.githubusercontent.com/50949470/111167989-4eecac00-85aa-11eb-97c8-59d0adf23905.png)
## Dataset preview
The CIFAR-100 dataset consists of 100 classes containing 600 images (32x32 colour) each. There are 500 training images and 100 testing images per class.
The 100 classes in the CIFAR-100 are grouped into 20 superclasses. For more information visit [DIFAR Dataser](https://www.cs.toronto.edu/~kriz/cifar.html).
## Memory management
We use TensorFlow Record ([TFRecord](https://www.tensorflow.org/tutorials/load_data/tfrecord#tftrainexample)) format for storing and reading our dataset. 
A TFRecord is when a sequence of records serializes to binary. The binary format takes less memory for storage in comparison to any other data formats. 
[Protocol buffers](https://developers.google.com/protocol-buffers/) are a cross-platform, cross-language library for efficient serialization of structured data.
## Network models
### "From scratch"
We develop three simple Convolutional Neural Networks "From Scratch" based on "LeNet".
### Transfer Learning
We use transfer learning of TensorFlow 2 from a pre-trained network. Specifically, we use [tf.keras.applications](https://www.tensorflow.org/api_docs/python/tf/keras/applications), which provides pre-trained models from Keras such us: VGG16, MobileNetV2, ResNet50, VGG19, Xception, DenseNet121, EfficientNetB7 and InceptionV3.
## Criteria - Μetrics
In order to choose which model we proceed in the optimization phase, we examine the above models based on following:
* Memory Usage
* Trainable Parameters
* Training Time
* Accuracy
## Optimization - Preprocessing
We improve the classification results, experimenting with some techniques and parameters:
* Data augmentation (Rotation, Flip, Zoom, Contrast, etc)
* Size of input image (32x32, 96x96, 128x128, etc)
* Freezing / Unfreezing layers
* Dropout (Regularization)
* Early Stopping
* Parameters, such us: learning rate, batch size, optimizers
## Results
The final optimal network model resulted with transfer learning from the pre-trained model DenseNet121. This is a network in which, each layer is connected to all the followings. Having run 100 epochs, after the preprocessing and the optimization, we achieve an accuracy of 92% in 20 classes and 84% in 80 classes.
