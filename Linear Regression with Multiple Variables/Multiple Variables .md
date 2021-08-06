# Multiple Features
\
Linear regression with multiple variables is also known as "multivariate linear regression".\
We now introduce notation for equations where we can have any number of input variables:\
![alt_text](https://i.imgur.com/wAbSLUG.png)
![alt_text](https://i.imgur.com/LL9wYZf.png)

The multivariable form of the hypothesis function accommodating these multiple features is as follows:\
![alt_text](https://i.imgur.com/w1X2muP.png)


In order to develop intuition about this function, we can think about θ0 (theta 0) as the basic price of a house, θ1 as the price per square meter, θ2 as the price per floor, etc.\
x1 will be the number of square meters in the house, x2 the number of floors, etc.

In this is formal hypothesis of a multivariable linear regression where we've adopted the convention that x0=1.
The parameters of this model are theta0 through theta n, but we can, instead of thinking of this as n separate parameters, we are going to think of the parameters as theta where theta here is a n+1-dimensional vector. 
So the parameters of this model as itself are a vector.
![alt_text](https://i.imgur.com/31Dld27.png)
![alt_text](https://i.imgur.com/ZjpXxC4.png)\
Using the definition of matrix multiplication, our multivariable hypothesis function can be concisely represented as:\
![alt_text](https://i.imgur.com/0QLWZ9C.png)
\
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
