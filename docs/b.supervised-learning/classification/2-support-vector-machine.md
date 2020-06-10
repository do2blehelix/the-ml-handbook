---
layout: default
title: Support Vector Machine
parent: Classification
grand_parent: Supervised Learning
nav_order: 2

---
### SVM (Support Vector Machine)![](https://lh5.googleusercontent.com/n0CPoXbAgg0MNx5jxNNmn14h-aWrPgVDUj4uo_6DqnUL4iRX7ZHTjl8GoDwXn1IWbp1743NgaDXva8rDUtac5oKaPdAZMbJ4qaOqNx23JVCZHwEOwyeLdizmFHJG57oHKNidmboV =308x209)

In this algorithm, each data item is plotted as a point in n-dimensional space (where n is the number of features you have) with the value of each feature being the value of a particular coordinate.

The aim is to determine the location of decision boundaries also known as hyperplane that produce the optimal separation of classes. Multiple frontiers are produced to suit the data. The best frontier is the one which is farthest away from the nearest support vector.

In case the data cannot be clearly segregated, the data is transformed to a higher dimensional plane where it can be segregated easily.

Classification Error : Split the data into 2, create boundary lines, classify anything between the margin as error, add errors.

Margin Error : Goal is to obtain a larger margin between the 2 boundary lines with lower error.

**Hyperparameters :**

C-parameter : It's just a constant that attaches itself to the classification error.

_Small c = large margin and some classification errors. Large c = classify well but small margin._

Kernel :

* Linear
* Polynomial Kernel :
  * Degree
* RBF (Radial Basis Functions) Kernel :
  * γ Parameter : small γ = wide curve / large γ = narrow curve

**SVMs can be implemented:**

* Maximum Margin Classifier : When your data can be completely separated, the linear version of SVMs attempts to maximize the distance from the linear boundary to the closest points (called the support vectors)

* Classification with Inseparable Classes :Data in the real world is rarely completely separable. For this reason, we introduced a new hyper-parameter called C. The C hyper-parameter determines how flexible we are willing to be with the points that fall on the wrong side of our dividing boundary. The value of C ranges between 0 and infinity. When C is large, you are forcing your boundary to have fewer errors than when it is a small value.

Note: when C is too large for a particular set of data, you might not get convergence at all because your data cannot be separated with the small number of errors allotted with such a large value of C.

* Kernel Methods : Kernels in SVMs allow us the ability to separate data when the boundary between them is nonlinear. Specifically, you saw two types of kernels: polynomial, rbf. By far the most popular kernel is the rbf kernel (which stands for radial basis function). The rbf kernel allows you the opportunity to classify points that seem hard to separate in any space. This is a density based approach that looks at the closeness of points to one another. This introduces another hyper-parameter gamma. When gamma is large, the outcome is similar to having a large value of C, that is your algorithm will attempt to classify every point correctly. Alternatively, small values of gamma will try to cluster in a more general way that will make more mistakes, but may perform better when it sees new data.

**Advantages** : Robust, accurate classification

**Disadvantages** : Computationally expensive
