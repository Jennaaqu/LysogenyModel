---
layout: default
title: Approach
nav_order: 4
---

## 1. Initial Elements

We build a dynamic mechanistic model that includes the main biological mechanisms in the system under study:

$$
\begin{align*} 
\frac{dL}{dt}&=\underbrace{r\bigg(1 - \frac{L}{K}\bigg)}_{\text{Logistic growth}} - \underbrace{\mu_i L}_{\text{Induction}} - \underbrace{\delta dT}_{\text{Infection}}& \\
\frac{dT}{dt}&=\underbrace{\mu_i L}_{\text{Induction}} - \underbrace{m T}_{\text{Decay}} - \underbrace{d TL}_{\text{Infection}}&
\end{align*} $$

This model assumes the existence of two bioagents (Lysogens and Temperate phages) that can undergo the following processes: Lysogen logistic growth, lysogen induction, lysogen reinfection, viral burst, and viral decay. As a first approximation, let us assume that lysogens are totally immune against infections ($$\delta=0$$). This yields the simplified model:

$$
\begin{align*} 
\frac{dL}{dt}&=\underbrace{r\bigg(1 - \frac{L}{K}\bigg)}_{\text{Logistic growth}} - \underbrace{\mu_i L}_{\text{Induction}}& \\
\frac{dT}{dt}&=\underbrace{\mu_i L}_{\text{Induction}} - \underbrace{m T}_{\text{Decay}}&
\end{align*}$$

The processes considered in the model are controlled by the parameters shown in this table:

| Parameter | Description | Value| Source|
| ----------- | ----------- | ----------- | ----------- |
| r | Maximum Growth Rate |0.471 (wild type), 0.382 (spot- mutant)  | Experiment data |
| K | Carrying capacity |8.2x10 7 (Wild type), 1x10 8 (mutant)  | Concentrations of bacteria at the end of the experiments without CX  |
| $$\mu_i$$ | Induction rate |spoT-: 8.481e-12, WT + CX: 5.793e-09, spoT- + CX: 1.814e-09, WT: 3.993e-11 | Experiment results  |
| $$\delta$$ | Probability of lysogen infection | 0 |  |
| d | Infection rate | 0 |  |
| c | Burst size | 125 |Da. Paepe et al, 2006  |
| m | Decay rate | 0.012h<sup>-1</sup>| Da Paepe et al, 2006  |

Our first step will be to try to fit the experimental data to this model.