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
