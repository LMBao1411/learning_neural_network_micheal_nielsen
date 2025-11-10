MICHEAL NIELSEN IMPLEMENTATION
source: http://neuralnetworksanddeeplearning.com/
28x28=784 pixels, 0.0 representing white and 1.0 representing black
denote the corresponding desired output by y=y(x), where y is a 10-dimensional vector.
For example, if a particular training image, x depicts a 6 then y(x)=(0,0,0,0,0,0,1,0,0,0)T is the desired output.
To quantify how well we're achieving the weights and biases so that the output from the network approximates y(x) for all training inputs x:
Loss function:  C(w,b) ≡ (1/2n) ∑(∥y(x)−a∥)^2.
w is all the weights, b is all the biases

In other words, we want to find a set of weights and biases which make the cost as small as possible.
We'll do that using an algorithm known as gradient descent
We're going to find a way of choosing Δv1 and Δv2 so as to make ΔC negative
$ ΔC ≈ (∂C/∂v1)Δv1 + (∂C/∂v2)Δv2 $
The gradient of C to be the vector of partial derivatives: $ (∂C/∂v1,∂C/∂v2)T $
We denote the gradient vector by ∇C:
$ ∇C ≡ (∂C/∂v1,∂C/∂v2)T $