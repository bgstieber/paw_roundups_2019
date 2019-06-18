
# Deep Learning Tutorial

__Note:__ in general, this tutorial was very good, but did bounce around quite a bit between stories from JM's experience, fitting models, looking at code, and investigating what the code was returning. The notes below somewhat match this bounciness.

## Notes

AI is ML applied to six different settings

  - five senses (sight, sound, taste, touch, smell)
  - understanding

package manager is important

   - anaconda has one, called conda
       - JM strongly recommends not using it
   - use pip instead 

hyperparameter training is mostly done by trial-and-error

`model.add(K.layers.Dense(units=5, input_dim=4, activation='tanh'))`

units is hyperparameter controlling number of hidden nodes

`model.add(K.layers.Dense(units=3, activation='softmax'))` 

units refers to num of prediction cols (predictions to return)

ONNX - standard way to save NN models

"enough data": 100s of thousands, or millions, or even billions

standardizing: dividing by constant (naive scaling), z-scoring, min-max (x - min(x) / max(x) - min(x))
    
which one should you use when? depends on problem context, but JM has had most success with order magnitude scaling (x / K)
    
- z-score: investigate values with abs(x) > 6
- naive scaling (order magnitude): he likes this one the most

binary predictor: map to -1/1 not 0/1 (differs from standard statistical approach)

- Lots of ways to do predictor encoding
    + 1 of (N-1): "interaction effects"/"effect coding"
    + 1 of N
- Encoding things to predict
    + 1 of N (one hot) if more than two classes
    + binary: use 0/1

handling 10,000 classes? one hot with sparse encoding

soft-max: coerces output of NN to sum to 1, allowing for a probability interpretation. This is useful in multi-class problems

thumbrules:

- number of input nodes matches number of predictors
- number of hidden nodes is hyperparameter
- number of hidden layers is hyperparameter
- number of output nodes matches number of things you're trying to predict

lines connecting nodes are "weights" (importance of value from node?)
biases applied to nodes (like intercept in regression)

training helps us to learn the weights

algorithms (only really need to know two)

- single hidden layer (simple neural network)
    + stochastic gradient descent and backpropagation (primitive)
- multiple hidden layers (deep neural network)
    + AdaM: adaptive momentum becoming standard for larger problems

activation function for hidden nodes:

- single hidden layer: tanh (hyperbolic tangent)
- multiple hidden layers: ReLU

activation function for output node

- multi-class: softmax
- binary: logistic sigmoid
- regression: None

[loss functions](https://keras.io/losses/)

- multi-class: categorical_crossentropy
- binary: binary_crossentropy
- regression: mean_squared_error (or pick another flavor)

[Universal approximation theorem](https://en.wikipedia.org/wiki/Universal_approximation_theorem): single hidden layer can do (approximately) the same task as a deep neural net

90% + of your time is spent prepraring your data (even the ML guy from Microsoft agrees!)

- cleaning, normalizing, and encoding the data

[training types (how it gets done)](https://www.kaggle.com/residentmario/full-batch-mini-batch-and-online-learning)

- full training: analyze data, update weights
- online training: read single data item, update all weights
- batch training: read subset of data, process, update weights
    + batch size: hyperparameter (8 or 16)
    + epochs: hyperparamter

techniques you should know about (__try to find some tutorials/blogs__)

- momentum: technique to speed up training
- dropout: technique to prevent overfitting
    + functions are characterized by their weights
        * large weights, not so good - want to keep weights small
    + works well for deep neural networks, not simple
    + Dropout consists in randomly setting a fraction rate of input units to 0 at each update during training time, which helps prevent overfitting.
        * fraction is a hyperparameter

LSTM with word embeddings - what does the data look like? he's got an example on his blog

Naive Bayes is particularly good when combined with NN in ensemble model

Naive Bayes - very good for small data sets 

If you have missing data for a neural network, toss it out

Outstanding questions

1. class imbalance
2. what to do next
    - substantial amount of time spent data prepping
    - have the environment, experience with Keras, and lots of sample templates, so you're ready to go
3. Unsupervised technique
    - Autoencoder for anomaly detection
        + worth looking more into autoencoders, what does the data look like at every stage?

## Main Takeaways

- Set up a "professional" python environment
- Walked through multiple examples of real problems being solved using neural networks in python with keras
- Understood different activation functions, loss functions, and optimization algorithms
- Learned about many different approaches to machine learning problems and some basic principles
- Learned about one typical folder structure of a machine learning project
- Spent time focusing on data manipulation and encoding techniques for neural nets
- Model evaluations with neural networks are mostly about accuracy
    + Important to pick a "good" accuracy measure for regression
        * His example: what % of predictions were within 15% of the true value?
- Plenty of opportunities for comparing and contrasting Machine Learning and Statistical Modeling techniques/principles/ideas