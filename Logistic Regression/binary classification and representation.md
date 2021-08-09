# Classification 

The classification problem is just like the regression problem, except that the values we now want to predict take on only a small number of discrete values. Let's focus on the **binary classification** problem in which y can take on only two values, 0 and 1. ) \
For instance, if we are trying to build a spam classifier for email, then x^(i) may be some features of a piece of email, and y may be 1 if it is a piece of spam mail, and 0 otherwise.\
The variable that we're trying to predict is a variable y that we can think of as taking on two values either zero or one, hence, y∈{0,1}. 0 is also called the negative class, and 1 the positive class, and they are sometimes also denoted by the symbols “-” and “+.” \
Given x^(i), the corresponding y^(i) is also called the label for the training example. 


# Hypothesis Representation 
It  doesn’t make sense for h_theta(x) to take values larger than 1 or smaller than 0 when we know that y ∈ {0, 1}. This would occur in a linear regression.
To fix this, let’s change the form for our hypotheses h_theta(x)to satisfy 0 ≤ h_theta(x) ≤ 1. This is accomplished by plugging theta^T * x into the Logistic Function.\
\
Our new form uses the "Sigmoid Function," also called the "Logistic Function":\
![alt_text](https://i.imgur.com/szMJoqK.png)\
The following image shows us what the sigmoid function looks like: \
![alt_text](https://i.imgur.com/1QNWwEy.png)\
\
The function g(z), shown here, maps any real number to the (0, 1) interval, making it useful for transforming an arbitrary-valued function into a function better suited for classification.\

h_theta(x) will give us the probability that our output is 1. For example, h_theta(x)=0.7 gives us a probability of 70% that our output is 1. Our probability that our prediction is 0 is just the complement of our probability that it is 1 (e.g. if probability that it is 1 is 70%, then the probability that it is 0 is 30%).\
![alt_text](https://i.imgur.com/cf0cBkv.png)

# Decision Boundary 

