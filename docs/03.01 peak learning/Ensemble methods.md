up:: 
tags:: #compsci #compsci/machinelearning #toprocess 

# Ensemble methods

This is a powerful technique used in machine learning to produce a powerful model by combining several "building-block" models.

It is popularly and most often used with Decision Tree models.

Instead of using just one Decision Tree and relying on it to make the right decision at every "split", ensemble methods take samples, calculate which features are most predictive, and aggregate into an effective predictor.

Types of methods:
1. **B**ootstrap **agg**regating (**Bagg**ing)
	- Pull multiple [[Bootstrap method|bootstrapped samples]] from the data and form a Decision Tree from each
	- Aggregate over the formed Decision Trees to form the best predictor

---
#### Sources
[Ensemble Methods in Machine Learning: What are They and Why Use Them? | by Evan Lutins | Towards Data Science](https://towardsdatascience.com/ensemble-methods-in-machine-learning-what-are-they-and-why-use-them-68ec3f9fef5f)