---
layout: post
title: Diffusion Models; A Brief Report
date: 2025-11-15 16:40:16
description: A breif overview of diffusion models and the landscape they currently occupy.
tags: ML
categories: blog-reports
---


# Diffusion Models  

A diffusion model consists of a forwards process and a backwards process,
- Forwards Process:
	- Take a clean sample of the data and sequentially 'corrupt' (or perturbed), via [[Gaussian]] (random) noise
	- In the infinite-time limit, this corresponds to a transition to pure noise
	- Gaussian Transition Kernel
- Backwards Process:
	- Train a denoising [[Neural Network|NN]], that sequentially removes noise to return to the original data



### Sub-categories of diffusion models:
- [[DDPMs]] (Denoising Diffusion Probabilistic Models), non-equilibrium thermodynamics inspired. An extension of [[VAEs]], mirroring the encoding decoding process.
- [[NCSNs]] (Noise Conditioned Score Networks), train a shared [[Neural Network||NN]] utilising score matching 
	- What is score matching.... ???
- [[SDE - Diffusion Models]] ([[Stochastic Differential Equation]]) approach, seen as a generalisation of the above two, modelling using forwards and reverse SDEs
	- Is this quasi physical ????

[[Diffusion Models in Vision_ A Survey]]

## Forwards Process

Ornstein-Ulhenbeck process defined by the [[Stochastic Differential Equation|SDE]]
$$
dX_{t} = -\frac{1}{2}g(t)X_{t}dt + \sqrt{ g(t) }dW_{t} \quad \text{for} \quad g(t)>0
$$




## Section for Literature Review

#### Intro

The field of Diffusion Models is one that experienced rapid growth after conception in the works of Sohl-Dickstein et al. 2015 and Ho et al. 2020. 

The basic principle of q diffusion model is to sample some well know random distribution (e.g. Gaussian), and by sequentially removing noise with a function estimator (NN) that has been trained to sequentially remove noise towards our target data distribution.

Three subcategroies of diffusion models quickly arose these being, denoising diffusion probabilistic networks (DDPMs), score-based generative models (SGMs) and stochastic differential equation (SDEs).



#### Mathematical Preliminaries

**Forwards and Backwards Process**


**Conditional Diffusion Models**


#### DDPMs

[[Deep Unsupervised Learning using Nonequilibrium Thermodynamics]]
[[Denoising Diffusion Probabilistic Models]], 
#### SGMs



#### SDEs

[[Score-Based Generative Modeling through Stochastic Differential Equations]]




