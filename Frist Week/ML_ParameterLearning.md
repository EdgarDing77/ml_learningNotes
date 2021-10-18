# ML Parameter Learning

## Gradient Descent

> Gradient Descent(梯度下降算法): estimate the parameters in the hypothesis function.

We use hypothesis function to predict X -> Y, And by using Cost Function we can get more exact parameters for our predictive model. So the problem become a minimize problem, but how can we find this minimium value with mutli-parameters hypothesis function. So That’s where gradient descent comes in.

![img](https://cdn.jsdelivr.net/gh/edgarding77/images@latest/ML_learningNotes/gradient_descent.png)

「Why」梯度下降算法的主要思想：

1. 初始化 $θ_0$ 和$θ_1$ , $θ_0$ = 0 , $θ_1$ = 0
2. 不断的改变 $θ_0$ 和 $θ_1$ 值，不断减少 F($θ_0$,$θ_1$)直至达到最小值（或者局部最小）。

想象成下山，如何下山最快？涉及到了下山的速度，即步长。若换旁边一个点，找到的最优解可能就是另一个，这也是梯度下降的一个特点，它会找到所有的局部解出来。而在该函数的图中，通过获取该点的**切线斜率**即该点的导数，我们走Cost Function在最陡的方向上，这一步的步长，用parameter α，叫learning rate。

The gradient descent algorithm is: $\theta_{j}:=\theta_{j}-\alpha \frac{\partial}{\partial \theta_{j}} J\left(\theta_{0}, \theta_{1}\right)$ (Simultaneously update j… ) j=0,1 represents the feature index number.
$$
\begin{aligned}
\text { temp } 0 &:=\theta_{0}-\alpha * \frac{\partial}{\partial \theta_{0}} \mathrm{~F}\left(\theta_{0}, \theta_{1}\right)=\theta_{0}-\alpha * \frac{1}{\mathrm{~m}} \sum_{\mathrm{i}=1}^{\mathrm{m}}\left(\mathrm{h}_{\theta}\left(\mathbf{x}^{(\mathrm{i})}\right)-\mathrm{y}^{(\mathrm{i})}\right) \\
\text { temp } 1 &:=\theta_{1}-\alpha * \frac{\partial}{\partial \theta_{1}} \mathrm{~F}\left(\theta_{0}, \theta_{1}\right)=\theta_{1}-\alpha * \frac{1}{\mathrm{~m}} \sum_{\mathrm{i}=1}^{\mathrm{m}}\left(\mathrm{h}_{\theta}\left(\mathrm{x}^{(i)}\right)-\mathrm{y}^{(\mathrm{i})}\right) * \mathrm{x}^{(\mathrm{i})} \\
\theta_{0} &:=\text { temp } 0 \\
\theta_{1} &:=\text { temp1 }
\end{aligned}
$$
On a side note, we should adjust our parameter \alpha*α* to ensure that the gradient descent algorithm converges in a reasonable time. 

* If å is too small, gradient descent can be slow. 
* If å is too larget, gradient descent can overshoot the minimum. it may fail to converge, or even diverge.

As we approach a local minimum, gradicent descent will automatically take smaller steps. So no need to decrease å over time.

具体梯度与导数的关系参考学习：https://halfrost.com/gradient_descent/，讲述十分清楚

**“Batch” Gradient Descent:** Each step of gradient descent users all the training examples.(Batch: 批次)

