# Torchvision Experiments
In this repository, I have actually experimented with different transformations and experimented them on CIFAR10 dataset using torchvision library. 
## Image Transformations
I have tried Image transformations on CIFAR10 as well as 3 images taken from the internet. I tried the following transformations:

1. A RandomHorizontalFlip
2. A RandomRotation
3. ColorJitter (tested different brightness, contrast, saturation and hue)
4. Grayscale

You can view the Notebook [here](https://github.com/ayushanand18/torchvision-experiments/blob/main/Image_Transformations.ipynb)

## CIFAR10 Experiments
Using the knowledge from above experiment about Image transformations, I did another experiment with the CIFAR10 dataset.
You can find the Notebook [here](https://github.com/ayushanand18/torchvision-experiments/blob/main/CIFAR10_Experiment_1_ResNet50.ipynb)

### Data transformations
We will try different image transformations with our data and prepare a detailed table of comparison on accuracy, speed, and efficiency with each set of transformations.
1. **ColorJitter**: We will vary the brightness, contrast, hue and saturation of an image and see which looks best.
2. **Rotation**: We will try to rotate the images randomly, and look at the model accuracy in test cases.
3. **Grayscale**: We will also try to randomly grayscale some of our data and see if our model can distinguish easily.\
We will try to experiment with 5 set of image transformations, (No Transformation, ColorJitter, Rotation,Rotation+Grayscale, and Rotation+ColorJitter).
### Model Architectures
We will also experiment with different model architectures. (All we will use are pre-trained).
1. Our all-favourite **ResNet50**.
3. Another **ResNet34**.
4. **ResNeXt50**: Born out of Facebook AI and UC Diego.

#### Hyper Parameters.
1. **Batchsize**: 64/128
2. **CyclicLR**
3. **Optimizer**: Ranger

### Conclusion
The Results table.

|Architecture (batch size) |No Transformation|ColorJitter|Rotation|Rot.+Color.|Rot.+Grayscale|
|-------------|-----------------|-----------|--------|-----------|--------------|
|ResNet50 (128)|99.282%|72.542%|-|-|-|
|ResNeXt50 (128)|98.942%|-|-|-|-|
`Rot. = Rotation`
`Color. = ColorJitter`

1. **Ranger** Optimizer just worked wonders and whithin 5 epochs got a 99%+ accuracy on ResNet50.
2. **ResNet50** scores slightly better than **ResNeXt50** on our dataset (in 5 epochs) but ResNeXt50 takes considerably more time for training than the former.

  |Model    |Training Time| Utilized time %|
  |---------|-------------|----------------|
  |ResNet50 |  18m 34s     |  70.64%       |
  |ResNeXt50|  26m 17s     |  100%         |
  
  ResNet50 performs slightly better while taking 30% lesser time than ResNeXt50.

  Therefore, it will be better for us to use **ResNet50** over **ResNeXt50** because of time constrains.

**Thank you so much for your time looking at my repository!**