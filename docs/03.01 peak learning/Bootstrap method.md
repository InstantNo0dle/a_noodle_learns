up:: 
tags:: #compsci #compsci/machinelearning 

# Bootstrap method

Bootstrap is a **resampling method** that tries to make a prediction about an estimate for a population parameter $\theta$ on sample data without making too many assumptions.

> [!Tldr]+
> It takes an original sample and independently samples, *with replacement*, the same sample size $n$, and then uses resampled data to perform an inference on the **population** level. The bootstrap method attempts to use the sample data to generalize to the population.
> ![[Pasted image 20221013090111.png]]

Obviously, resampling *with replacement* is an important aspect. Otherwise, you're just resampling the original sample and end up the same sample for all.

## Steps
1. Get an original sample from the population with size $n$
2. Resample from the original sample with replacement, size $n$. These resamples are called **bootstrap samples** (B in total)
3. Form an [[Empirical distribution function]] from the resamples
4. Calculate the statistic of the population parameter $\theta$ for each bootstrap sample -> B statistics in total
	- Turn the parameters of interest into a **function** of the distribution function $\theta = g(\hat F)$
	- Plug in the EDF into the function above. EDF is an estimate of the population CDF, so it allows for evaluation of the population parameter.
		- ![[Pasted image 20221014091633.png]]
5. Calculate the variance for the B statistics to approximate the true variance

 ![[Pasted image 20221014092437.png]]
 
## Why use bootstrap?
When you sample from the population and generate statistics about that data (mean, median, etc.), those statistics (aka **point estimate**) are virtually never equal to population parameters because of **sampling variability**. It will always have some sort of **standard error**.  

Usually, you'd assume that the population has a certain distribution (say roughly normal) and make inferences using your point estimates and standard error that way.
- In normal distributions, the sampled mean $\mu$ lies within 2 standard errors of population mean $\bar X$ 

However, reality slaps you in the face ✋ and two issues arise:
1. You don't know *for sure* the distribution about the population (sometimes you barely know any information at all!)
2. There may not be a formula for the standard error of the statistic you're measuring (like median)

In those scenarios, the bootstrap method is extremely powerful.

## Why does this work?
By the **Law of Large Numbers**, as the number of bootstrapped samples approaches infinity, the mean of the statistic on those B samples converges to the **true mean**.

Similarly, the sample variance does the same thing.

![[Pasted image 20221014084935.png]]

---
#### Sources
[An Introduction to the Bootstrap Method | by Lorna Yen | Towards Data Science](https://towardsdatascience.com/an-introduction-to-the-bootstrap-method-58bcb51b4d60)