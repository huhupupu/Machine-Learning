# Classification, Logistic Regression, and Regularization
## Logistic Regression Model
Threshold classifier output $h_\theta(x)$ at 0.5:
$h_\theta(x)$ = $g(\theta^Tx)$ = $\frac{\mathrm{1} }{\mathrm{1} + e^- \theta^Tx }$
 * If h$_\theta$(x) $\geq$ 0.5, predict "y=1";
  $\theta^Tx$ $\geq$ 0
 * If h$_\theta$(x) $\leq$ 0.5, predict "y=0";
  $\theta^Tx$ $\leq$ 0

Python code:
```python
import numpy as np

def sigmoid(z): 
    
    return 1 / (1 + np.exp(-z))
```
## Decision Boundary(判定边界)
${h_\theta}\left(x\right) = g\left({\theta_0}+{\theta_1}{x_1}+{\theta_2}{x_2}\right)$

并且参数$\theta$ 是向量[-3 1 1]。 则当$-3+{x_1}+{x_2} \geq 0$，即${x_1}+{x_2} \geq 3$时，模型将预测 $y=1$。 我们可以绘制直线${x_1}+{x_2} = 3$，这条线便是我们模型的分界线，将预测为1的区域和预测为 0的区域分隔开。

##Non-linear Decision Boundary
${h_\theta}\left( x \right)=g\left( {\theta_0}+{\theta_1}{x_1}+{\theta_{2}}{x_{2}}+{\theta_{3}}x_{1}^{2}+{\theta_{4}}x_{2}^{2} \right)$
If $\theta$ equals [-1 0 0 1 1] 
predict "y=1" if -1+${x_1^2}$+${x_2^2}$ $\geq$ 0
${x_1^2}$+${x_2^2}$ $\geq$ 1
*Decision is the property of hypothesis, not the dataset*

##Cost Function
How to choose $\theta$
$J\left( \theta \right)=\frac{1}{m}\sum\limits_{i=1}^{m}{{Cost}\left( {h_\theta}\left( {x}^{\left( i \right)} \right),{y}^{\left( i \right)} \right)}$

# Newton’s method(牛顿法)
