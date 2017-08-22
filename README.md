# learning ML

Notes for Udacity's Intro to Machine Learning Course
## Supervised learning
In supervised learning, we are provided with a set of training data, wherein each entry consistes 
of some elements describing that entry (features) and an output value (label) to which input elements
collectively belong. There are basically 3 supervised classification Algorithms:
 * Naive Bayes classifier
 * SVM (Support vector machines)
 * Decision Trees

## Problem of Overfitting
If we make our algorithm too strong (many polynomial features), it will be very sensitive to even small fluctuations in our training
set causing overfitting, i.e modelling the random noise instead of the intended outputs.
In overfitting, the decision boundary tends to become complex when a simple decision boundary is possible.
As in the following image, a simple linear decision boundary is possible but the algorithm
gave a complex one.

![under fitting and over fitting](https://i.stack.imgur.com/yhkx4.jpg)

## Decision Trees
Decision trees lets you do a non-linear decision making with simple linear decision surfaces.
for eg. in the below figure the red objects could be defined to belong to 2 linear surfaces:
x>=w10 and y >=w20
![decesion tree](https://image.slidesharecdn.com/lecture02ml4ltmarinasantini2013-130827052029-phpapp02/95/lecture-02-machine-learning-for-language-technology-decision-trees-and-nearest-neighbors-10-638.jpg?cb=1378716784)

the root if the tree consists of all the training examples. we keep breaking it into sub nodes each having a subset of it's parent's training examples.

Decision tree started code:
```
 from sklearn import tree
 # X is a an array with each index representing features for that data
 X = [[0, 0], [1, 1]]
 # each element in Y represents the label to which the corresponding element in X belongs
 Y = [0, 1]
 clf = tree.DecisionTreeClassifier()
 clf = clf.fit(X, Y)
 # below line will predict labels for the given features
 clf.predict([[2., 2.]])
```

prototype of the Decision tree classifer function :

```
DecisionTreeClassifier(criterion=’gini’, splitter=’best’, max_depth=None, min_samples_split=2, min_samples_leaf=1, min_weight_fraction_leaf=0.0, max_features=None, random_state=None, max_leaf_nodes=None, min_impurity_decrease=0.0, min_impurity_split=None, class_weight=None, presort=False)
```

the min_samples_split argument decides if we can split a node further or not. we can split 
only if the no of training examples in that node is greater than or equal to min_samples_split
the lower the value of this argument, the higher the chance of getting a overfitting decision
boundary because then the decision boundary will try to cover every input point (even if
it is far from all the other points) and thus making the decision boundary look complex.




## The above content is mainly derived from the following links

* [Intro to Machine Learning](https://in.udacity.com/course/intro-to-machine-learning--ud120/?) - Machine learning course for beginners by udacity
* [Scikit Documentation](http://scikit-learn.org/stable/index.html) - Scikit Library
<!--
## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

-->
## Authors

* **Nitin Kumar** - *Initial work* - [Github](https://github.com/Nitinkmr)

<!--
## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
-->
## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc
