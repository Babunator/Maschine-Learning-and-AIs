# Cost Function for logistic regression
We cannot use the same cost function that we use for linear regression because the Logistic Function will cause the output to be wavy, causing many local optima. In other words, it will not be a convex function.\

Instead, our cost function for logistic regression looks like:\
![alt_text](https://i.imgur.com/a1Tndod.png)\
When y = 1, we get the following plot J(θ) vs h_θ(x):\
![alt_text](https://i.imgur.com/MLOVTOu.png)\
Similarly, when y = 0, we get the following plot for J(θ) vs h_θ(x):\
![alt_text](https://i.imgur.com/741pvyN.png)\
\
![alt_text](https://i.imgur.com/vnMs6Wq.png)\\
If our correct answer 'y' is 0, then the cost function will be 0 if our hypothesis function also outputs 0. If our hypothesis approaches 1, then the cost function will approach infinity.\
If our correct answer 'y' is 1, then the cost function will be 0 if our hypothesis function outputs 1. If our hypothesis approaches 0, then the cost function will approach infinity.\

Note that writing the cost function in this way guarantees that J(θ) is convex for logistic regression.\
