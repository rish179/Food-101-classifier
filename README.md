# Food-101-classifier
Done on Google Collab using cuda GPU which is faster the CPU.

Resnet-50 classifier and mobilenetv2 classifier based on transfer learning  and pytorch.
Dataset used 101 food types as classes. 

Devided the dataset into train and test classes based on test files segregating the data into train and test.
![image](https://user-images.githubusercontent.com/53693971/119274717-e9164380-bc2e-11eb-804f-da9aec97bd20.png)

Data Augmentation based on pytorch Transformation to add rotation,flip and converrting dataset into tensors.

2 classifier models:

1. Mobilenetv2:
Model trained on preTrained parameters to save time. 

2. Resnet 50:
Based on Transfer Learning,pretrained model from PyTorch library.
created the last layer of 101 classes and added to the pretrained model. Ran the train function.



