# Normal Equation
\
Gradient descent gives one way of minimizing J. Let’s discuss a second way of doing so, this time performing the minimization explicitly and without resorting to an iterative algorithm.\
In the "Normal Equation" method, we will minimize J by explicitly taking its derivatives with respect to the θj ’s, and setting them to zero.\
This allows us to find the optimum theta without iteration. The normal equation formula is given below: \
![alt_text](https://i.imgur.com/x6Zsc2m.png)\
\
Let's take a very simplified cost function J of Theta. So, for now, imagine that Theta is just a scalar value or that Theta is just a row value/real number. \
We have a cost function J that's a quadratic function of this real value parameter Theta.\
To minimize a quadratic function take derivative J with respect to the parameter of Theta and to set derivatives equal to zero. \
The value of Theda that minimizes J of Theta.\
![alt_text](https://i.imgur.com/JfGH38A.png)\
In the problem that we are interested in, Theta is no longer just a real number, but is this n+1-dimensional parameter vector
and, a cost function J is a function of this vector value or Theta 0 through Theta m\
To minimize this cost function J? You take the partial derivative of J, with respect to every parameter of Theta J in turn, and then, to set all of these to 0.
If you do that, and you solve for the values of Theta 0, Theta 1, up to Theta N, then, this would give you that values of Theta to minimize the cost function J.\
![alt_text](https://i.imgur.com/CpUzaUo.png)\
\
How to implement this algorithm? In aexample let's say that I have m = 4 training examples.\
Take the data set and add an extra column that corresponds to my extra feature, x0, that is always takes on this valu.e of 1.\
Then construct a matrix called X that's a matrix are basically contains all of the features from my training data\
Let's do something similar for y's. Take the values that we are trying to predict and construct now a vector, like so and call that a vector y.\
X is going to be a m by (n+1) - dimensional matrix, and Y is going to be a m-dimensional vector. Where m is the number of training examples, n is, n is a number of features and n+1, because of this extra feature X0.\
Set theta to be equal to X transpose X inverse times X transpose Y, this would give you the value of theta that minimizes your cost function.\
![alt_text](https://i.imgur.com/wUsJU18.png)\
More general:\ 
![alt_text](https://i.imgur.com/2vkatSU.png)\
For Matrix X take the first training example, so that's a vector, take its transpose into the first row of my design matrix.
Then I am going to take my second training example, x2, take the transpose of that and put that as the second row of x and so on, down until my last training example.
Take the transpose of that, and that's my last row of my matrix X. And, so, that makes my matrix X, an M by N +1 dimensional matrix. \
The vector Y is obtained by taking all all the labels (e.g. all the correct prices of houses) and just stacking them up into an M-dimensional vector.\
Finally, having constructed the matrix X and the vector Y, we then just compute theta as:\
![alt_text](https://i.imgur.com/njoi6uv.png)
![alt_text](https://i.imgur.com/CtYs7p7.png)\

There is no need to do feature scaling with the normal equation.\

### The following is a comparison of gradient descent and the normal equation:\
![alt_text](https://i.imgur.com/nbt9mkX.png)\
With the normal equation, computing the inversion has complexity O(n^3).So if we have a very large number of features, the normal equation will be slow.\
In practice, when n exceeds 10,000 it might be a good time to go from a normal solution to an iterative process.
