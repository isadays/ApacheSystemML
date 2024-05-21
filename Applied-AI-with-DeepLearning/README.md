# Applied-AI-with-DeepLearning
Applied AI with DeepLearning from IBM

![Lorenz attractor](https://github.com/isadays/Applied-AI-with-DeepLearning/blob/main/lorenzattractor.png)


- Some concepts about TensorFlow:

TensorFlow placeholder: A way to add data to the TensorFlow execution graph at a later stage.

Data stored in a TensorFlow variable: The weight matrix W


Unhealthy value distribution (histogram) of values in the weight matrix: Values at the far end of the spectrum indicate over-saturation of the weight matrix;A uniform distribution indicates a lack of parameter updates and therefore problems with training; Most of the values-centered very close to zero forces gradients to become very small

Relationship between accuracy and loss: Both values should behave inversely during neural network training.


 Automatic differentiation in TensorFlow: Every operator in TensorFlow has registered the first derivative of its operation as well. Therefore TensorFlow can apply the chain rule of automatic differentiation to compute the 1st derivative of any complex function

- Some concepts about Keras:

The default backend of Keras is TensorFlow. 

The first layer should have an input_shape argument in an MLP.

Keras layers are core abstractions for every model. 

Sequential models: in sequential models layers have input, output, input_shape, and output_shape.

The Keras layers can get weights as a list of numpy arrays through the command layer.get_weights()

The Keras layers can set the weights through the command layer.set_weights(weights)

Each layer has a defining configuration, through the command  layer_get_config()

#### Building a sequential model (ALgorithm)
1) Instantiate a Sequential model
2) Add layers to it one by one using add
3) Compile the model with a loss function, an optimizer and optional evaluation metrics
4) Use data to fit the model
5) Evaluate the model, persist or deploy model, start new experiment, etc.

- Good practices
  
### Loss functions
from keras.losses import mean_squared_error

model.compile(loss=mean_squared_error, optimizer=...)

### Optimizers 
from keras.optimizers import SGD

sgd = SGD(lr=0.01,decay=1e-6,momentum=0.9)

model.compile(loss=...,optimizer=sgd)

### Fit, evaluate and predict
model.fit(x_train,y_train,batch_size=32, epochs=10, validation_data=(x_val,y_val))

evaluate(x_test,y_test,batch_size=32)

predict(x_test,batch_size=32)

------------------------------------------------

### Feed-Forward networks in Keras

Dense layers with activations

Use Dropout for regularization

Build a Sequential model from Dense and Dropout layers

from keras.layers import Dense

Dense(units, activation=None, use_bias=True, kernel_initializer='glorot_uniform', bias_initializer='zeros')

#units, number of output neurons


Dropout layers - regularization

from keras.layers import Dropout

Dropout(rate, seed=None) 


### Recurrent neural networks in Keras

GRU - Gated Recursive Unit 

LSTM - Long short-term memory

from keras.layers.recurrent import LSTM

LSTM(units, activation = 'tanh', recurrent_activation='hard_sigmoid', recurrent_initializer = 'orthogonal', recurrent_regularizer = None, dropout = 0.0, recurrent_dropout = 0.0,
return_sequence= False)

### Embedding Layers

from keras.layers.embeddings import Embedding 
Embedding(input_dim, output_dim, embeddings_initializer = 'uniform', mask_zero = False)








