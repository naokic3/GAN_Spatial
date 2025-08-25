---
title: Graph Neural Networks for Spatial Causal Analysis
authors:
  - name: Naoki Conning
    affiliations:
      - Stuyvesant High School

numbering: 
  headings: true
  math: true
  figure:
    continue: true

bibliography:
  - crime.bib

exports:
  - format: tex
    template: lap
---


+++{"part": "abstract"}
 This paper presents a novel approach to spatial causal analysis using Graph Neural Networks (GNNs). By leveraging the structural information inherent in spatial data, GNNs can effectively model complex relationships and dependencies between spatial units. We demonstrate the efficacy of our approach through a series of experiments on real-world datasets, highlighting its potential to advance the field of spatial econometrics.
+++

## Introduction





- "The weights matrix should bear a direct relationship to a theoretical conceptualization of the structure of dependence, rather than reflecting an ad hoc description of spatial pattern [@anselin1988]."

(SR_section)=
## Spatial Regression

$$
\label{eq_splag}
\Delta P_{i,t} = \alpha + \rho W \Delta P_{j,t} + \beta X_{i,t} + \epsilon_{i,t}
$$



- heteroskedasticity
- Error autocorrelation
  - spatial correlated errors
  - omitted lagged variable  (might explain spatial dependence)



The spatial lag equation [](#eq_splag)


## The choice of Spatial Weight Matrix

Network structure spillover

In spatial regression, the choice of spatial weight matrix \( W \) is crucial as it defines the spatial relationships between different regions. Common choices for \( W \) include:

1. **Contiguity-based weights**: These weights are based on the physical adjacency of regions. If two regions share a boundary, they are considered neighbors and receive a weight of 1; otherwise, the weight is 0.

2. **Distance-based weights**: In this approach, weights are assigned based on the distance between regions. Closer regions receive higher weights, while those farther away receive lower weights. This can be implemented using a decay function.

```{figure} ../figures/edens2000.png
:label: map1
:width: 700px
:align: center
County Population density
```

## A Graph Attention Autoencoder

Graph Attention Autoencoders (GAEs) are a type of neural network architecture designed to work with graph-structured data. They leverage attention mechanisms to focus on the most relevant parts of the graph, allowing for more effective learning and representation of complex relationships. In the context of spatial regression, GAEs can be used to model the spatial dependencies captured by the weight matrix \( W \).


As laid out in [](#SR_section) on Spatial Regression...

## Application to Crime

## Data and methods

See [](#map1) for a spatial distribution.


OLS
Spatial Lag Model (SLM)  with contiguity-based weights
Spatial Error Model (SEM)
Spatial Durbin Model (SDM)

## Construction Graph Auto Encoder 

The Construction Graph Auto Encoder (GAA) is designed to learn a low-dimensional representation of the spatial structure in the data. It does this by encoding the graph's topology and the features of its nodes into a latent space, which can then be used for various downstream tasks, such as regression or classification.

The GAA consists of two main components:


### Analysis

Spatial spillover


## Conclusion

See [@anselin2000] for more information on spatial regression.



List of Figures

- County Crime Data Visualization
- Focused network edge visualization
- Spatial spillover contiguity vs. GAA

