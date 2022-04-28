# Fashion-MNIST-PyTorch
Pytorch implementation of Gray Image Classification 


## Dataset:
[Fashion MNIST](https://www.kaggle.com/datasets/zalando-research/fashionmnist)
is a set of 28x28 grayscale images of clothes.  
A dataset which contains 70,000 grayscale images in 10 categories  
![Data](./images/fashion-mnist.png)  
**Clasess:**    
- T-shirt/top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle boot  

Set | #Train | #Validation | #Test |
--- | --- | --- | --- |
#images | 48K | 12K | 10K |  

**Installations**  
```pip install torch, torchvision, tensorflow, sklearn```  
## 3 Layer simple DNN Results:
![DNN_RES](./images/DNN.jpg) ![DNN_CM](./images/DNN_cm.jpg)  

## 2 Layer CNN + BN + MaxPool + L2 Regularization + 30% Drop-out Results:
![CNN_RES](./images/cnn_res.jpg) ![CNN_CM](./images/cnn_cm.jpg)   
**TSNE on Train and Test (128 Latent feature vectors)**  
![CNN_tsne_train](./images/cnn_tsne_train.jpg) ![CNN_cnn_tsne_test](./images/cnn_tsne_test.jpg)  
## Data Manipulation (Merge Classes):
Class 0 - Top: T-Shirt/Top (0), Pullover (2), Dress (3), Coat (4), Shirt (6)  
Class 1 - Bottom: Trouser (1), Sandal (5), Sneaker (7), Ankle Boot (9)  
Class 2 - Accessories: Bag (8)  
![3class_RES](./images/3class_res.png) ![3class_CM](./images/3class_cm.png)   
**TSNE on Test (128 Latent feature vectors)**  
![3class_tsne_test](./images/3class_tsne_test.png)   
## Data Augmentation:  
**'noise', 'RandomRotation', 'RandomHorizontalFlip', 'brightness', 'contrast', 'RandomResizedCrop'**  
**'Noise'**
```transforms.Compose([transforms.ToTensor(), AddGaussianNoise(0.1, 0.08)])```  
![noiseAug](./images/noise.png)  
**'RandomRotation', 5%**  
```transforms.Compose([transforms.ToTensor(), transforms.RandomRotation(degrees=5)])```  
![RandomRotationAug](./images/random_rotation.png)  
**'RandomHorizontalFlip', 90% probability**  
```transforms.Compose([transforms.ToTensor(), transforms.RandomHorizontalFlip(p=0.9)])```
![RandomHorizontalFlip](./images/Random_horizontal_flip.png)  
**'brightness', 50%**  
```transforms.Compose([transforms.ToTensor(), transforms.ColorJitter(brightness=0.5)])```  
![Brightness](./images/brightness.png)  
**'contrast', 50%**  
```transforms.Compose([transforms.ToTensor(), transforms.ColorJitter(contrast=0.5)])```  
![Contrast](./images/contrast.png)   
**'RandomResizedCrop', original size=28X28 pixels**  
```transforms.Compose([transforms.ToTensor(), transforms.RandomResizedCrop(size=(28, 28))])```  
![RandomResizedCrop](./images/random_resized_crop.png)   

