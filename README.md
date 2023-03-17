# Mnist-classification-with-NN
simple Neural Network applied to a well known mnist dataset.
After loading the mnist dataset, We normalize the input in the range [0,1]

The output of the network will be a proability distribution over the different categories. Similarly, we generate a ground truth distribution, and the training objective will consist in minimizing their distance (categorical crossentropy). The ground truth distribution is the so called "categorical" distribution: if x has label l, the corresponding categorical distribution has probaility 1 for the category l, and 0 for all the others.

Our first Netwok just implements logistic regression

Now we need to compile the network. In order to do it, we need to pass two mandatory arguments:
the optimizer, in charge of governing the details of the backpropagation algorithm
the loss function

 A choose is Adam optimizer, implementing an adaptive lerning rate, with momentum

Optionally, we can specify additional metrics, mostly meant for monitoring the training process.

Finally, we fit the model over the trianing set.
Fitting, just requires two arguments: training data e ground truth, that is x and y. Additionally we can specify epochs, batch_size, and many additional arguments.
In particular, passing validation data allow the training procedure to measure loss and metrics on the validation set at the end of each epoch.
