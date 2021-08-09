# Classification 

The classification problem is just like the regression problem, except that the values we now want to predict take on only a small number of discrete values. Let's focus on the **binary classification** problem in which y can take on only two values, 0 and 1. ) \
For instance, if we are trying to build a spam classifier for email, then x^(i) may be some features of a piece of email, and y may be 1 if it is a piece of spam mail, and 0 otherwise.\
The variable that we're trying to predict is a variable y that we can think of as taking on two values either zero or one, hence, y∈{0,1}. 0 is also called the negative class, and 1 the positive class, and they are sometimes also denoted by the symbols “-” and “+.” \
Given x^(i), the corresponding y^(i) is also called the label for the training example. 


# Hypothesis Representation 
It  doesn’t make sense for h_theta(x) to take values larger than 1 or smaller than 0 when we know that y ∈ {0, 1}. This would occur in a linear regression.
To fix this, let’s change the form for our hypotheses h_theta(x)to satisfy **0 ≤ h_theta(x) ≤ 1**. This is accomplished by plugging theta^T * x into the Logistic Function.\
\
Our new form uses the "Sigmoid Function," also called the "Logistic Function":\
![alt_text](https://i.imgur.com/szMJoqK.png)\
The following image shows us what the sigmoid function looks like: \
![alt_text](https://i.imgur.com/1QNWwEy.png)\
\
The function g(z), shown here, maps any real number to the (0, 1) interval, making it useful for transforming an arbitrary-valued function into a function better suited for classification.

h_theta(x) will give us the probability that our output is 1. For example, h_theta(x)=0.7 gives us a probability of 70% that our output is 1. Our probability that our prediction is 0 is just the complement of our probability that it is 1 (e.g. if probability that it is 1 is 70%, then the probability that it is 0 is 30%).\
![alt_text](https://i.imgur.com/lYigya1.png)\
Reading: P(y=1|x;theta) This is the probability (P()) that y is equal to one. Given x, given the features x(e.g   tumor size in a patient) and this probability is parameterized by theta. 


# Decision Boundary 

In order to get our discrete 0 or 1 classification, we can translate the output of the hypothesis function as follows:\
![alt_text](https://i.imgur.com/qVPjHjC.png)\
The way our logistic function g behaves is that when its input is greater than or equal to zero, its output is greater than or equal to 0.5:\
![alt_text](https://i.imgur.com/aS736x2.png)\
Note:\
![alt_text](https://i.imgur.com/XEd0mNI.png)\
So if our input to g is theta^T * X, then that means:\
![alt_text](https://i.imgur.com/3G9acBW.png)\
From these statements we can now say:\
![alt_text](https://i.imgur.com/IyWY8s7.png)\
The decision boundary is the line that separates the area where y = 0 and where y = 1. It is created by our hypothesis function.\

Example:\
![alt_text](https://i.imgur.com/rbNXutx.png)\
Let's suppose we end up choosing the following values for the parameters. theta 0 equals 3, theta 1 equals 1, theta 2 equals 1.\
We know that y equals one is more likely, that is the probability that y equals one is greater than or equal to 0.5, whenever theta transpose x is greater than zero. \
![alt_text](https://i.imgur.com/GC7qg7p.png)\
![alt_text](https://i.imgur.com/1ACs6Pq.png)\
The green straight line, X1 plus X equals 3. That corresponds to the region where H of X is equal to 0.5 exactly. This is the decision boundary that separates the region where the hypothesis predicts Y equals 1 from the region where the hypothesis predicts that y is equal to zero.
\
Example non-linear decision boundarier:\
We could add extra higher order polynomial terms to the features for logistic regression.\
![alt_text](https://i.imgur.com/nRVDT4I.png)\
Hypothesis will predict that y=1 whenever -1 + x1 squared + x2 squared is greater than or equal to 0. This is whenever theta transpose times my theta transfers, my features is greater than or equal to zero.\
![alt_text](https://i.imgur.com/jWf6hd1.png)\
If you were to plot the curve for x1 squared plus x2 squared equals 1, that is the equation for circle of radius one, centered around the origin. So that is the decision boundary.\
![alt_text](https://i.imgur.com/nolvUa6.png)\

