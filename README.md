# Evaluation of Resilience in Neural Networks using MILP
This work is based on the Paper [Maximum Resilience of Artificial Neural Networks](https://arxiv.org/abs/1705.01040) released in July 2017.

In general the performance of a Neural Network is meassured by using a Testset. This gives a feeling about the general quality of such a Model but makes no conclusion about certain conditions.
The approach used in the two given Jupyther Notebooks uses Integer Linear Programming to make mathematicaly conclusions about the existens or absence of certain behaviours.

## mnist+resilience.ipynb
For this piece of applied a Neural Network with one hidden Layer (45 Nodes) with ReLu and Softmax on the output Layer. It reaches a accuracy of 97% with the MNIST dataset.
Choosen one correct predicted image with high probability, ILP (Gurobi) is used to calculate the minimal required distortion so that the same Model predicts wrongly.

## deeptraffic+resilience.ipynb
Here I trained another Model to run the MIT Deeptraffic competition.
With the same ILP approach I proved the existance of situation in which the Model would steer the car into the sidelanes or other obstacles.
The Deeptraffic simulation generates random traffic conditions but might not generate such conditions ever.

## Conclusion
The approach of using ILP or MILP to validate the resilience of Neural Networks and other ML models has a huge potential.
In the covered cases I used pretty small Models. More complex Models such as ConvNets can not be computet with this technology.
This leads to the conclusion that ILP Optimization can be used for small Models.
