---
layout: archive
title: "Side Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

_Last Updated 09/2022_

<div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <div style="flex: 0 0 300px;">
        <img src="/images/project-marl.png" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; font-size: 0.85em;">
        <h3>Multi-agent reinforcement learning using coordination graphs</h3>
        In this project (2021), we made a tutorial and blog post based on Sheng's work on multi-agent reinforcement learning using graph-based attention on a coordination graph of interacting agents. 

        <a href="https://medium.com/@jamgochian95/multi-agent-reinforcement-learning-with-coordination-graphs-428dddb99907">Blog Post</a> | <a href="https://colab.research.google.com/drive/1WAgfCL0HEb9u07JsmNXnx2vwt8TyPmX5">Tutorial Notebook</a> | <a href="https://arxiv.org/abs/2006.11438">Sheng's Paper</a>
    </div>
</div>

<div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <div style="flex: 0 0 300px;">
        <img src="/images/projects_covid19.png" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; font-size: 0.85em;">
        <h3>Covid-19 infection prediction modeling</h3>
        In this project (2021), we posited our own (convex) models to predict COVID-19 infections. We compared our models to regularized autogregressive moving average (also trained through convex optimization), along with a (non-convex) SIRD model trained through <a href="http://proceedings.mlr.press/v119/menda20a/menda20a.pdf">Certainty-Equivalent Expectation-Maximization</a>. We found that our models were (non-surprisingly) much faster to learn and all models were comparably poor at predicting COVID-19 infections. Turns out COVID-19 is quite hard to forecast.

        <a href="/files/projects-covid19.pdf">Paper</a> | <a href="https://github.com/jamgochiana/CovidModeling">Code</a>
    </div>
</div>

<div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <div style="flex: 0 0 300px;">
        <img src="/images/projects_diffqlearning.png" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; font-size: 0.85em;">
        <h3>Modified differential Q-Learning</h3>
        In this project (2021), we looked at <a href="http://proceedings.mlr.press/v139/wan21a/wan21a.pdf">differential Q-learning</a>, a variant of Q-learning which overcomes the need to introduce an artificial discount factor by keeping track of average reward and differentials instead of cumulative reward. We suggested a modification that kept track of additional differentials over state partitions, showing that if you had a problem where reward was amenable to state partitioning and did so smartly, you could learn better policies more quickly.

        <a href="/files/projects_diffqlearning.pdf">Paper</a>
    </div>
</div>

<div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <div style="flex: 0 0 300px;">
        <img src="/images/projects_metatimeseries.jpg" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; font-size: 0.85em;">
        <h3>Meta black-box time-series forecasting with external covariates</h3>
        In this project (2020), we tried to see if we could meta-learn how to make time-series predictions of electricity demand at new locations given little data at those locations (few-shot), but a lot of data at related locations. We put forward a method called TSMANN that built off of <a href="http://proceedings.mlr.press/v48/santoro16.pdf">Memory Augmented Neural Networks</a> but applied specifically to time-series forecasting with external covariates (e.g. weather information).

        <a href="/files/projects_metatimeseries.pdf">Paper</a>
    </div>
</div>

<div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <div style="flex: 0 0 300px;">
        <img src="/images/projects_bayesopt.png" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; font-size: 0.85em;">
        <h3>Hyperparameter tuning through Expected Improvement exploration</h3>
        In this project (2020), we wrote a library to do automatic hyperparameter tuning using Bayesian optimization with Expected Improvement exploration. There are better methods to do this nowadays, e.g. <a href="https://proceedings.neurips.cc/paper/2011/file/86e8f7ab32cfd12577bc2619bc635690-Paper.pdf">Tree Parzen estimators</a>, or <a href="http://proceedings.mlr.press/v80/falkner18a.html">BOHB</a>.

        <a href="/files/projects_bayesopt-2.pdf">Paper</a> | <a href="https://github.com/jamgochiana/GaussianProcessBandits.py">Code</a>
    </div>
</div>

<div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <div style="flex: 0 0 300px;">
        <img src="/images/projects_mcts.png" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; font-size: 0.85em;">
        <h3>Continuous action EV charge scheduling through Monte Carlo Tree Search</h3>
        In this project (2020), I tried to use Monte Carlo Tree Search to schedule electric vehicle charging given different probabilistic models of external electricity demand and non-convex charging dynamics. I handled the large continuous action and space spaces by using double progressive widening. I also compared using linear, feedforward neural network, and recurrent neural network models to do the single-step electricity demand prediction, while propagating appropriate information down through the tree search. I think now, the most efficient way to solve this problem may be using <a href="https://ieeexplore.ieee.org/abstract/document/7963253">multi-forecast (scenario-based) MPC</a> with sample-efficient methods to do the non-convex optimization, e.g. <a href="https://arc.aiaa.org/doi/pdf/10.2514/1.G001921">MPPI</a> or <a href="https://arxiv.org/abs/1604.00772">CMA-ES</a>.

        <a href="/files/projects_mcts.pdf">Paper</a>
    </div>
</div>

<div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <div style="flex: 0 0 300px;">
        <img src="/images/projects_bayesianrnn.png" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; font-size: 0.85em;">
        <h3>Bayesian probabilistic driver modeling</h3>
        In this project (2020), we developed a probabilistic driver prediction model based on real highway data for vehicles changing lanes. We captured different methods for capturing epistemic uncertainty, including probabilistic feedforward and recurrent neural networks, RNNs trained with <a href="http://proceedings.mlr.press/v37/blundell15.pdf">Bayes by Backprop</a>, and Bayesian RNNs with <a href="https://arxiv.org/pdf/1704.02798.pdf">posterior sharpening</a>. 

        <a href="/files/projects-bayesianrnn.pdf">Paper</a> | <a href="https://github.com/parachutel/bayes-by-backprop">Code</a>
    </div>
</div>

<div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <div style="flex: 0 0 300px;">
        <img src="/images/projects_gmphd.png" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; font-size: 0.85em;">
        <h3>GaussianFilters.jl</h3>
        We made a Julia library (2019) that implements a Kalman, Extended Kalman, and Unscented Kalman Filters with automatic differentiation to calulate dynamic and observation function Jacobians automatically. We also implemented the Probability Hypothesis Density filter for multi-target object tracking in cluttered environments.

        <a href="/files/projects_phd_filter.pdf">Paper</a> on the PHD filter | <a href="http://github.com/sisl/GaussianFilters.jl">Code</a>
    </div>
</div>

<div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <div style="flex: 0 0 300px;">
        <img src="/images/projects_3dnst-1.png" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; font-size: 0.85em;">
        <h3>3D neural style transfer</h3>
        In this project (2019), we attempted to apply Neural Style Transfer to images with depth channels, with the hopes of being able to blend the style transfer with the depth to make some cool pictures. We had some mixed success, a big problem being style itself is often 2D and doesn't blend well with depth. We still had some pretty cool pictures come out, and there are definitely better ways to do this nowadays.

        <a href="/files/projects_3dneuralstyletranser-2.pdf">Paper</a>
    </div>
</div>

<div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <div style="flex: 0 0 300px;">
        <img src="/images/projects-roboticautonomy.png" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; font-size: 0.85em;">
        <h3>Robotic autonomy</h3>
        For the Stanford robotic autonomy class (2019), we worked together to develop an autonomous software stack for a TurtleBot equipped with a camera and lidar. Our turtlebot operated autonomously in a real test environment while detecting signs and objects through its fast object recognition modules, mapping the environment with lidar SLAM, planning its path using RRT, and successfully navigating to different requested objects. 
    </div>
</div>

