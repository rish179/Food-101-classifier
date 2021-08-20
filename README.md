# Food-101-classifier
Done on Google Collab using cuda GPU which is faster the CPU.

Resnet-50 classifier and mobilenetv2 classifier based on transfer learning  and pytorch.
Dataset used 101 food types as classes. 

Devided the dataset into train and test classes based on test files segregating the data into train and test.
![image](https://user-images.githubusercontent.com/53693971/119274717-e9164380-bc2e-11eb-804f-da9aec97bd20.png)

Data Augmentation based on pytorch Transformation to add rotation,flip and converrting dataset into tensors.

##2 classifier models:

###1. Mobilenetv2:
Model trained on preTrained parameters to save time. 

###2. Resnet 50:
Based on Transfer Learning,pretrained model from PyTorch library.
created the last layer of 101 classes and added to the pretrained model. Ran the train function.

##Case study of models on FOOD101 Dataset.
###Data Augmentation Function:
We used the cv2 and numpy, first we divided the frame into 5 equal parts and used it as the width of the image. To maintain aspect ratio we took the present ratio of the image and took the ratio as a constant. Then we calculated the height of the resultant image maintaining the aspect ratio.
We then stacked the images in a single image using hstack function.

We saved the dataset into the drive and then used the command to load it into collab page. 

We used the function to divide dataset i to test and train folders. We used the text file containing the test/train images names to do that.

For data preprocessing we used PyTorch Transforms function. We rotated/flipped the images and then more importantly converted them into tensors to load them into the dataloader.
These dataloaders then can be loaded into model pipelines.

###Mobilenet_v2:
We created mobilenet_v2 model and used pretrained parameters to save time and increase accuracy . It would be  pretrained. 
 It provided accuracy of < 80%.
I also tried transfer learning using pretrained  model present in PyTorch library and changing last layer to our target of 101 classes. If ot worked ot will provide accuracy of 90% with atmax 50 epochs.
Resnet 50:
Just like the mobilenet_v2, we used the model from PyTorch library, and replaced the last layer with our 101 class layer.We created a function to train and print the loss and accuracy values.
We trained it with our dataloader. It provided maximum accuracy of 75-80% on 10 iteration which can go up on more iterations. It took 3-4 hours to train model.




