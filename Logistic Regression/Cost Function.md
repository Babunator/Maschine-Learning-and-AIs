# Cost Function for logistic regression
We cannot use the same cost function that we use for linear regression because the Logistic Function will cause the output to be wavy, causing many local optima. In other words, it will not be a convex function.\

Instead, our cost function for logistic regression looks like:\
![alt_text](https://i.imgur.com/83hVimb.png)

When y = 1, we get the following plot J(θ) vs h_θ(x):\
![alt_text](https://i.imgur.com/MLOVTOu.png)\
Why the plot looks like this is because if you were to plot log z with z on the horizontal axis, then that looks like below. But we're interested only in the range of when this function goes between zero and one.\
![alt_text](https://i.imgur.com/3G4gBzr.png)\
First, notice that if h(x) = 1, if that hypothesis predicts that y = 1 and if indeed y = 1 then the cost = 0.\
But now notice also that as h(x) approaches 0, so as the output of a hypothesis approaches 0, the cost blows up and it goes to infinity. And what this does is this captures the intuition that if a hypothesis of 0, that's like saying a hypothesis saying the chance of y equals 1 is equal to 0.\
If we told a prediction this with that level of certainty and we turn out to be wrong, then we penalize the learning algorithm by a very, very large cost.\
![alt_text](https://i.imgur.com/hxMZAVY.png)\
\
Similarly, when y = 0, we get the following plot for J(θ) vs h_θ(x):\
![alt_text](https://i.imgur.com/741pvyN.png)\

![alt_text](https://i.imgur.com/vnMs6Wq.png)\
If our correct answer 'y' is 0, then the cost function will be 0 if our hypothesis function also outputs 0. If our hypothesis approaches 1, then the cost function will approach infinity.\
If our correct answer 'y' is 1, then the cost function will be 0 if our hypothesis function outputs 1. If our hypothesis approaches 0, then the cost function will approach infinity.

Note that writing the cost function in this way guarantees that J(θ) is convex for logistic regression.

# Simplified Cost Function 
We can compress our cost function's two conditional cases into one case:\
![alt_text](https://i.imgur.com/83hVimb.png)\
Our overall cost function is 1 over m times the sum over the trading set of the cost of making different predictions on the different examples of labels y i.\
We say that cost of H(x), y. Write this as -y times log(h(x))- (1-y) times log (1-h(x)).
Because it's equal to the previous cost function. Let's put in y= 1 and y=0:
![alt_text](https://i.imgur.com/pJkcuXE.png)\
![alt_text](https://i.imgur.com/sSXoAyG.png)\
Often the minus sign will be put outside.\
