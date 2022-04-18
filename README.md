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

