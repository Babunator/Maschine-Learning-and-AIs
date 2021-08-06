# Gradient Descent for Multiple Variables
\
Instead of thinking of J as a function of  n+1 numbers, we can write J as just a function of the parameter vector theta.\
![alt_text](https://i.imgur.com/saL1boQ.png)\

In the gradient descent it will repeatedly update each parameter theta j according to theta j minus alpha times this derivative term. And once again we just write this as J of vector theta. 
![alt_text](https://i.imgur.com/4aoup9O.png)\
\
Here's what we have for gradient descent for the case of when we had N=1 feature. 
We had two separate update rules for the parameters theta0 and theta1.
The partial derivative of the cost function with respect to the parameter of theta0, and similarly we had a different update rule for the parameter theta1.
We previously had only one feature, we would call that feature x(i) but now in our new notation we would of course call this x(i)_1 to denote our one feature.\
![alt_text](https://i.imgur.com/nx5mSGz.png)\
In the new algorithm for we have more than one feature.\
if you take the definition of the cost function and take the partial derivative of the cost function J with respect to the parameter theta j, you'll find that that partial derivative is exactly:\
![alt_text](https://i.imgur.com/oISFo6P.png)\

Let's consider a case where we have two features or maybe more than two features, so we have three update rules for the parameters theta0, theta1, theta2 and maybe other values of theta as well.\
If you look at the update rule for theta0, what you find is that this update rule here is the same as the update rule that we had previously for the case of n = 1. 
And the reason that they are equivalent is, because in our notational convention x(i)_0 = 1 , which is why these two term  are equivalent.\
Similarly, if you look the update rule for theta1, you find that this term here is equivalent to the e equation or the update rule we previously had for theta1, where of course we're just using this new notation x(i)_1 to denote our first feature.\
And now that we have more than one feature we can have similar update rules for the other parameters like theta2 and so on.\
![alt_text](https://i.imgur.com/xRaGK2q.png)\
\
The gradient descent equation itself is generally the same form; we just have to repeat it for our 'n' features:\
![alt_text](https://i.imgur.com/wBzoSHE.png)\

# Gradient Descent - Feature Scaling
\
We can speed up gradient descent by having each of our input values in roughly the same range. This is because θ will descend quickly on small ranges and slowly on large ranges, and so will oscillate inefficiently down to the optimum when the variables are very uneven.\

The way to prevent this is to modify the ranges of our input variables so that they are all roughly the same. Ideally:\
![alt_text](https://i.imgur.com/TSOwLUt.png)\
Example: If you plot the contours of the function J of parameters theta zero, theta one and theta two.(for now we can ignore theta Zero).
If x1 can take on a much larger range of values than x2.  The contours of the cause function J of theta can take on this very tall and skinny elliptical shape.\
if you run gradient descents on this costfunction, your gradients may end up taking a long time and can oscillate back and forth and take a long time before it can finally find its way to the global minimum.\
![alt_text](https://i.imgur.com/ysCabFZ.png) \
In these settings, a useful thing to do is to scale the features.\
If you instead define the feature X one to be the size of the house divided by two thousand, and define X two to be maybe the number of bedrooms divided by five, then the conture of the cost function is much less skewed so the contours may look more like circles.\
And if you run gradient descent on a cost function you can find a much more direct path to the global minimum.\
![alt_text](https://i.imgur.com/MdsSNtp.png)\

These aren't exact requirements; we are only trying to speed things up. The goal is to get all input variables into roughly one of these ranges, give or take a few.\
Two techniques to help with this are feature scaling and mean normalization. Feature scaling involves dividing the input values by the range (i.e. the maximum value minus the minimum value) of the input variable, resulting in a new range of just 1. Mean normalization involves subtracting the average value for an input variable from the values for that input variable resulting in a new average value for the input variable of just zero. To implement both of these techniques, adjust your input values as shown in this formula:
![alt_text](https://i.imgur.com/I4JUTBm.png)

Where μ_i is the average of all the values for feature (i) and s_i is the range of values (max - min), or s_is is the standard deviation.\
Note that dividing by the range, or dividing by the standard deviation, give different results.\

For example, if x_i represents housing prices with a range of 100 to 2000  and a mean value of 1000, then:\
![alt_text](https://i.imgur.com/JsfvBIZ.png)
\
# Gradient Descent - Learning Rate
\
Debugging gradient descent. Make a plot with number of iterations on the x-axis. Now plot the cost function, J(θ) over the number of iterations of gradient descent. If J(θ) ever increases, then you probably need to decrease α.\
\
The job of gradient descent is to find the value of theta for you that hopefully minimizes the cost function J(theta).\
To make sure that gradient descent is working correctly you can plot the cost function J(theta) as gradient descent runs.\
So the x axis here is a number of iterations of gradient descent and as gradient descent runs you hopefully get a plot liek this:\
![alt_text](https://i.imgur.com/dhOGOjO.png)\

After 100 iteration we get a value for theta and then we need to evaluate the cost function J(theta) (the vertical height is the value of J(theta)). \
The second point here  corresponds to the value of J(theta) for the theta after running gradient descent for 200 iterations.\
So what this plot is showing is, is it's showing the value of your cost function after each iteration of gradient decent. And if gradient is working properly then J(theta) should decrease after every iteration.\
It's also possible to come up with automatic convergence test, namely to have a algorithm try to tell you if gradient descent has converged.\
\
It's possible to come up with automatic convergence test, namely to have a algorithm try to tell you if gradient descent has converged. 
Example:\
Automatic convergence test. Declare convergence if J(θ) decreases by less than E in one iteration, where E is some small value such as 10^−3. However in practice it's difficult to choose this threshold value.\ (Usually choosing what this threshold (here 10^-3) is is pretty difficult.\

Looking at this sort of figure can also tell you, or give you an advance warning, if maybe gradient descent is not working correctly. \
If you see a figure like this where J(theta) is actually increasing, then that gives you a clear sign that gradient descent is not working:\
![alt_text](https://i.imgur.com/8Ge1wDF.png)\
If the learning rate is too big, then gradient descent can instead keep on overshooting the minimum. So that you actually end up getting worse and worse instead of getting to higher values of the cost function J(theta).\
\
Sometimes you may also see J(theta) do something like this, it may go down for a while then go up then go down for a while then go up go down for a while go up and so on:\
![alt_text](https://i.imgur.com/zkYLESS.png)\
A fix for something like this is also to use a smaller value of alpha.\
\
If your learning rate alpha is small enough, then J(theta) should decrease on every iteration. So if this doesn't happen probably means the alpha's too big, you should set it smaller. \
But of course, you also don't want your learning rate to be too small because if you do that then the gradient descent can be slow to converge.
\
Summary:\
If α is too small: slow convergence. \
If α is too large: J(theta) may not decrease on every iteration and thus may not converge.\
In order to debug all of these things, often plotting that J(theta) as a function of the number of iterations can help you figure out what's going on.\
E.g. Try running gradient descent with a range of values for alpha, like 0.001, 0.003, 0.01, 0.03, 0.1, 0,3, 1 ....\
\
# Features and Polynomial Regression
We can improve our features and the form of our hypothesis function in a couple different ways.

We can combine multiple features into one. For example, we can combine x_1 and x_2 into a new feature x_3 by taking x_1 ⋅ x_2x \
e.g:\
![alt_text](https://imgur.com/OMHIsNS.png)\
Let's say you have a housing price data set. Then there are a few different models you might fit to this. \
One thing you could do is fit a quadratic model, where you think the size and the price is a quadratic function.\
But then you may decide that your quadratic model doesn't make sense because of a quadratic function, eventually this function comes back down and well, we don't think housing prices should go down when the size goes up too high.\
So then maybe we might choose a different polynomial model and choose to use instead a cubic function.
![alt_text](https://imgur.com/GZ16sMm.png)\
To predict the price of a house:  theta 0 plus, theta 1 times the size of the house plus, theta 2 times the square size of the house plus, theta 3 times the cube of the size of the house raises that third term. \
In a cubic function feature scaling becomes increasingly important.\
Example square root function:\
![alt_text](https://imgur.com/nLM35KR.png)
## Polynomial Regression
![alt_text](https://i.imgur.com/oimxXaF.png)
