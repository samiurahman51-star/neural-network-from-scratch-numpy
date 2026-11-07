# neural-network-from-scratch-numpy
A neural network built from scratch in NumPy: dense layers, ReLU, Softmax, cross-entropy loss, backpropagation, L1/L2 regularization, dropout, and SGD, Adagrad, RMSprop and Adam optimizers. Learning project based on the book “Neural Networks from Scratch in Python”

## What is in the notebook

- **Layers:** dense (fully connected) layer with forward and backward passes, and dropout
- **Activations:** ReLU, Softmax, Sigmoid
- **Loss:** categorical cross-entropy, plus the combined Softmax + cross-entropy backward pass
- **Regularization:** L1 and L2 penalties on weights and biases, and dropout
- **Optimizers:** SGD (with learning rate decay and momentum), Adagrad, RMSprop, Adam
- **Training:** a 3-class spiral dataset, with a separate validation set

## Result

The network has one hidden layer of 512 neurons. I trained it for 10,000 epochs with Adam, L2 regularization and dropout.

| Dataset | Accuracy |
|---|---|
| Training | 88.3% |
| Validation (new spiral data) | 79.7% |

I also checked that the combined Softmax + cross-entropy gradient matches the separate Softmax and loss gradients. The combined version is about 13 times faster in my timing test.

## How to run

```bash
pip install numpy nnfs jupyter
jupyter notebook neural_network_from_scratch.ipynb
```

`nnfs` is used only to generate the spiral dataset and set the random seed.

## Notes

- This is a learning project on a small synthetic dataset. It is not a research result.
- The gap between training and validation accuracy shows some overfitting. More regularization or more data would be the next thing to try.
- Next step: apply the same ideas to real geotechnical data, such as jute geotextile test results, and compare against simpler models like linear regression.

## About

Md. Samiur Rahman Surid, Civil Engineering graduate (BUET), Geotechnical Engineering. I am teaching myself machine learning and neural networks to use them in geotechnical research.
