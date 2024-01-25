# Problem with Perceptron for XOR Operation

## Introduction

The perceptron is a simple binary classification algorithm that learns a linear decision boundary to separate two classes. However, the perceptron has limitations when it comes to solving certain problems, particularly those that are not linearly separable. One classic example of such a problem is the XOR (exclusive OR) operation.

## XOR Operation

The XOR operation is a binary operation that outputs true only when the number of true inputs is odd. The truth table for XOR is as follows:

| Input1 | Input2 | Output |
| ------- | ------- | ------ |
|    1    |    1    |    0   |
|    1    |    0    |    1   |
|    0    |    1    |    1   |
|    0    |    0    |    0   |

## Perceptron Model for XOR

We attempted to train three perceptron models (one each for OR, AND, and XOR) using the `sklearn` library. While the perceptron successfully learned the linear decision boundaries for the OR and AND operations, it failed to converge for the XOR operation.

### Model Parameters and Decision Boundaries

#### OR Operation
- Coefficients: [2.0, 2.0]
- Intercept: -1.0
- Decision Boundary:
![OR Decision Boundary](https://github.com/Kunal3012/Problem-with-Perceptron/blob/main/images/or.png)


#### AND Operation
- Coefficients: [2.0, 2.0]
- Intercept: -2.0
- Decision Boundary:   
![AND Decision Boundary](https://github.com/Kunal3012/Problem-with-Perceptron/blob/main/images/and.png)


#### XOR Operation
- Coefficients: [0.0, 0.0]
- Intercept: 0.0
- Decision Boundary:
![XOR Decision Boundary](https://github.com/Kunal3012/Problem-with-Perceptron/blob/main/images/xor.png)


## Problem with Perceptron for XOR

The perceptron's failure to learn the XOR operation can be visually understood by plotting the decision boundaries. The XOR operation requires a non-linear decision boundary, which cannot be achieved by a single perceptron with a linear activation function.


## Conclusion

The perceptron model, due to its linearity, is not suitable for solving problems that involve non-linear decision boundaries, such as the XOR operation. In cases like XOR, more complex models like multi-layer perceptrons (neural networks) with non-linear activation functions are required to capture and learn the intricate relationships within the data.

To address XOR-type problems, consider exploring more advanced machine learning models that can handle non-linearities effectively.  