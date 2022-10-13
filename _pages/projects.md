---
layout: archive
title: "Miscellaneous Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

_Last Updated 09/2022_

Multi-agent reinforcement learning using coordination graphs 
=====
![](/images/project-marl.png)

In this project (2021), we made a tutorial and blog post based on Sheng's work on multi-agent reinforcement learning using graph-based attention on a coordination graph of interacting agents. 

[Blog Post](https://medium.com/@jamgochian95/multi-agent-reinforcement-learning-with-coordination-graphs-428dddb99907) \| [Tutorial Notebook](https://colab.research.google.com/drive/1WAgfCL0HEb9u07JsmNXnx2vwt8TyPmX5) \| [Sheng's Paper](https://arxiv.org/abs/2006.11438) 

Covid-19 infection prediction modeling
=====
![](/images/projects_covid19.png)

In this project (2021), we posited our own (convex) models to predict COVID-19 infections. We compared our models to regularized autogregressive moving average (also trained through convex optimization), along with a (non-convex) SIRD model trained through [Certainty-Equivalent Expectation-Maximization](http://proceedings.mlr.press/v119/menda20a/menda20a.pdf). We found that our models were (non-surprisingly) much faster to learn and all models were comparably poor at predicting COVID-19 infections. Turns out COVID-19 is quite hard to forecast.

[Paper](/files/projects-covid19.pdf) \| [Code](https://github.com/jamgochiana/CovidModeling)

Modified differential Q-Learning
=====
![](/images/projects_diffqlearning.png)

In this project (2021), we looked at [differential Q-learning](http://proceedings.mlr.press/v139/wan21a/wan21a.pdf), a variant of Q-learning which overcomes the need to introduce an artificial discount factor by keeping track of average reward and differentials instead of cumulative reward. We suggested a modification that kept track of additional differentials over state partitions, showing that if you had a problem where reward was amenable to state partitioning and did so smartly, you could learn better policies more quickly.

[Paper](/files/projects_diffqlearning.pdf)

Meta black-box time-series forecasting with external covariates
=====
![](/images/projects_metatimeseries.jpg)

In this project (2020), we tried to see if we could meta-learn how to make time-series predictions of electricity demand at new locations given little data at those locations (few-shot), but a lot of data at related locations. We put forward a method called TSMANN that built off of [Memory Augmented Neural Networks](http://proceedings.mlr.press/v48/santoro16.pdf) but applied specifically to time-series forecasting with external covariates (e.g. weather information).

[Paper](/files/projects_metatimeseries.pdf)


Hyperparameter tuning through Expected Improvement exploration
=====
![](/images/projects_bayesopt.png)

In this project (2020), we wrote a library to do automatic hyperparameter tuning using Bayesian optimization with Expected Improvement exploration. There are better methods to do this nowadays, e.g. [Tree Parzen estimators](https://proceedings.neurips.cc/paper/2011/file/86e8f7ab32cfd12577bc2619bc635690-Paper.pdf), or [BOHB](http://proceedings.mlr.press/v80/falkner18a.html).

[Paper](/files/projects_bayesopt-2.pdf) \| [Code](https://github.com/jamgochiana/GaussianProcessBandits.py)

Continuous action EV charge scheduling through Monte Carlo Tree Search
=====
![](/images/projects_mcts.png)

In this project (2020), I tried to use Monte Carlo Tree Search to schedule electric vehicle charging given different probabilistic models of external electricity demand and non-convex charging dynamics. I handled the large continuous action and space spaces by using double progressive widening. I also compared using linear, feedforward neural network, and recurrent neural network models to do the single-step electricity demand prediction, while propagating appropriate information down through the tree search. I think now, the most efficient way to solve this problem may be using [multi-forecast (scenario-based) MPC](https://ieeexplore.ieee.org/abstract/document/7963253) with sample-efficient methods to do the non-convex optimization, e.g. [MPPI](https://arc.aiaa.org/doi/pdf/10.2514/1.G001921) or [CMA-ES](https://arxiv.org/abs/1604.00772).

[Paper](/files/projects_mcts.pdf)

Bayesian probabilistic driver modeling
=====
![](/images/projects_bayesianrnn.png)

In this project (2020), we developed a probabilistic driver prediction model based on real highway data for vehicles changing lanes. We captured different methods for capturing epistemic uncertainty, including probabilistic feedforward and recurrent neural networks, RNNs trained with [Bayes by Backprop](http://proceedings.mlr.press/v37/blundell15.pdf), and Bayesian RNNs with [posterior sharpening](https://arxiv.org/pdf/1704.02798.pdf). 

[Paper](/files/projects-bayesianrnn.pdf) \| [Code](https://github.com/parachutel/bayes-by-backprop)

GaussianFilters.jl
=====
![](/images/projects_gmphd.png)

We made a Julia library (2019) that implements a Kalman, Extended Kalman, and Unscented Kalman Filters with automatic differentiation to calulate dynamic and observation function Jacobians automatically. We also implemented the Probability Hypothesis Density filter for multi-target object tracking in cluttered environments.

[Paper](/files/projects_phd_filter.pdf) on the PHD filter \| [Code](http://github.com/sisl/GaussianFilters.jl)


3D neural style transfer
=====

![](/images/projects_3dnst-1.png)

In this project (2019), we attempted to apply Neural Style Transfer to images with depth channels, with the hopes of being able to blend the style transfer with the depth to make some cool pictures. We had some mixed success, a big problem being style itself is often 2D and doesn't blend well with depth. We still had some pretty cool pictures come out, and there are definitely better ways to do this nowadays.

[Paper](/files/projects_3dneuralstyletranser-2.pdf)

Robotic autonomy 
=====

![](/images/projects-roboticautonomy.png)

For the Stanford robotic autonomy class (2019), we worked together to develop an autonomous software stack for a TurtleBot equipped with a camera and lidar. Our turtlebot operated autonomously in a real test environment while detecting signs and objects through its fast object recognition modules, mapping the environment with lidar SLAM, planning its path using RRT, and successfully navigating to different requested objects. 

