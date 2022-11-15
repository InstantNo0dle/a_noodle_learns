---
year: 10
course: sci-res
alias: [PETA dataset]
---
date: 2022-11-08
tags: #compsci/machinelearning 
# pedestrian attribute recognition at far distance
## intro
Attribute recognition previously done far away with the full body because close-ups aren't available from surveillance in the real world.
- Two challenges associated:
	1. **Appearance diversity**: a lot of variation even in the same attribute
		- Thus needs large and diverse training set
	2. **Appearance ambiguity**: task is made very difficult because of the poor quality

Goals/contributions:
- Existing datasets aren't diverse enough, PETA dataset aims to fix this.
- New approach for attribute recognition to mitigate ambiguity in features
	- Use neighboring images (appearances are similar) during **inference** to help
		- Treat as form of **regularization** or context
		- Form a [[markov random field]] (MRF) graph (first paper to propose this!)
			- Associations between nodes weighted by *similarity*
			- Infer on the graph to estimate attribute probability for all images

## pedstrian attribute dataset
The dataset was made from combining 10 smaller scale public datasets.
- Varying in camera angles, view point, illumination, resolution, and indoor/outdoor to provide the needed diversity

Processing:
1. Removed duplicate and erroneous images
2. Relabeled images with 61 binary and 4 multi-class attributes

The dataset can be used for research on pedestrian tracking, detection, etc. and integrated with other sources.

## baseline methods
1. **SVM with intersection kernel** (ikSVM) based on a previous study which applied it successfully.
2. **Markov Random Field** to use context of neighbors
	- Essentially makes sure to penalize for assigning different states to the similar nodes (like saying that two instances of an attribute are two *different* attributes)
		- **ikSVM** learns the probability of predicting the attribute value of the image (the unary cost)
		- **Random forest** learns the **gaussian kernel** (pairwise cost)
	- Limit number of neighbors by building a k-NN sparse graph (k=5)

## experiment
They separated the dataset into training (9,500), verification (1,900), testing (7,600).
- 35 attributes selected with 15 categorized as "important" by experts and 20 that were difficult

For attributes with *imbalanced* positive and negative samples, SVM was trained by making the positive samples the *same size* as negative samples, to avoid bias.

Markov Random Field graphs were built in two ways:
1. With only testing images
2. With both training and testing images

Color and texture features were used in the representation of the image (inside the model):
- RGB, HSV, YCbCr and other color channels
- Gabor and Schmid filters on luminance aquired 21 texture channels
- Divided image into six strips and extracted features

Results:
Markov random field graphs performed better than SVM on most of the attributes -- graph regularization does help!
- Using both training and testing images increases performance of the MRF graphs.
- Random forest performs much better than gaussian kernel generally

All methods had poor performance on attributes with imbalanced distribution.

## conclusions
Future work:
- Evaluate existing algorithms in attribute classification by using PETA as a benchmark

---
### Sources
[Pedestrian Attribute Recognition At Far Distance (cuhk.edu.hk)](http://mmlab.ie.cuhk.edu.hk/projects/PETA.html)
