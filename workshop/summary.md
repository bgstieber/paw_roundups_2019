
# Deep Learning Tutorial


## Notes

AI is ML applied to six different settings
    five senses (sight, sound, taste, touch, smell)
    understanding


package manager is important
    anaconda has one, called conda
        JM strongly recommends not using it
    use pip instead 

hyperparameter training is mostly done by trial-and-error
    model.add(K.layers.Dense(units=5, input_dim=4, activation='tanh')) # units is hyper
    model.add(K.layers.Dense(units=3, activation='softmax')) # units refers to num of prediction cols

ONNX - standard way to save NN models

"enough data": 100s of thousands, or millions, or even billions

standardizing: dividing by constant (naive scaling), z-scoring, min-max (x - min(x) / max(x) - min(x))
    which one should you use when?
        z-score: investigate values with abs(x) > 6
        naive scaling (order magnitude): he likes this one the most

binary predictor: map to -1/1 not 0/1 (differs from standard statistical approach)
    Lots of ways to do predictor encoding
        1 of (N-1): "interaction effects"/"effect coding"
        1 of N
    Encoding things to predict
        1 of N (one hot) if more than two classes
        binary: use 0/1

handling 10,000 classes?
    one hot with sparse encoding

soft-max: coerces output of NN to sum to 1, allowing for a probability interpretation
    useful when trying to predict 1 of something

number of input nodes matches number of predictors
number of hidden nodes is hyperparameter
number of output nodes matches number of things you're trying to predict

lines connecting nodes are "weights" (importance of value from node?)
biases applied to nodes (like intercept in regression)

training helps us to learn the weights

algorithms (only really need to know two)
    single hidden layer
        stochastic gradient descent and backpropagation (primitive)
    multiple hidden layers
        AdaM: adaptive momentum becoming standard for larger problems

activation function for hidden nodes:
    single hidden layer: tanh (hyperbolic tangent)
    multiple hidden layers: ReLU

activation function for output node
    multi-class: softmax
    binary: sigmoid

Universal approximation theorem: single hidden layer can do (approximately) the same task as a deep neural net

90% + of your time is spent prepraring your data (even the ML guy from Microsoft agrees!)
    cleaning, normalizing, and encoding the data

training
    full training: analyze data, update weights
    online training: read single data item, update all weights
    batch training: read subset of data, process, update weights
        batch size: hyperparameter (8 or 16)
        epochs: hyperparamter

techniques you should know about
    momentum: technique to speed up training
    dropout: technique to prevent overfitting
        functions are characterized by their weights
            large weights, not so good
            want to keep weights small
        works well for deep neural networks, not simple
        Dropout consists in randomly setting a fraction rate of input units to 0 at each update during training time, which helps prevent overfitting.
            fraction is a hyperparameter

LSTM with word embeddings - what does the data look like?
    he's got an example on his blog

Naive Bayes is particularly good when combined with NN in ensemble model

Naive Bayes - very good for small data sets 

If you have missing data for a neural network, toss it out

Outstanding questions

1. class imbalance
2. what to do next
    - substantial amount of time spent data prepping
    - have the environment, so you're ready to go
3. Unsupervised technique
    - Autoencoder for anomaly detection
        + worth looking more into autoencoders, what does the data look like at every stage?


