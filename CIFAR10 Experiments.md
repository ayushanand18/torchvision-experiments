# CIFAR10 Experiments
Experiment we will be going to do with the CIFAR10 dataset.
## Data transformations
We will try different image transformations with our data and prepare a detailed table of comparison on accuracy, speed, and efficiency with each set of transformations.
1. **ColorJitter**: We will vary the brightness, contrast, hue and saturation of an image and see which looks best.
2. **Rotation**: We will try to rotate the images randomly, and look at the model accuracy in test cases.
3. **Grayscale**: We will also try to randomly grayscale some of our data and see if our model can distinguish easily.\
We will try to experiment with 5 set of image transformations, (No Transformation, ColorJitter, Rotation,Rotation+Grayscale, and Rotation+ColorJitter).
## Model Architectures
We will also experiment with different model architectures. (All we will use are pre-trained).
1. Our all-favourite **ResNet50**.
3. Another **ResNet34**.
4. **ResNeXt50**: Born out of Facebook AI and UC Diego.

### Hyper Parameters.
1. **Batchsize**: 64/128
2. **CyclicLR**
3. **Optimizer**: Ranger v/s Adam

## Conclusion
The Results table.
|Architecture |No Transformation|ColorJitter|Rotation|Rot.+Color.|Rot.+Grayscale|
|-------------|-----------------|-----------|--------|-----------|--------------|
|ResNet34 (64)|                 |           |        |           |              |
|ResNet34 (128)||||||
|ResNet50 (128)|99.282%|||||
|ResNeXt50 (128)||||||
|ResNeXt50 (64)||||||
