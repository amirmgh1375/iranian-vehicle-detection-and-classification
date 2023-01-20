
# Simultaneous Vehicle Detection and Classification Model based on Deep YOLO Networks
Detect and classify iranian vehicle make and model based on deep cnn neural networks with keras framework.
Implementation and review of the article [IEEE](https://ieeexplore.ieee.org/abstract/document/9116922)

## Abstract

Due to the rapid growth of vehicles, traffic monitoring and tracking systems in the last decade, vehicle detection and extracting information such as vehicle type and model and car plate recognition are the important issues of the day and many efforts have been made using different methods to identify vehicles. Given the high number of vehicles and similarities of classes, it is a difficult task to find an accurate and rapid approach to differentiate available classes and classify them. In this article we propose a new approach which simultaneously detects vehicles and identifies their type. Two models are trained in this paper. The first model is based on CNN networks to extract features and detect vehicle models, and the second model which is the main contribution of this article is based on YOLO (You Only Look Once) algorithm and SSD to detect vehicle location in the image. To train and test this approach, we collect 150,000 images of 115 domestic and foreign vehicle classes from Iranian websites. Hence, the images have large variations in image size, illumination and pose. The experimental results on the accrued dataset shows that the proposed method is able to correctly classify 91% of the vehicles in uncontrolled conditions.

## PROPOSED METHOD
There are various methods to extract   and classify the features available in a vehicle image. In this   study, two different scenarios were employed to classify and identify vehicle type and its location in the image. The first scenario involves combining an SSD object detection network in the image to determine the vehicle location and a ResNet  convolutional class network to identify vehicle type. In the second scenario, which is the approach proposed in this paper,  the YOLO algorithm is used to train an end-to-end network for the seamless and direct detection of all vehicles in the image.

<!-- ![paper_res44](https://user-images.githubusercontent.com/25933029/213679776-bf561610-5a45-4a99-886e-139233bc3d19.png) -->
<img src="https://user-images.githubusercontent.com/25933029/213679776-bf561610-5a45-4a99-886e-139233bc3d19.png" width="500" height="350">

## Data Collection and dataset creation
To collect data and create this dataset of common vehicles in Iran, a script was implemented which surveyed car dealing websites  and  extracted  and  saved  images  of  vehicles  in available categories. Then, by examining the number of images of cars in each class, categories with over 400 images were selected for testing. A total of 95 vehicle classes were prepared to conduct the experiment. Images removed from other classes are included in class 115, which has been considered for making models other than the models in the main classes.  

| Row | Vehicle | Model | Number |
|--|--|--|--|
|1 | Saipa | Pride | 14833 |
|2 | IranKhodro| Peykan| 7442|
|3 | Peugeot| Pride | 7367|
|... | ...| ... | ...|

Ultimately, a dataset containing 148414 images of various classes was prepared. Table I displays 3 vehicles in the database by brand, model and number.

To download the dataset, please send your request to my email amirmg.1375@gmail.com.

## RESULTS
In experiment 1, a 91.0% accuracy was obtained  with the dataset introduced at the beginning of this section including 96 classes of common vehicles in Iran. A 91.2%  
accuracy was obtained in experiment 2. As we observe, the second method is more accurate than the first one which represents that pre-processing and cutting images had a positive effect on accuracy improvement. Table II show some of the true and false results obtained from experiments 1 and 2.  The accuracy value reported in the second scenario in Table II is based on the value of the detected confidence for each class and applying the specified threshold on the values.

|               | Scenario 1    |  Scenario 1   | Scenario 2  |
|----------------|---------------|---------------|-------------|
|              | Experiment 1  | Experiment 2  |Experiment 1 |
| Accuracy       | 89            | 90.5          | 75.03       |
| Mean time  (second)    | 1.378         | 1.378         | 0.08        |
| Input image size | 324×324       | 424×424       | 416×416     |
| mAP            | -             | -             | 0.73        |
| IoU threshold  | -             | -             | 0.66        |
| Precision      | 0.9           | 0.91          | 0.72        |
| Recall         | 0.9           | 0.88          | 0.73        |
| F1-score       | 0.9           | 0.89          | 0.72        |


<!-- ![paper_res](https://user-images.githubusercontent.com/25933029/213677822-2c61a52a-e7e7-4267-911b-6716770a1256.png) -->
<img src="https://user-images.githubusercontent.com/25933029/213677822-2c61a52a-e7e7-4267-911b-6716770a1256.png" width="500" height="350">

<!-- ![paper_res_tables](https://user-images.githubusercontent.com/25933029/213677873-21474ac5-65dd-4596-8675-1ff2d5c2f7f0.png) -->
<img src="https://user-images.githubusercontent.com/25933029/213677873-21474ac5-65dd-4596-8675-1ff2d5c2f7f0.png" width="500" height="200">

## How to run the model

First download the pretrained cnn model from this link address

https://drive.google.com/open?id=13x7I9UyVLSReSJAmoroRNjqEUyyYxNvz


Then run the `test_predict.py` notebooke and get the results.

## Citation
```
@INPROCEEDINGS{9116922,
  author={Ghoreyshi, Amir Mohammad and AkhavanPour, Alireza and Bossaghzadeh, Alireza},
  booktitle={2020 International Conference on Machine Vision and Image Processing (MVIP)}, 
  title={Simultaneous Vehicle Detection and Classification Model based on Deep YOLO Networks}, 
  year={2020},
  volume={},
  number={},
  pages={1-6},
  doi={10.1109/MVIP49855.2020.9116922}}
```


---
Complete codes and documentations will comming soon : )
