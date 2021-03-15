# Image Classification with CIFAR-100 (Deep Learning)
Performance optimization of Deep Learning models in the CIFAR-100 dataset using the TensorFlow 2 library
![download](https://user-images.githubusercontent.com/50949470/111167989-4eecac00-85aa-11eb-97c8-59d0adf23905.png)
## Dataset preview
The CIFAR-100 dataset consists of 100 classes containing 600 images (32x32 colour) each. There are 500 training images and 100 testing images per class.
The 100 classes in the CIFAR-100 are grouped into 20 superclasses. For more info click [here](https://www.cs.toronto.edu/~kriz/cifar.html)
## Memory management
We use TensorFlow Record ([TFRecord](https://www.tensorflow.org/tutorials/load_data/tfrecord#tftrainexample)) format for storing and reading our dataset. 
A TFRecord is when a sequence of records serializes to binary. The binary format takes less memory for storage in comparison to any other data formats. 
[Protocol buffers](https://developers.google.com/protocol-buffers/) are a cross-platform, cross-language library for efficient serialization of structured data.
## Network models
### "From scratch"
