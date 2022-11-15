---
year: 10
course: sci-res
---
up:: [[School MOC]]
tags:: #compsci #compsci/machinelearning 

# Research Plan
[[Elevator statement]]

## Rationale

1.3 million people annually die in road accidents and it is the leading cause of death in kids from 5-29 years old. The most common causes of these accidents are speeding, driving under influence and distracted driving, among others (WHO, 2018). The main motivation for manufacturing autonomous vehicles is a need for safer driving. Autonomous vehicles are those that have features allowing for movement from one point to another without any human intervention. Some features include sensing the environment, connecting to the internet, obeying traffic rules, self-navigation, making quick decisions, and ensuring safety of all road agents. The use of these features is able to reduce human error-caused road accidents, fuel consumption, and traffic (Parekh et al., 2022). 

In order to make quick decisions of the best route to take in places crowded with people, the autonomous vehicle makes use of pedestrian trajectory prediction to prevent collisions (Sighencea et al., 2021). Pedestrian trajectory prediction is the use of past motion of the pedestrian to predict future locations (Rasouli, Kotseruba et al., 2019). 

There has been much progress with the computational part of pedestrian trajectory prediction with the development of several state of the art models, such as Trajectron++ (Salzmann et al., 2021), BiTraP (Yao et al., 2020), and Social NCE (Liu et al., 2021), all perform markedly better than baseline models. Although these state of the art models have high performance on datasets as a whole, there is large disparity in performance between different age demographics. It is found for both BiTraP and Trajectron++ in unpublished work. 

In particular, both models performed worse on the senior demographic. This demographic is already more susceptible to collisions, with drivers over 70 years old having higher crash death rates per 1,000 crashes than middle-aged adults (35-54 years old) (CDC WISQARS, 2022). This increase in mortality rate has been discussed to partially be caused by changes in vision, physical ability, memory, and some diseases or medications that affect driving ability (Pomidor, 2019). Not only did the models perform worse on the senior demographic, but also the child demographic. Similarly to the seniors, children are vulnerable. 20% of children under the age of 15 killed in car crashes were pedestrians, compared to the 17% of people older than 15 (CDC WISQARS, 2022). Because these populations are more prone to collisions, it is even more crucial to ensure equal, if not better performance than on middle-aged adults.

Ensemble learning or ensemble model is the combination of multiple predictions from different models to make the final prediction. This optimization method has shown to be a good approach to increase a model's performance both experimentally and theoretically: A similar mechanism to Marquis de Condorcet theorem in political science is what leads to such improvements (Ganaie et al., 2022). Thus, it will be used to improve the performance on both demographics by combining an object detection model with a pedestrian trajectory prediction model.

In the machine learning community, it is generally accepted that the more data a model is trained on, the better it performs (Zhu et al., 2015). The main reason for this is the fact that a model aims to solve a problem by taking inputs and fine tuning a function that maps the input onto the output. So the more input/output pairs (data) a model is given, the more "fine-tuned" the function is! This idea will be implemented by training the ensemble model on multiple datasets amalgamated into one so it can better encapsulate the relationship between the input and outputs.

The aim of this study is focused on whether using such an ensemble model as described before will improve the model's performance on vulnerable demographics.


## Research question and hypothesis
> [!question]+
> Will using an object detection model [^1] with the pedestrian trajectory prediction model [^2] improve its performance on vulnerable demographics?

>[!note]+ Hypothesis
>Implementing an object detection model [^1] in conjunction with the pedestrian trajectory prediction model [^2] will significantly improve its performance on children and elderly in all metrics compared to baseline tests with just the pedestrian trajectory prediction model.

The baseline pedestrian trajectory prediction model Trajectron++ [^2] has been trained on two datasets -- nuScenes and ETH-UCY -- both of which have data predominantly concerning adults. It is well known in the field of machine learning that generally, the more data the model is given during training, the better it's able to predict during test time. To compensate for this lack of diversity in age ranges, an object detection model (YOLOv7 [^1]) is used to conditionally load the best parameters onto Trajectron++. Additionally, it will be trained with multiple sources of data, an aggregate of multiple datasets. Therefore, it is reasonable to conclude that the combination of these factors will aid in the model's performance and contribute to a significant increase.

## Procedure
### Dataset collection
#### Object detection
- PETA dataset
	1. Dataset will be downloaded from the website [^3]
	2. Python script will be written to select the attributes (personalLess15, personalLess30, personalLess45, personalLess60, personalLarger60) from each text file labels and the corresponding pedestrians
	3. Pedestrians will be reannotated
		- personalLess15 -> 'Child'
		- All pedestrians will be labeled with personalLess30, personalLess45, personalLess60 -> 'Adult'
		- personalLarger60 -> 'Senior'
- RAPv2 dataset
	1. The agreement form to download the dataset will be filled out [^4]
	2. The provided scripts in github repository [^5] will be used ('generate_selected_attribute_name.py', 'selected_attribute_idx.txt', and 'selected_attribute_name.txt')
		- To select the attributes and corresponding pedestrians(AgeLess16, Age17-30, Age31-45, Age46-60, AgeBiger60)
	3. Corresponding pedestrians labeled with the age groups will be reannotated
		- AgeLess16 -> 'Child'
		- All pedestrians labeled with Age17-30, Age31-45, Age46-60 -> 'Adult'
		- AgeBiger60 -> 'Senior'
- All pedestrian images will be combined into one dataset and all the annotations (only concerned with the age annotations) will be compiled

#### Pedestrian trajectory prediction
- JAAD dataset
	1. Dataset will be downloaded from the website [^6] 
	2. Python script will be written to divide the dataset into three fragments based on age
		- xml files with pedestrian ids will be used to extract both age attribute and pedestrian id onto a new file (one file per age group)
		- Should end up with three "mini-datasets" -- child, adult, senior
- PIE dataset
	1. Dataset will be downloaded from the website [^7]
	2. Python script will be written to perform the same tasks as on JAAD dataset (structure of the dataset is virtually the same)
- TITAN dataset
	1. Dataset will be acquired through Stonybrook professor, more details on the website [^8]
	2. Python script will be written to perform same tasks, may be different format TBD

### Model training
#### Object detection
- Combined dataset (of PETA and RAPv2) will be turned into a format suitable for YOLOv7
	1. Upload images and annotations to Roboflow [^9]
	2. Make any additional tweaks (TBD)
	3. "Download" in YOLOv7 Pytorch format by clicking the "show download code" button [^10]
	4. Copy download code and paste into a cell of a Jupyter Notebook to download and unzip dataset right into the working directory
- Environment will be set up
	1. Clone YOLOv7 repository [^11]
	2. Pip install requirements.txt
- YOLOv7 will be trained using the combined dataset
	1. Train on default setting: batch size TBD, epochs = 100 (to iterate quickly), weights are loaded from 'yolov7_training.pt' (also found in repository [^11])
	2. After first iteration adjust batch size, epoch numbers, learning rate, and other hyperparameters (also TBD)
		- Use Weights and Bases library [^12] to keep track of hyperparameters and model performance

#### Pedestrian trajectory prediction
- Each "mini" dataset for each dataset (PIE, TITAN, JAAD) will be turned into a format suitable for Trajectron++
	1. Use 'process_data.py' scripts for nuScenes and ETH-UCY (the datasets that Trajectron++ was originally trained on), found in the github repository [^13], to create a custom script for each dataset
	2. Combine datasets into 3 heterogenous ones for each demographic (i.e. one child dataset would contain data that was originally in PIE, TITAN, and JAAD) into a pkl file
- Environment will be set up (following instructions from github repository [^13])
	1. Create conda environment for dependencies
	2. Install conda environment as a kernel
- Trajectron++ will be trained on the pedestrian datasets
	1. Create a json file of the settings for training using 'config.json' and 'nuScenes.json' as a reference [^13]
	2. Keep all the parameters from batch size to maximum history length the same for the first iteration, but tweak the rest to fit the created datasets (exact method and values TBD)
	3. After first iteration adjust everything until reach the best parameters (again using Weights and Bases [^12]) 
- Parameters for each demographic will be saved into pkl files
	- Done automatically after each training iteration

#### Script to conditionally load parameters at test time (TBD) -- will need to finish training object detection model first.

### Model Evaluation
- A script will be written to connect all parts of the model ([[Ensemble methods]]) (will be added to)
	1. Load 'detect.py' script that is included in YOLOv7 [^11]
	2. Passes outputs to "conditional" script (mentioned just above)
	3. Conditional script should load the parameters on Trajectron++ and automatically run the 'evaluate.py' script [^13]
	4. 'evaluate.py' script generates csv files
- A Jupyter Notebook for analyzing results will be written using 'Results Analysis.ipynb' [^13] as a reference. All evaulation metrics are already found in the csv files; the jupyter notebook will make them more visually understandable.
	1. KDE NLL
	2. Most likely FDE
	3. Most likely ADE
	4. Best of 20 FDE
	5. Best of 20 ADE
	6. KDE NLL Velocity
	7. Most likely FDE Velocity
	8. Most likely ADE Velocity
	9. Best of 20 FDE Velocity
	10. Best of 20 ADE Velocity

### Evaluation of Significance
- ANOVA will be run on all metrics to see if there is significance
- If there is significance, T-test will be run to see which metrics are significant

[^1]: [[YOLOv7 - Wang et al.]]: [https://arxiv.org/pdf/2207.02696.pdf](https://arxiv.org/pdf/2207.02696.pdf)
[^2]: [https://arxiv.org/pdf/2001.03093.pdf](https://arxiv.org/pdf/2001.03093.pdf)
[^3]: [Pedestrian Attribute Recognition At Far Distance](http://mmlab.ie.cuhk.edu.hk/projects/PETA.html)
[^4]: [Download RAP Dataset](https://docs.google.com/forms/d/e/1FAIpQLSc-lcbWv_JFTeUYmqig15RQOXHdZlXWbXvi8OigDNWzkYB2xA/viewform)
[^5]: [RAP/person-attribute/static at master · dangweili/RAP · GitHub](https://github.com/dangweili/RAP/tree/master/person-attribute/static)
[^6]: [JAAD dataset](https://data.nvision2.eecs.yorku.ca/JAAD_dataset/)
[^7]: [PIE dataset](https://data.nvision2.eecs.yorku.ca/PIE_dataset/)
[^8]: [TITAN - Honda Research Institute USA](https://usa.honda-ri.com/titan)
[^9]: [https://proceedings.mlr.press/v164/lin22c/lin22c.pdf](https://proceedings.mlr.press/v164/lin22c/lin22c.pdf)
[^10]: [Exporting Data - Roboflow](https://docs.roboflow.com/exporting-data)
[^11]: [GitHub - WongKinYiu/yolov7: Implementation of paper - YOLOv7: Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors](https://github.com/WongKinYiu/yolov7)
[^12]: [Weights & Biases – Developer tools for ML](https://wandb.ai/site?utm_source=google&utm_medium=cpc&utm_campaign=Conversions%3A+Marketing+Site+-+Non-Branded+-+Dynamic+Search&utm_content=Baseline+-+1st+Ad&gclid=CjwKCAjwkaSaBhA4EiwALBgQaLtHYGxfKYPJbMrP9EozkurT5nRJ-HlC81ielROv4i1x-xmP1aPBKRoCsqQQAvD_BwE)
[^13]: [GitHub - StanfordASL/Trajectron-plus-plus: Code accompanying the ECCV 2020 paper "Trajectron++: Dynamically-Feasible Trajectory Forecasting With Heterogeneous Data" by Tim Salzmann*, Boris Ivanovic*, Punarjay Chakravarty, and Marco Pavone (* denotes equal contribution).](https://github.com/StanfordASL/Trajectron-plus-plus)
