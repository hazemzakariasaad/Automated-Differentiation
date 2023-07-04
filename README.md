# Automated Differentiation

This project implements automated differentiation, a technique used in computational graph-based frameworks for automatic calculation of derivatives. The provided code defines a `comp_node` class that represents nodes in a computation graph and enables automatic calculation of gradients using the backpropagation algorithm.

## Key Features

- **Mathematical Operations:** The `comp_node` class overloads various mathematical operators such as addition, subtraction, multiplication, division, and power to perform element-wise computations between nodes.
- **Trigonometric Functions:** The class also provides support for trigonometric functions like sine and cosine.
- **Gradient Calculation:** The `backward()` method is implemented for each node to compute gradients using the backpropagation algorithm. The gradients can be accessed through the `grad` attribute of each node.
- **Loss Function Graph:** The `loss_graph()` function constructs a computation graph for a given loss function. It takes input nodes (`xp` and `yp`), data inputs (`datax` and `datay`), and constructs a graph to calculate the loss and other intermediate values.
- **Example Usage:** The provided code demonstrates an example usage scenario by creating a loss function graph and computing the gradients for the nodes in reverse topological order.

## Usage

To use the automated differentiation functionality:

1. Define and manipulate instances of the `comp_node` class to perform mathematical operations and construct computation graphs.
2. Use the provided mathematical operators (`+`, `-`, `*`, `/`, `**`) and trigonometric functions (`sin`, `cos`) to create expressions and perform computations.
3. Construct a computation graph using the `loss_graph()` function by specifying input nodes (`xp` and `yp`) and data inputs (`datax` and `datay`).
4. Access the computed loss value and intermediate nodes from the graph.
5. Set the `grad` attribute of the desired output node(s) to the appropriate value(s) to initiate the backpropagation process.
6. Call the `backward()` method on each node in reverse topological order to calculate the gradients using the backpropagation algorithm.
7. Access the gradients through the `grad` attribute of each node for further analysis or optimization.

Please note that this implementation provides a basic framework for automated differentiation and can be extended or customized based on specific requirements and use cases.

## Acknowledgments

- I would like to express my gratitude to my university and the professors who taught the concepts of automated differentiation during the lectures.
