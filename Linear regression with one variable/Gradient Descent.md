# Gradient Descent

- Gradient descent is a algorithm for minimizing the cost function. (You can use gradient descent to minimize other functions as well, not just the cost function J for the linear regression.)
- So we have our hypothesis function and we have a way of measuring how well it fits into the data. Now we need to estimate the parameters in the hypothesis function.
![Alt_text](https://i.imgur.com/gMNkqyV.jpg)

- Imagine that we graph our hypothesis function based on its fields theta_0 and theta_1  (actually we are graphing the cost function as a function of the parameter estimates). We are not graphing x and y itself, but the parameter range of our hypothesis function and the cost resulting from selecting a particular set of parameters.
- We put theta_0 on the x axis and theta_1 on the y axis, with the cost function on the vertical z axis. The points on our graph will be the result of the cost function using our hypothesis with those specific theta parameters. 
![alt_text](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bn9SyaDIEeav5QpTGIv-Pg_0d06dca3d225f3de8b5a4a7e92254153_Screenshot-2016-11-01-23.48.26.png?expiry=1627516800000&hmac=WI14KtDOmXioOm9bAc3sJ7pnPV_xfj9mdMWVegizkqo)
- We will know that we have succeeded when our cost function is at the very bottom of the pits in our graph, i.e. when its value is the minimum. 
- The way we do this is by taking the derivative (the tangential line to a function) of our cost function. The slope of the tangent is the derivative at that point and it will give us a direction to move towards. We make steps down the cost function in the direction with the steepest descent. The size of each step is determined by the parameter α, which is called the learning rate. 
- For example, the distance between each 'star' in the graph above represents a step determined by our parameter α. A smaller α would result in a smaller step and a larger α results in a larger step. The direction in which the step is taken is determined by the partial derivative of J(theta_0,theta_1). Depending on where one starts on the graph, one could end up at different points. The image above shows us two different starting points that end up in two different places. 
- So if you had started the first point, you would've wound up at left local optimum, but if you started just at a slightly different location, you would've wound up at a very different local optimum.
- The gradient descent algorithm is: 
- ![alt_text](https://i.imgur.com/W3RX6HA.jpg)
- := is the assignment operator.  If a := b  this means in computers take the value in b and use it overwrite whatever value is a. (Whereas in contrast, if I use the equal sign and I write a equals b, then this is a truth assertion)
- This alpha is the learning rate
- And the subtlety of how you implement gradient descent is for th expression, for this update equation, you want to simultaneously update theta 0 and theta 1.
- So I'm gonna set temp0 equals that, set temp1 equals that so basic compute the right-hand sides, and then having computed the right-hand sides and stored them into variables temp0 and temp1, I'm gonna update theta 0 and theta 1 simultaneously because that's the correct implementation.
- ![Alt_text](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yr-D1aDMEeai9RKvXdDYag_627e5ab52d5ff941c0fcc741c2b162a0_Screenshot-2016-11-02-00.19.56.png?expiry=1627516800000&hmac=lieJ7AYTVLQepsubnIy00DqFT3pKxdH8HWSBGYAul_I)
- Right is wrong: by this time you've already updated theta 0, then you would be using the new value of theta 0 to compute this derivative term. And so this gives you a different value of temp1, than the left-hand side. Because you've now plugged in the new value of theta 0 into this equation. And so, this on the right-hand side is not a correct implementation of gradient descent.
