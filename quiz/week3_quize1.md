# Week 2 | IV. Linear Regression with Multiple Variables

## Question 1



Suppose that you have trained a logistic regression classifier, 
and it outputs on a new example x a prediction hθ(x) = 0.4. This means (check all that apply):
### Answer

* **Our estimate for P(y=1|x;θ) is 0.4.**

* Our estimate for P(y=0|x;θ) is 0.4.

* Our estimate for P(y=1|x;θ) is 0.6.

* **Our estimate for P(y=0|x;θ) is 0.6.**

	
---

## Question 2


Suppose you have the following training set, and fit a logistic regression classifier hθ(x)=g(θ0+θ1x1+θ2x2).

![](https://d3c33hcgiwev3.cloudfront.net/vDH1Eb5xEeSVRiIAC2sM-Q_Screen-Shot-2015-02-27-at-3.09.52-AM.png?Expires=1500508800&Signature=WLRnJn0pRzBNRf2X5BeZXn3b1U8dAzehdQ8XWmBK-elkwPME-yluKCD1WSMIENT7R1VP4TXtveFzi~GUH6396XxfrKCH0hQ6afqh5DBzeT~AzBNn6ZKAqcvVMYFo~fpZzulO8EI315fSsnqhyh8t7ZGBR61bJ~ho97S4yEpjRMI_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
![](https://d3c33hcgiwev3.cloudfront.net/x6wwkr5xEeSVRiIAC2sM-Q_Screen-Shot-2015-02-27-at-3.10.20-AM.png?Expires=1500508800&Signature=cBqI61e3AUH3Bwp0DNX5vNnjd6Krt-q2kGo-RVDO-MwImfBUWsxTtum-UtO7sP2r-j1Ekob4PVWD5ma02GrhrzYdpBIee~iKeGaHkHwVmWRMljem89h8uwUNUTIwMu1sw3RPxjNpZhdcg7~3DolQELqguomobaTXNsaJQBSPMus_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

Which of the following are true? Check all that apply.


### Answer


Adding polynomial features (e.g., instead using hθ(x)=g(θ0+θ1x1+θ2x2+θ3x21+θ4x1x2+θ5x22) ) could increase how well we can fit the training data.

At the optimal value of θ (e.g., found by fminunc), we will have J(θ)≥0.

*Adding polynomial features (e.g., instead using hθ(x)=g(θ0+θ1x1+θ2x2+θ3x21+θ4x1x2+θ5x22) ) would increase J(θ) because we are now summing over more terms.
	

* If we train gradient descent for enough iterations, for some examples x(i) in the training set it is possible to obtain hθ(x(i))>1.


--- 

## Question 3

For logistic regression, the gradient is given by ∂∂θjJ(θ)=1m∑mi=1(hθ(x(i))−y(i))x(i)j. Which of these is a correct gradient descent update for logistic regression with a learning rate of α? Check all that apply.

### Answer

* θ:=θ−α1m∑mi=1(11+e−θTx(i)−y(i))x(i).

θj:=θj−α1m∑mi=1(θTx−y(i))x(i)j (simultaneously update for all j).

θ:=θ−α1m∑mi=1(θTx−y(i))x(i).

θ:=θ−α1m∑mi=1(hθ(x(i))−y(i))x(i).

---

## Question 4

Which of the following statements are true? Check all that apply.

### Answer

Since we train one classifier when there are two classes, we train two classifiers when there are three classes (and we do one-vs-all classification).

The cost function J(θ) for logistic regression trained with m≥1 examples is always greater than or equal to zero.

* The one-vs-all technique allows you to use logistic regression for problems in which each y(i) comes from a fixed, discrete set of values.

* For logistic regression, sometimes gradient descent will converge to a local minimum (and fail to find the global minimum). This is the reason we prefer more advanced optimization algorithms such as fminunc (conjugate gradient/BFGS/L-BFGS/etc).


---

## Question 5

Suppose you train a logistic classifier hθ(x)=g(θ0+θ1x1+θ2x2). Suppose θ0=6,θ1=0,θ2=−1. Which of the following figures represents the decision boundary found by your classifier?

### Answer



