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

We can speed up gradient descent by having each of our input values in roughly the same range. This is because θ will descend quickly on small ranges and slowly on large ranges, and so will oscillate inefficiently down to the optimum when the variables are very uneven.\
The way to prevent this is to modify the ranges of our input variables so that they are all roughly the same. Ideally:\
![alt_text](https://i.imgur.com/TSOwLUt.png)

These aren't exact requirements; we are only trying to speed things up. The goal is to get all input variables into roughly one of these ranges, give or take a few.\
Two techniques to help with this are feature scaling and mean normalization. Feature scaling involves dividing the input values by the range (i.e. the maximum value minus the minimum value) of the input variable, resulting in a new range of just 1. Mean normalization involves subtracting the average value for an input variable from the values for that input variable resulting in a new average value for the input variable of just zero. To implement both of these techniques, adjust your input values as shown in this formula:
![alt_text](https://i.imgur.com/I4JUTBm.png)

Where μ_i is the average of all the values for feature (i) and s_i is the range of values (max - min), or s_is is the standard deviation.\
Note that dividing by the range, or dividing by the standard deviation, give different results. \

For example, if x_i represents housing prices with a range of 100 to 2000  and a mean value of 1000, then:\
![alt_text](https://i.imgur.com/JsfvBIZ.png)
