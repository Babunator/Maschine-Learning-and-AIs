# Gradient Descent
Now let's figure out how to actually minimize J of theta as a function of theta so that we can actually fit the parameters to our training set. The way we're going to minimize the cost function is using gradient descent. \
Here's our cost function and if we want to minimize it as a function of theta, here's our usual template for graded descent where we repeatedly update each parameter by taking, updating it as itself minus learning ray alpha times this derivative term.\
![alt_text](https://i.imgur.com/rpthnVL.png)\
with:\
![alt_text](https://i.imgur.com/ZDnJvAl.png)\

We get:\
![alt_text](https://i.imgur.com/ZeyzydK.png)
The  Gradient Descent rule for linear regression looks exactly what we have for logistic regression. They migh look the same, but definition for the logistic hypothesis h_theta(x) has changed. So as whereas for linear regression, we had h(x) equals theta transpose times X, now this definition of h(x) has changed. And is instead now one over one plus e to the negative transpose x.\
![alt_text](https://i.imgur.com/U7Y7TbT.png)\

A vectorized implementation is:\
![alt_text](https://i.imgur.com/eF75BuC.png)\
To make sure the learning rate \alphaα is set properly and that gradient descent is running correctly you do it similiar like in alinear regression. Plot J(θ) as a function of the number of iterations and make sure J(θ) is decreasing on every iteration.\
