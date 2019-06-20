# Tensorflow and Deep Reinforcement Learning without a PhD - Gorner
 
## Notes 
 
- NN 101
    + activation functions (relu and softmax)
    + Loss functions (cross entropy: `-sum_i(y_i * log(hat(y_i))`, `y_i` actual probability (one hot), `hat(y_i)` predicted probabilities)
- Tensorflow 101
    + add layers with appropriate data, size, and activation functions
    + define loss function and final activation function
    + define optimizer (gradient methods: move in the direction of largest improvement in loss function)
- What about playing pong?
    + Easy to get the input (pixels for the pong board), but how to know the correct board
    + This is where reinforcement learning comes in
    + Policy gradients, transforming loss function into reward function by being based on future outcome of move
        * Can weight the policy gradient: discounted rewards and normalized rewards
 
## Key Takeaways 

- RL seems kind of fun, but does require some "hacking" of normal neural networks
    + Might need to resort to low level tensorflow programming
- Neural architecture search
    + Use NN with rewards, policy graidents, and RL to build a better neural network architecture
        * AutoML
- 
 
## Other Details / Follow Up 
 
[Blog post](https://karpathy.github.io/2016/05/31/rl/) on the pong thing

[Learn TensorFlow and deep learning, without a Ph.D.](https://cloud.google.com/blog/products/gcp/learn-tensorflow-and-deep-learning-without-a-phd)

Improve understanding of what the data actually looks like. Where do the win/lose come from?
