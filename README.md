# nn_from_scratch
3-layer neural network for handwritten digit classification translated from Andrew Ng coursera assignment in MATLAB.

Layers:

    Input Layer: 400 input unit for 20x20 unrolled image + 1 bias unit

    Hidden Layer: 25 hidden units + 1 bias unit

    Output Layer: 10 output units used for classification [0->9]

Data:

    x.csv -> shape[5000x400); 5000 examples of 20x20 pixel handwritten digits
    
    y.csv -> shape[5000x1]; class label for each example
    
    theta1.csv -> shape[25x401]; optimized weights from input to hidden layer
    
    theta2.csv -> shape[10x26]; optimized weights from hidden layer to output

The program will generate random initial weight matrices and optimize their values by minimizing the neural network cost function. The optimizer uses weight gradients computed using backpropagation. The optimizing algorithm is from scipy optimization library called Newton Conjugate Gradient, and it runs for 200 iterations. Data is shuffled and split 80% into training and 20% into test data. The program will output the model accuracy on the training data and the visualization of the activation of each the hidden layer units.
