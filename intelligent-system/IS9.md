# Artificial Neural Networks

Arsitektur ANN
![](attachments/Pasted%20image%2020211102195804.png)

Input X1 to Xn and they have each weight, and then output Y
![](attachments/Pasted%20image%2020211102195929.png)

## Activation Function
Activation function of neuron
![](attachments/Pasted%20image%2020211102201233.png)

**Sign Function**, sign plus or minus based on the value of x.
The activation function:
![](attachments/Pasted%20image%2020211102200322.png)

$x1w1 + x2w2 + xnwn$

If the output is the sum of weighted value of x \* w. 
- The threshold is 0, if value is lower than 0, neuron output is -1.
- If the value is greater or equal to 0, neuron is activated and the output is +1

**Step Function**, just like sign function, but with the y 1 or 0, instead of 1 and -1. Sign function and step function produce discontinuity. 

> Step function and Sign function have discontinuity (the value is discontinue to 0, 1, or -1, it can be a problem if we apply optimization, such as gradient descent). 
 
**Linear Function**

**Sigmoid Function**

**RelU**

## Perceptron
by Frank Rosenblatt, first training algorithm for a simple ANN. Consists of a single neuron with adjustable weight with a hard limiter (apply discontinuity).
![](attachments/Pasted%20image%2020211102203243.png)

The aim of perceptron is to classify inputs into one of two classes (A1 and A2).

In the case of an elementary perceptron, the n-dimensional space is divided by a hyperplane into two decision regions. Hyperplane is defined by the linearly separable function:
![](attachments/Pasted%20image%2020211102203730.png)

Two input preceptron classified with two dimensional space (cartesian) and three input perceptron classified with three dimensional space.
![](attachments/Pasted%20image%2020211102204109.png)

For two dimensional space, we can separate using line, for three dimensional space, we can separate using plane. For four dimensional space, we can use hyperplane (we can not see or feel it, but you can imagine it)

**How does the perceptron learn its classification?**
Small adjusment in the weight to reduce the difference between the actual and desired outputs of the perceptron. The initial weights are randomly assigned, usually in the range of `[-0.5, 0.5]`, then updated when training is operating.

$y = w0 + w1x1 + w2x2 + wnxn$

You have the desired condition and actual condition, the model is being trained to match closely to desired condition and you can calculate the error value (how far the actual condition off from desired condition)

![](attachments/Pasted%20image%2020211102205749.png)

e(p) = error
Yd(p) = desired output
Y(p) = actual output

If the error is positive, we need to increase Y(p), but if it is negative, we need to decrease Y(p).

**Perceptron learning rule**
![](attachments/Pasted%20image%2020211102210051.png)

p = previous output
$\alpha$ = is the learning rate.

If the error positive, you increase the weight.
If the error is negative, you decrease the weight.

## Perceptron Training Algorithm
1 - Initialization
Set initial weight, and threshold ($\theta$) to random numbers in the range of $[-0.5, 0.5]$, it is adjustable later on based on error value.

2 - Activation
Using step function
$Y(p) = step [\sum_{i=1}^{n} x_i(p).w_i(p) - \theta]$

3 - Weight training
Update the weights of the perceptron
$w_i(p+1) = w_i(p)+\Delta w_i(p)$

The weight correction is computed by the delta rule:
$\Delta w_i(p) = \alpha.x_i(p).e(p)$

4 -  Iteration
Increase iteration p by one, go back to step 2 and repeat the process until convergence.

Results -
![](attachments/Pasted%20image%2020211102213103.png)

The threshold and learning rate is fixed, which are $\theta = 0.2$ and $\alpha = 0.1$
Epoch 1 still has error, so we want to change the weights.

**How to understand the result**
- Understand that there is constant desired output $Y_d(p)$ is 0, 0, 0, 1 on all epoch.
- Understand that there is constant value of $x_1, x_2$ which are (0,0 ; 0,1 ; 1,0 ; 1,1)
- You know that $\alpha$ is 0.1 and $\theta$  is 0.2 on all epoch.

**Calculate the Y(p)**
$Y(p) = step [\sum_{i=1}^{n} x_i(p).w_i(p) - \theta]$

Calculate this first
$w_1.x_1+w_2.x_2-\theta$

Input $x_1 = 0$ and $x_2 =0$ 
$(0.3 * 0) + (-0.1 * 0) - 0.2 = -0.2$

**Feed into activation function**
If result < 0, $Y(p)$ is 0
If result >= 0, $Y(p)$ is 1

So, $Y(p) = 0$

**Look for error value**
Error value $e(p) = Y_d(p) - Y(p)$
Error value is 0

**Weight correction **
$\Delta w_i(p) = \alpha.x_i(p).e(p)$

On $x1$
$\Delta w_i(p) = 0.1 * 0 * 0$
$\Delta w_i(p) = 0$

On $x2$
$\Delta w_i(p) = 0.1 * 0 * 0$
$\Delta w_i(p) = 0$

**Weight Update (because no error, there is no weight update)**
$w_i(p+1) = w_i(p)+\Delta w_i(p)$

On $x1$
$w_i(p+1) = w_i(p)+\Delta w_i(p)$
$w_i(p+1) = 0.3 + 0$

On $x2$
$w_i(p+1) = w_i(p)+\Delta w_i(p)$
$w_i(p+1) = -0.1 + 0$

**You got that**
![](attachments/Pasted%20image%2020211102223617.png)

The calculation really happens at input that produces error.



