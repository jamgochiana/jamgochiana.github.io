---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

_Last Updated 12/2022_

Constrained POMDP planning in continuous spaces
=====
![](/images/research_ccs.gif)

Rather than augmenting rewards with penalties for undesired behavior, Constrained Partially Observable Markov Decision Processes (CPOMDPs) plan safely by imposing inviolable hard constraint value budgets. Previous work performing online planning for CPOMDPs has only been applied to discrete action and observation spaces. In this work, we propose algorithms for online CPOMDP planning for continuous state, action, and observation spaces by combining dual ascent with progressive widening. We empirically compare the effectiveness of our proposed algorithms on continuous CPOMDPs that model both toy and real-world safety-critical problems. Additionally, we compare against the use of online solvers for continuous unconstrained POMDPs that scalarize cost constraints into rewards, and investigate the effect of optimistic cost propagation.

[Preprint](https://arxiv.org/abs/2212.12154) \| [Code](https://github.com/sisl/CPOMDPExperiments)


Meta-learning for system identification
=====
![](/images/research_metasysid.png)

In this paper, we propose Meta-SysId, a meta-learning approach to model sets of systems that have behavior governed by common but unknown laws and that differentiate themselves by their context. Inspired by classical modeling-and-identification approaches, Meta-SysId learns to represent the common law through shared parameters and relies on online optimization to compute system-specific context. Compared to optimization-based meta-learning methods, the separation between class parameters and context variables reduces the computational burden while allowing batch computations and a simple training scheme. We test Meta-SysId on polynomial regression, time-series prediction, model-based control, and real-world traffic prediction domains, empirically finding it outperforms or is competitive with meta-learning baselines.

[Preprint](https://arxiv.org/abs/2206.00694)

Safe heirarchical imitation learning for urban driving
=====
![](/images/research_shail.png)

Designing a safe and human-like decision-making system for an autonomous vehicle is a challenging task. Generative imitation learning is one possible approach for automating policy-building by leveraging both real-world and simulated decisions. Previous work that applies generative imitation learning to autonomous driving policies focuses on learning a low-level controller for simple settings. However, to scale to complex settings, many autonomous driving systems combine fixed, safe, optimization-based low-level controllers with high-level decision-making logic that selects the appropriate task and associated controller. In this paper, we attempt to bridge this gap in complexity by employing Safety-Aware Hierarchical Adversarial Imitation Learning (SHAIL), a method for learning a high-level policy that selects from a set of low-level controller instances in a way that imitates low-level driving data on-policy. We introduce an urban roundabout simulator that controls non-ego vehicles using real data from the Interaction dataset. We then show empirically that our approach can produce better behavior than previous approaches in driver imitation which have difficulty scaling to complex environments.

[Preprint](https://arxiv.org/abs/2204.01922) \| [Code](https://github.com/sisl/InteractionImitation) \| [Simulator](https://github.com/sisl/InteractionSimulator)

Game-theoretic planning for urban driving
=====
![](/images/research_decnash.png)

Safe navigation in dense, urban driving environments remains an open problem and an active area of research. Unlike typical predict-then-plan approaches, game-theoretic planning considers how one vehicle's plan will affect the actions of another. Recent work has demonstrated significant improvements in the time required to find local Nash equilibria in general-sum games with nonlinear objectives and constraints. When applied trivially to driving, these works assume all vehicles in a scene play a game together, which can result in intractable computation times for dense traffic. We formulate a decentralized approach to game-theoretic planning by assuming that agents only play games within their observational vicinity, which we believe to be a more reasonable assumption for human driving. Games are played in parallel for all strongly connected components of an interaction graph, significantly reducing the number of players and constraints in each game, and therefore the time required for planning. We demonstrate that our approach can achieve collision-free, efficient driving in urban environments by comparing performance against an adaptation of the Intelligent Driver Model and centralized game-theoretic planning when navigating roundabouts in the INTERACTION dataset. 

[Workshop paper](https://arxiv.org/abs/2201.0271) \| [Code](https://github.com/sisl/DecNashPlanning) \| [Simulator](https://github.com/sisl/InteractionSimulator)


POMDP planning for urban driving with occlusions
=====
![](/images/research_modia.png)

We present solutions for autonomous vehicles in limited visibility scenarios, such as traversing T-intersections, as well as detail how these scenarios can be handled simultaneously. The approach models each problem separately as a partially observable Markov decision process (POMDP). We propose an approach for integrating limited visibility within a POMDPs and implementing them on a physical robot. In order to address scalability challenges, we use a framework for multiple online decision-components with interacting actions (MODIA). We present the novel necessary architectural details to deploy MODIA on an actual robot. The entire approach is demonstrated on a fully operational autonomous vehicle prototype acting in the real world at two different T-intersections.

[Conference paper](https://ieeexplore.ieee.org/abstract/document/9419519/) \|
[Workshop paper](https://drive.google.com/file/d/1x1okLTMYdwALAdfYkeIO9IVVQXkuSa8d/view) \|
[Workshop video](https://www.youtube.com/watch?v=NojRqX3cIH4&feature=youtu.be)

Probabilistic multi-step time-series forecasting of energy demand
=====
![](/images/research_jdf-3.png)

Some real-world decision-making problems require making probabilistic forecasts over multiple steps at once. However, methods for probabilistic forecasting may fail to capture correlations in the underlying time-series that exist over long time horizons as errors accumulate. One such application is with resource scheduling under uncertainty in a grid environment, which requires forecasting electricity demand that is inherently noisy, but often cyclic. In this paper, we introduce the conditional approximate normalizing flow (CANF) to make probabilistic multi-step time-series forecasts when correlations are present over long time horizons. We first demonstrate our method's efficacy on estimating the density of a toy distribution, finding that CANF improves the KL divergence by one-third compared to that of a Gaussian mixture model while still being amenable to explicit conditioning. We then use a publicly available household electricity consumption dataset to showcase the effectiveness of CANF on joint probabilistic multi-step forecasting. Empirical results show that conditional approximate normalizing flows outperform other methods in terms of multi-step forecast accuracy and lead to up to 10x better scheduling decisions.

[Preprint](https://arxiv.org/abs/2201.02753) \| [Repository](https://github.com/sisl/JointDemandForecasting)

[Tutorial](https://colab.research.google.com/drive/1xA3x-hi2JpsuBuiZwkGDDLNl1iGefjvy) for probabilistic multi-step time-series forecasting with external covariates (application to energy demand forecasting).

Electric vehicle charge scheduling
=====
![](/images/research_evcharging-1.png)

With the penetration of electric vehicles in local markets, vehicle-induced electricity demand can cause power grid instability. Collaborative smart charging can help stabilize grid demand and mitigate those issues. This paper formulates charge scheduling when connected vehicles constitute a large portion of instantaneous demand. Allowing coordinated charging to sway electricity price, we formulate a multi-objective stochastic optimization problem to minimize cost while maximizing charge in each car. We model stochastic base electricity demand using a Gaussian Mixture Model (GMM) and solve the certainty-equivalent stochastic optimization problem. We then implement a stochastic model predictive control (SMPC) algorithm and compare performance between a naive policy, a certainty-equivalent optimized policy, and SMPC on a dataset derived from California ISO-serviced demand.

[Conference paper](https://ieeexplore.ieee.org/abstract/document/8965237/)