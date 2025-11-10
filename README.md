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
ΔC ≈ (∂C/∂v1)Δv1 + (∂C/∂v2)Δv2
and this is equivalent to ΔC ≈ ∇C⋅Δv
The gradient of C to be the vector of partial derivatives: (∂C/∂v1,∂C/∂v2)T 
∇C ≡ (∂C/∂v1,∂C/∂v2)T

lets us see how to choose Δv so as to make ΔC negative. In particular, suppose we choose
Δv = −η∇C, where η is a small, positive parameter (known as the learning rate).
Then this tells us that ΔC ≈ −η∇C⋅∇C = −η∥∇C∥^2 Because ∥∇C∥^2 ≥ 0
This guarantees that ΔC ≤ 0 i.e., C will always decrease, never increase.

The idea is to use gradient descent to find the weights Wk and biases Bl which minimize the cost function
Let's restate the gradient descent update rule, with the weights and biases replacing the variables Vj
Writing out the gradient descent update rule in terms of components, we have:
Wk -> W'k = Wk - η(∂C/∂Wk)
Bl -> B'l = Bl - η(∂C/∂Bl)

Stochastic gradient descent can be used to speed up learning. 
The idea is to estimate the gradient ∇C by computing ∇Cx for a small sample of randomly chosen training inputs.
By averaging over this small sample it turns out that we can quickly get a good estimate of the true gradient ∇C, and this helps speed up gradient descent, and thus learning.





