# CNN-architectures

I developed a new summary technique for neural network visualization. Rather than Keras' summary function, my technique is much more simpler and easy to understand input and output connections. Additionally, I display the activation functions in each layer.

For example, a couple of layers of VGG16 architecture displayer by Keras' summary function:
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
input_2 (InputLayer)         (None, 224, 224, 3)       0         
_________________________________________________________________
block1_conv1 (Conv2D)        (None, 224, 224, 64)      1792      
_________________________________________________________________
block1_conv2 (Conv2D)        (None, 224, 224, 64)      36928     
_________________________________________________________________
block1_pool (MaxPooling2D)   (None, 112, 112, 64)      0         
_________________________________________________________________
block2_conv1 (Conv2D)        (None, 112, 112, 128)     73856     
_________________________________________________________________
block2_conv2 (Conv2D)        (None, 112, 112, 128)     147584    
_________________________________________________________________
block2_pool (MaxPooling2D)   (None, 56, 56, 128)       0         
_________________________________________________________________
...


and a couple of layers of VGG16 architecture displayer by my summary function:

---------------------------------------------------------------------------------------------------------
     Layer Type       Layer Dimensions       Activation           Output Shape                Param #    
---------------------------------------------------------------------------------------------------------
     InputLayer             None                None           (None, 224, 224, 3)               0       
         Conv2D        (3, 3, 3, 64)            relu          (None, 224, 224, 64)             1792      
         Conv2D        (3, 3, 64, 64)           relu          (None, 224, 224, 64)             36928     
   MaxPooling2D             None                None          (None, 112, 112, 64)               0       
         Conv2D       (3, 3, 64, 128)           relu          (None, 112, 112, 128)            73856     
         Conv2D       (3, 3, 128, 128)          relu          (None, 112, 112, 128)           147584     
   MaxPooling2D             None                None           (None, 56, 56, 128)               0       
   


- [VGG-16](https://github.com/onuralg/CNN-architectures/blob/master/cnn-architectures-vgg-16.ipynb)
- [VGG-19](https://github.com/onuralg/CNN-architectures/blob/master/cnn-architectures-vgg-19.ipynb)
- [ResNet50](https://github.com/onuralg/CNN-architectures/blob/master/cnn-architectures-resnet50.ipynb)
- InceptionV3
- InceptionResNetV2
