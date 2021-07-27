# Model representation
- To establish notation for future use, we’ll use x^(i)  to denote the “input” variables (living area in this example), also called input features
and y^(i) to denote the “output” or target variable that we are trying to predict (price). 
- A pair (x^(i) , y^(i))is called a training example, 
and the dataset that we’ll be using to learn—a list of m training examples (x^(i) , y^(i) ); i = 1, . . . , mis called a training set. Note that the superscript “(i)” in the notation is simply an index into the training set, and has nothing to do with exponentiation. We will also use X to denote the space of input values, and Y to denote the space of output values. 
In this example, X = Y = ℝ. 

- To describe the supervised learning problemwe use the function h : X → Y so that h(x) is a “good” predictor for the corresponding value of y. 
this function h is called a hypothesis.
![alt text](https://images3.programmersought.com/573/a2/a220024e9dc5043f20b95b4ef9b5851d.png)

# Cost function:
-We can measure the accuracy of our hypothesis function by using a cost function. This takes an average difference  of all the results of the hypothesis with inputs from x's and the actual output y's.
See ride side:

![alt text](https://i.imgur.com/bQh4Zl8.jpg)![alt text](https://images4.programmersought.com/760/a7/a716a4b7783155b0dea56f41acf96ef0.png)
- To break it apart, it is 1/2 x where x is the mean of the squares of h0(x(^i)) - y^(i)or the difference between the predicted value and the actual value.
- This function is otherwise called the "Squared error function", or "Mean squared error". The mean is halved  1/2 as a convenience for the computation of the gradient descent, as the derivative term of the square function will cancel out the 1/2 term. The following image summarizes what the cost function does: 

- To understand the cost function. To do so, we simplify the algorithm. So that it only had one parameter theta one. And we set the parameter theta zero to be only zero. 
- Our objective is to get the best possible line. The best possible line will be such so that the average squared vertical distances of the scattered points from the line will be the least. Ideally, the line should pass through all the points of our training data set. In such a case, the value of J(theta_0, theta_1) will be 0. 
- ![alt_text](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_B8TJZtREea33w76dwnDIg_3e3d4433e32478f8df446d0b6da26c27_Screenshot-2016-10-26-00.57.56.png?expiry=1627516800000&hmac=0vNbjp0msX8d6GCfkG0245auxxN_ZNL1yBwNi7P9bEI)![alt_text](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fph0S5tTEeajtg5TyD0vYA_9b28bdfeb34b2d4914d0b64903735cf1_Screenshot-2016-10-26-01.09.05.png?expiry=1627516800000&hmac=6DIlAu41xhPZX9GPO7BoGGzlKVsjxfIBPxVPoCdYWe0)
