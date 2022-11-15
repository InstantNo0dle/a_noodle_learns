---
year: 10
course: sci-res
---
up:: [[Research Plan]]
tags:: #compsci #compsci/machinelearning 

# Elevator statement

When you ask someone what the advantages of self-driving cars are, they will probably say something about them being safer. That sentiment could potentially become reality, if the car can accurately predict where traffic agents are. That’s exactly what trajectory prediction is -- prediction of the coordinates of pedestrians, cars, trucks, etc. at a point in the future. Currently, the best models perform worse on older and younger pedestrians, who are more prone to accidents than adults; adults over 65 accounted for 20% of all pedestrian deaths and 20% of children under the age of 15 killed in crashes were pedestrians. Since those two demographics are already much more vulnerable, it is imperative that a fair model must be designed. This will be done in two parts. The first part will be an object detection model that will detect the demographic of the pedestrian, label them, and draw a “bounding box” around them. The second part is the pedestrian trajectory prediction model which will be trained on each demographic separately to obtain the best performing “version” of the model for each -- there will be three “versions” that will be saved into a file. At test time, based on the demographic detected, a version of the pedestrian trajectory prediction model will be loaded. This way, it accounts for the nuances associated with each demographic (i.e. elderly tend to walk slower).