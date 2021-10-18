# ML Model and Cost Function

## Model Representation

**Review:** 

Supervised Learning: Given the “right answer” for each example in the data. 

- Regression Problem: Predict real-valued output.

- Classification problem: Discrete-valued output.

**Notation(注释):**

> denote the number of traning examples. 

- m = Number of training examples
- x’s = “input” variable / features
- y’s = “output” variable / “target” variable
- (x,y) = one training example
- ($x^{(i)}$, $y^{(i)}$ = $i^{th}$ training example

Training Set -> Learning Algorithm -> h(hypothesis，假说) h just a shorthand.

![supervisied learning](https://cdn.jsdelivr.net/gh/edgarding77/images@latest/ML_learningNotes/model_notation.png)

This is a linear regression with one variable problem.

![img](https://cdn.jsdelivr.net/gh/edgarding77/images@latest/ML_learningNotes/oneVariable_linearRegression.png)

Our parameters which we choose decide our result, So it is a minimize problem.
$$
h_{\theta}(x)=\theta_{0}+\theta_{1} x
$$
「Why」我们可以通过点的分布（training examples）的进行一个绘制，它的分布类似一条直线；对于该问题（房屋价格预测），我们引入一个可能的表达式，因为只有一个feather/input，因此该问题称为单变量线性回归问题。

## Cost Function

![img](https://cdn.jsdelivr.net/gh/edgarding77/images@latest/ML_learningNotes/cost_function.png)

By using a **cost function**, we can measure the accuracy of our hypothesis function. This takes an average difference (actually a fancier version of an average) of all the results of the hypothesis with inputs from x's and the actual output y's. **Squared error function(平方误差函数):** $J\left(\theta_{0}, \theta_{1}\right)=\frac{1}{2 m} \sum_{i=1}^{m}\left(\hat{y}_{i}-y_{i}\right)^{2}=\frac{1}{2 m} \sum_{i=1}^{m}\left(h_{\theta}\left(x_{i}\right)-y_{i}\right)^{2}$** 

「Why」一种更高级版本的平均数，这需要*h*的所有结果与来自输入x's和实际的y's进行计算平均值。因此J函数代表的是Model与Training Set的偏差值，而*h*代表的是我们的模型。

#### Intuition I

We need to choose suitable parameters(theta0, theta1) with our model. Our decision will effect accuracy of our model to training set. The difference between the values predicted by our model and the actual values in training set is “**modeling error**”. (**建模误差**)

So our target is to choose suitable parameters so that we get a minimize modeling error.
$$
J\left(\theta_{0}, \theta_{1}\right)=\frac{1}{2 m} \sum_{i=1}^{m}\left(\hat{y}_{i}-y_{i}\right)^{2}=\frac{1}{2 m} \sum_{i=1}^{m}\left(h_{\theta}\left(x_{i}\right)-y_{i}\right)^{2}
$$
「Why」通过以上公式可以计算出我们选定的theta1 or theta0所带来模型的偏差值。

We can use our calculated results to plot and get the following, then this is reason why it is a minimize problem. Of course, it is come from one parameter theta1 function and theta0 we set theta0 = 0.

![img](https://cdn.jsdelivr.net/gh/edgarding77/images@latest/ML_learningNotes/function_parameter.png)

#### Intuition II

A contour plot is a graph that contains many contour lines. A contour line of a two variable function has a constant value at all points of the same line. An example of such a graph is the one to the right below. It means that taking any color and going along the 'circle', one would expect to get the same value of the cost function.

![img](https://cdn.jsdelivr.net/gh/edgarding77/images@latest/ML_learningNotes/function_twoparameter.png)

