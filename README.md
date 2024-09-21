

# Deep Learning Models for Causal Inference (under selection on observables)

### <span style="color:red">UPDATE 09/30/2023</span>: The [paper](https://osf.io/preprints/socarxiv/aeszf) is forthcoming in Sociological Methods & Research.

While there is a lot of interest in using causal inference to improve deep learning, there aren't many examples of how deep learning can be used to estimate causal effects. This repository contains extensive tutorials for building deep learning models to do causal estimation under selection on observables.

I tried to write the tutorials at a very high level so that anybody with a basic understanding of causal inference and machine learning could find them useful. The tutorials assume very little prior knowledge about deep learning and TensorFlow. In addition to featuring relevant models, I hoped that these tutorials could be a gentle introduction for building, tuning, and evaluating your own complex models in Tensorflow 2.

*These are a work in a progress.* If you have any questions or feedback on how I can improve them, please let me know. The tutorials accompany a review we are currently writing on this literature. **Lastly, if you enjoyed these tutorials, feel free to star the repository.** Thanks!

### [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Zx0AkriygB_ws6qXjA7VfqebG-YMwbWl?usp=sharing) 1. Introduction to Deep Learning for Causal Inference on Observables. [SHORT]
#### (For those already familar with Tensorflow)
This tutorial introduces the idea of representation learning for causal inference. You also build and test a simple conditional average treatment effect (CATE) estimator, TARNet (first introduced in [Shalit et al., 2017](http://proceedings.mlr.press/v70/shalit17a.html)), using the TF2 functional API.

### [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1zLCWcYChBN33wvZhRw9cB_ZFk-JT3HEZ?usp=sharing) 1. Introduction to Deep Learning for Causal Inference on Observables. [LONG]
#### (For those with no prior DL experience)
This tutorial is an "unabridged" version of the above for those who have never done any DL and may find TF overwhelming. It introduces S-learners, and T-learners before TARNet as a way to get familiar with building custom Tensorflow models.

### [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1MBUkQO7rh89JrlAV0p1aLNoF9CIB3rZZ?usp=sharing) 2. Causal Inference Metrics and Hyperparameter Optimization.
Because we do not observe counterfactual outcomes, it's not obvious how to optimize supervised learning models for causal inference. This tutorial introduces some metrics for evaluating model performance. In the first part, you learn how to assess performance on these metrics in Tensorboard. In the second part, we hack [Keras Tuner](https://keras-team.github.io/keras-tuner/) to do hyperparameter optimization for TARNet, and discuss considerations for training models as estimators rather than predictors.

### [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1XzyOINgdSr78_KT7HJRJn07AwkHh-fG8?usp=sharing) 3. Semi-parametric extensions to TARNet 
This tutorial highlights some semi-parametric extensions to TARNet featured in [Shi et al., 2020](https://papers.nips.cc/paper/2019/file/8fb5f8be2aa9d6c64a04e3ab9f63feee-Paper.pdf). We add treatment modeling to our TARNet model and build an augmented inverse propensity score estimator. We then briefly describe the algorithm for Targeted Maximum Likelihood Estimation to introduce and build a TARNet with Shi et al.'s Targeted Regularization.   

 ### [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1NHYTbvGq-cWyy-mm0TrBH2rAmMqtcgPJ?usp=sharing) 4. Uncertainty and Interpretation. [IN PROGRESS]
This tutorial reimplements Dragonnet in Pytorch and shows how to calculate asymptotically-valid confidence intervals for the average treatment effect. We also interpret the features contributing to different heterogeneous CATEs using Integrated Gradients and SHAP scores. This is also a good tutorial if you also just want to learn how to interpret SHAP scores, independent of the context of causal inference.

 ### [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1phpoNEdvDgipCZCnpfvPC5anuIuodKB6?usp=sharing) 5. Using Integral Probability Metrics for Causal Inference [OPTIONAL]
 This tutorial features the Counterfactual Regression Network (CFRNet) and propensity-weighted CFRNet featured in [Shalit et al., 2017](http://proceedings.mlr.press/v70/shalit17a.html), [Johannson et al. 2018](https://arxiv.org/abs/1802.08598), [Johannson et al. 2020](https://arxiv.org/abs/2001.07426). This approach relies on Integral Probability Metrics (e.g. the MMD and Wasserstein distance used in GANs) to bound the counterfactual prediction loss and force the treated and control distributions closer together. The weighted variant adds adaptive propensity-based weights that provide a consistency guarantee, relax overlap assumptions, and ideally reduce bias.   
 

