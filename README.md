# Positive Resampler using DNN
Author: Suyong Choi (Korea University)

Positive weight resampler using DNN for samples with negative sample weights. This can be useful if you are trying to use samples that have non-negative weights but need them to have positive values. Such cases arise in machine learning. 

In general, it is not possible to assign positive values to all the events. However, in high-energy physics, simulated events produced at next-to-leading order precision have negative weight events that have positive weight events nearby such that local average of the weight can be positive. Here, we assume that the local average weight is positive for the sample. In https://arxiv.org/abs/2005.09375, a positive resampler for binned data is introduced. However, for unbinned data, it cannot be used. Here, we turn the problem is turned into finding the weight <img src="https://latex.codecogs.com/svg.latex?\tilde{w}(\vec{x})\geq&space;0" title="\tilde{w}(\vec{x})\geq 0" /> as a function of the phase space variables.

<img src="https://latex.codecogs.com/svg.latex?\tilde{w}(\vec{x})\approx\frac{w_&plus;(\vec{x})P_&plus;(\vec{x})&space;&plus;&space;w_-(\vec{x})P_-(\vec{x})}{P_&plus;(\vec{x})&plus;P_-(\vec{x})}" title="\tilde{w}(\vec{x})\approx\frac{w_+(\vec{x})P_+(\vec{x}) + w_-(\vec{x})P_-(\vec{x})}{P_+(\vec{x})+P_-(\vec{x})}" />


The positivity of sample weights is imposed by using a softplus activation function at the output.
