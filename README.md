<img src="https://github.com/jmschrei/pomegranate/blob/master/docs/logo/pomegranate-logo.png" width=300>

[![Build Status](https://travis-ci.org/jmschrei/pomegranate.svg?branch=master)](https://travis-ci.org/jmschrei/pomegranate) ![Build Status](https://ci.appveyor.com/api/projects/status/github/jmschrei/pomegranate?svg=True) [![Documentation Status](https://readthedocs.org/projects/pomegranate/badge/?version=latest)](http://pomegranate.readthedocs.io/en/latest/?badge=latest)

*NOTE: pomegranate does not yet work with networkx 2.0. If you have problems, please downgrade networkx and try again.*

[JMLR-MLOSS Manuscript](http://jmlr.org/papers/volume18/17-636/17-636.pdf) Please consider citing it if you used it in your academic work.

pomegranate is a package for probabilistic and graphical models for Python, implemented in cython for speed. It grew out of the [YAHMM](https://github.com/jmschrei/yahmm) package, where many of the components of a hidden Markov model could be re-arranged to form other probabilistic models. It currently supports:

* [Probability Distributions](http://pomegranate.readthedocs.io/en/latest/Distributions.html)
* [General Mixture Models](http://pomegranate.readthedocs.io/en/latest/GeneralMixtureModel.html)
* [Hidden Markov Models](http://pomegranate.readthedocs.io/en/latest/HiddenMarkovModel.html)
* [Naive Bayes and Bayes Classifiers](http://pomegranate.readthedocs.io/en/latest/NaiveBayes.html)
* [Markov Chains](http://pomegranate.readthedocs.io/en/latest/MarkovChain.html)
* [Discrete Bayesian Networks](http://pomegranate.readthedocs.io/en/latest/BayesianNetwork.html)

The discrete Bayesian networks also support novel work on structure learning in the presence of constraints through a constraint graph. These constraints can dramatically speed up structure learning through the use of loose general prior knowledge, and can frequently make the exact learning task take only polynomial time instead of exponential time. See the [PeerJ manuscript](https://peerj.com/articles/cs-122/) for the theory and the [pomegranate tutorial](https://github.com/jmschrei/pomegranate/blob/master/tutorials/Tutorial_4b_Bayesian_Network_Structure_Learning.ipynb) for the practical usage! 

To support the above algorithms, it has efficient implementations of the following:

* Kmeans
* Factor Graphs

It currently supports the following features:

* [Multi-threaded Training](http://pomegranate.readthedocs.io/en/latest/parallelism.html)
* [BLAS/GPU Acceleration](http://pomegranate.readthedocs.io/en/latest/gpu.html)
* [Out-of-Core Learning](http://pomegranate.readthedocs.io/en/latest/ooc.html)
* [Minibatch Learning](http://pomegranate.readthedocs.io/en/latest/minibatch.html)
* [Semi-supervised Learning](http://pomegranate.readthedocs.io/en/latest/semisupervised.html)
* [Missing Value Support](http://pomegranate.readthedocs.io/en/latest/nan.html)
* [Customized Callbacks](http://pomegranate.readthedocs.io/en/latest/callbacks.html)

Please take a look at the [tutorials folder](https://github.com/jmschrei/pomegranate/tree/master/tutorials), which includes several tutorials on how to effectively use pomegranate!

See [the website](http://pomegranate.readthedocs.org/en/latest/) for extensive documentation, API references, and FAQs about each of the models and supported features.

No good project is done alone, and so I'd like to thank all the previous contributors to YAHMM, and all the current contributors to pomegranate, including the graduate students who share my office I annoy on a regular basis by bouncing ideas off of.

### Dependencies

pomegranate requires:

```
- Cython (only if building from source)
- NumPy
- SciPy
- NetworkX
- joblib
```

To run the tests, you also must have `nose` installed.

### User Installation

pomegranate is pip installable using `pip install pomegranate` and conda installable using `conda install pomegranate`. If that does not work, more detailed installation instructions can be found [here](http://pomegranate.readthedocs.io/en/latest/install.html).

## Contributing

If you would like to contribute a feature then fork the master branch (fork the release if you are fixing a bug). Be sure to run the tests before changing any code. You'll need to have [nosetests](https://github.com/nose-devs/nose) installed. The following command will run all the tests:

```
python setup.py test
```

Let us know what you want to do just in case we're already working on an implementation of something similar. This way we can avoid any needless duplication of effort. Also, please don't forget to add tests for any new functions.

