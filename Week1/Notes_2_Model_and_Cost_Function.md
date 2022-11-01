# Notes_2_Model_and_Cost_Function

## Model

To establish notation for future use, we’ll use x(i)x(i) to denote the “input” variables (living area in this example), also called input features, and y(i)y(i) to denote the “output” or target variable that we are trying to predict (price). A pair (x(i),y(i))(x(i),y(i)) is called a training example, and the dataset that we’ll be using to learn—a list of m training examples (x(i),y(i));i=1,...,m(x(i),y(i));i=1,...,m—is called a training set. Note that the superscript “(i)” in the notation is simply an index into the training set, and has nothing to do with exponentiation. We will also use X to denote the space of input values, and Y to denote the space of output values. In this example, X = Y = ℝ.

## Cost Function

We can measure the *accuracy* of our hypothesis function by using a cost function. This takes an average difference (actually a fancier version of an average) of all the results of the hypothesis with inputs from x's and the actual output y's.

J(θ0,θ1)=12m∑i=1m(y^i−yi)2=12m∑i=1m(hθ(xi)−yi)2J(θ0​,θ1​)=2m1​i=1∑m​(y^​i​−yi​)2=2m1​i=1∑m​(hθ​(xi​)−yi​)2

To break it apart, it is 1221​ xˉxˉ where xˉxˉ is the mean of the squares of hθ(xi)−yihθ​(xi​)−yi​ , or the difference between the predicted value and the actual value.

This function is otherwise called the "Squared error function", or "Mean squared error". The mean is halved (12)(21​) as a convenience for the computation of the gradient descent, as the derivative term of the square function will cancel out the 1221​ term. The following image summarizes what the cost function does:

```
Hyptothesis is the function for ML.
Cost function desfines the correctness of Hypothesis.

Minimizing Cost Function is aim.
```
