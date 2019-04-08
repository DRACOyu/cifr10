
# Paper keypoints
1. the effect of the convolutional network **depth** on its accuracy in the large-scale image recognition setting
  
2. using an architecture with very small (3 X 3) convolution filters, with stride 1
  
3. max-pooling is performed over a 2 × 2 pixel window, with stride 2
  
4. conv + 3 fully-connected layers (number of FC neurons: 4096 > 4096 > n_classes)
  
5. learning rate decay, parameter initializaiton from pre-trained models, etc.
training：
1. load pre-trained parameters (trained on ImageNet dataset, 1000 classes), you can download the parameter file (vgg16.npy, about 500M) here:
https://mega.nz/#!YU1FWJrA!O1ywiCS2IiOlUCtCpI6HTJOMrneN-Qdv3ywQP5poecM
2. For Chinese users, I put the pre-trained parameter file (about 500M) on baidu: https://pan.baidu.com/s/1pLGzull
2. Remove the final layer, add one layer with 10 nodes to test the CIFAR10 dataset(binary version).
https://www.cs.toronto.edu/~kriz/cifar.html
3. It took me around one hour to train with 15000 training steps and learning rate is 0.01. The testing accuracy on the CIFAR10 test dataset is about 85.69%.

