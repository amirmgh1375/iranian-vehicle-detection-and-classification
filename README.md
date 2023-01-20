# iranian-vehicle-detection-and-classification
detect and classify iranian vehicle make and model based on deep cnn neural networks with keras framework

## Abstract

Due to the rapid growth of vehicles, traffic monitoring and tracking systems in the last decade, vehicle detection and extracting information such as vehicle type and model and car plate recognition are the important issues of the day and many efforts have been made using different methods to identify vehicles. Given the high number of vehicles and similarities of classes, it is a difficult task to find an accurate and rapid approach to differentiate available classes and classify them. In this article we propose a new approach which simultaneously detects vehicles and identifies their type. Two models are trained in this paper. The first model is based on CNN networks to extract features and detect vehicle models, and the second model which is the main contribution of this article is based on YOLO (You Only Look Once) algorithm and SSD to detect vehicle location in the image. To train and test this approach, we collect 150,000 images of 115 domestic and foreign vehicle classes from Iranian websites. Hence, the images have large variations in image size, illumination and pose. The experimental results on the accrued dataset shows that the proposed method is able to correctly classify 91% of the vehicles in uncontrolled conditions.

## How to run the model

First download the pretrained cnn model from this link address

https://drive.google.com/open?id=13x7I9UyVLSReSJAmoroRNjqEUyyYxNvz


Then run the `test_predict.py` notebooke and get the results.


---
Complete codes and documentations will comming soon : )
