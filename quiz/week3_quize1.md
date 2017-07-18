# Week 2 | IV. Linear Regression with Multiple Variables

## Question 1



Suppose that you have trained a logistic regression classifier, 
and it outputs on a new example x a prediction hθ(x) = 0.4. This means (check all that apply):
### Answer

* Our estimate for P(y=1|x;θ) is 0.4.

* Our estimate for P(y=0|x;θ) is 0.4.

* Our estimate for P(y=1|x;θ) is 0.6.

* Our estimate for P(y=0|x;θ) is 0.6.

	
---

## Question 2


Suppose you have the following training set, and fit a logistic regression classifier hθ(x)=g(θ0+θ1x1+θ2x2).

https://d3c33hcgiwev3.cloudfront.net/vDH1Eb5xEeSVRiIAC2sM-Q_Screen-Shot-2015-02-27-at-3.09.52-AM.png?Expires=1500508800&Signature=WLRnJn0pRzBNRf2X5BeZXn3b1U8dAzehdQ8XWmBK-elkwPME-yluKCD1WSMIENT7R1VP4TXtveFzi~GUH6396XxfrKCH0hQ6afqh5DBzeT~AzBNn6ZKAqcvVMYFo~fpZzulO8EI315fSsnqhyh8t7ZGBR61bJ~ho97S4yEpjRMI_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A

### Answer

* **Rather than use the current value of α, it'd be more promising to try a larger value of α (say α=1.0).**
	* A larger value for α should increase the rate of convergence to the minimum of J(θ).
* Rather than use the current value of α, it'd be more promising to try a smaller value of α (say α=0.1).
* α=0.3 is an effective choice of learning rate.


--- 

## Question 3

Suppose you have m=14 training examples with n=3 features (excluding the additional all-ones feature for the intercept term, which you should add). The normal equation is θ=(X<sup>T</sup>X)<sup>−1</sup> X<sup>T</sup>y. For the given values of m and n, what are the dimensions of θ, X, and y in this equation?

### Answer

Add feature to X => 14x4 matrix
y = 1 col, m rows => 14X1 ( 1 result per example)
θ = 4 cols, 1 row => 1x4 ( 1 value per feature)

(m x n) * (n * m)

* **X is 14×4, y is 14×1, θ is 4×1**
* X is 14×4, y is 14×4, θ is 4×4
* X is 14×3, y is 14×1, θ is 3×3
* X is 14×3, y is 14×1, θ is 3×1

---

## Question 4
Suppose you have a dataset with m=1000000 examples and n=200000 features for each example. You want to use multivariate linear regression to fit the parameters θ to our data. Should you prefer gradient descent or the normal equation?

### Answer

* The normal equation, since it provides an efficient way to directly find the solution.
* Gradient descent, since it will always converge to the optimal θ.
* **Gradient descent, since (X<sup>T</sup>X)^−1 will be very slow to compute in the normal equation.**
	* With n=200000 features, you will have to invert a 200001×200001 matrix to compute the normal equation. Inverting such a large matrix is computationally expensive, so gradient descent is a good choice.	
* The normal equation, since gradient descent might be unable to find the optimal θ.


---

## Question 5
Which of the following are reasons for using feature scaling?

### Answer


* **It speeds up gradient descent by making it require fewer iterations to get to a good solution.**
	* Feature scaling speeds up gradient descent by avoiding many extra iterations that are required when one or more features take on much larger values than the rest.
* It is necessary to prevent gradient descent from getting stuck in local optima.
	* The cost function J(θ) for linear regression has no local optima. 
* It speeds up gradient descent by making each iteration of gradient descent less expensive to compute.
	* The magnitude of the feature values are insignificant in terms of computational cost.
* It prevents the matrix X<sup>T</sup>X (used in the normal equation) from being non-invertable (singular/degenerate).
	* X<sup>T</sup>X can be singular when features are redundant or there are too few examples. Feature scaling does not solve these problems.
