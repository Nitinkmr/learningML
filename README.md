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

Decision tree started code:
```
 from sklearn import tree
 # X is a an array with each index representing features for that data
 X = [[0, 0], [1, 1]]
 # each element in Y represents the label to which the corresponding element in X belongs
 Y = [0, 1]
 clf = tree.DecisionTreeClassifier()
 clf = clf.fit(X, Y)
```

### Installing

A step by step series of examples that tell you have to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc
