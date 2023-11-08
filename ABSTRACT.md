**Digital Breakthrough 2022: Ulyanovsk - Car Plate Detection** is a dataset for an object detection task. The dataset consists of 482 images with 482 labeled objects belonging to 1 single class (*plate*). Dataset from Digital breakthrough: season AI (Ulyanovsk region) competition.

## About Digital Breakthrough: Season AI (Ulyanovsk Region)

According to the press service of the Moscow Traffic Police, by the end of 2021, non-compliance with the distance between cars has become the most dangerous violation. It is because of non-compliance with the safe distance to the car in front that people most often die and get into accidents on the roads.

Maintaining a safe distance from the vehicle in front is one of the important criteria for road safety. In real-time, such a parameter cannot be monitored with the help of surveillance cameras, and it is also impossible to estimate what distance the driver observes while driving around the city. To control safe driving, a solution is needed that will be able to track the distance between cars in real-time. This will reduce the number of accidents and save the lives of drivers and passengers.

The participants of the championship are faced with the task of developing an algorithm that allows determining the distance to the car in front in real-time, using a dataset of photos of cars from different distances. Subsequently, this algorithm can be used in navigation systems to warn of a dangerous approach and to monitor compliance with the distance.

## Author's solution

The author's solution is based on two datasets:

- Digital Breakthrough 2022: Ulyanovsk - Car Plate Detection (current)
- Digital Breakthrough 2022: Ulyanovsk - Car Object Detection [(available on DatasetNinja)](https://datasetninja.com/digital-breakthrough-2022-ulyanovsk-car-object)

The baseline provided by the organizers of the championship was taken as the basis of the solution, which was improved, namely, in addition to detecting the car, the number, and the car-mating badge were also detected, which gave a greater increase in speed. Additional models were retrained on the competition data train (manual marking using an online service [makesense.ai](https://www.makesense.ai/) ) using the [YOLOv5](https://github.com/ultralytics/yolov5) (YOLOv5m6) model. CatBoostRegressor with improved parameters was used to predict the distance.

<img src="https://github.com/dataset-ninja/digital-breakthrough-2022-ulyanovsk-car-object/assets/123257559/28e8618f-f690-40f7-b79e-b145ed707350" alt="image" width="800">
