# Training a Sigmoid Neuron from Scratch

## Objective

Demonstrate the calculations involved in training a single artificial neuron using NumPy, without a neural-network training framework.

## Model

The neuron calculates a weighted sum of its inputs, adds a bias, and applies the sigmoid activation function.

The training examples contain four binary input patterns. Their target outputs correspond to the first input feature.

## Training Method

The notebook:

1. Initializes weights and bias using a fixed random seed.
2. Calculates predictions with a forward pass.
3. Measures mean squared error.
4. Computes gradients using the sigmoid derivative and the chain rule.
5. Updates weights and bias using gradient descent.

Training runs for 500 iterations with a learning rate of 1.0.

## Outputs

The notebook prints:
- Training loss every 100 iterations.
- Final continuous predictions.
- Rounded binary predictions.
- Learned weights and bias.

The results demonstrate fitting the four training examples; no separate evaluation dataset is used.

## Run

Open [sigmoid_neuron_training.ipynb](sigmoid_neuron_training.ipynb) in Google Colab and run the cell.

The only dependency is NumPy.
