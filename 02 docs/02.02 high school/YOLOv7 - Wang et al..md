---
year: 10
course: sci-res
---
up:: [[School MOC]]
tags:: #compsci #compsci/machinelearning #toprocess 
dates:: 
people:: Chien-Yao Wang, Alexey Bochkovskiy, Hong-Yuan Mark Liao
URL:: [https://arxiv.org/pdf/2207.02696.pdf](https://arxiv.org/pdf/2207.02696.pdf)

# YOLOv7: Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors
## Goals
- Supporting mobile GPU and GPU devices from edge to cloud
- Optimize training process in addition to architecture (what most other models with the above goal are doing)
	- Try to strengthen training cost -- improve accuracy of object detection -- without increasing inference cost
- Propose solutions to issues with [[Model re-parameterization]] and dynamic label assignment

## Background
Characteristics of a state-of-the-art real-time object detector:
1. Faster and stronger network architecture
2. Effective feature integration method
3. Accurate detection method
4. Robust loss function
5. Efficient label assignment method
6. Efficient training network

YOLOv7 tries to come up with solutions to issues with current SOTA methods of 4, 5, and 6.

---

- Back Matter
	- published:: 2022-07-06
	- read:: 

---