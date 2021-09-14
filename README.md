# Positive Resampler
Author: Suyong Choi (Korea University)

Positive weight resampler using DNN for samples with negative sample weights. This can be useful if you are trying to use samples that have non-negative weights but need them to have positive values. Such cases arise in machine learning. 

In general, it is not possible to assign positive values to all the events. However, in high-energy physics, simulated events produced at next-to-leading order precision have negative weight events that have positive weight events nearby such that local average of the weight can be positive. Here, we assume that the local average weight is positive for the sample. In https://arxiv.org/abs/2005.09375, a positive resampler for binned data is introduced. For unbinned data, it cannot be used. Here, we turn the problem is turned into finding the weight <img src="https://latex.codecogs.com/svg.latex?w(\vec{x})" title="w(\vec{x})" /> as a function of the phase space variables.

<img src="https://latex.codecogs.com/svg.latex?\tilde{w}(\vec{x_0})=\frac{\int&space;w(\vec{x})P(\vec{x},\vec{x_0})&space;d^n&space;x}{\int&space;P(\vec{x},\vec{x_0})&space;d^n&space;x}" title="\tilde{w}(\vec{x_0})=\frac{\int w(\vec{x})P(\vec{x},\vec{x}_0) d^n x}{\int P(\vec{x},\vec{x_0}) d^n x}" />

The <img src="https://latex.codecogs.com/gif.latex?P(\vec{x},\vec{x}_0)" title="P(\vec{x},\vec{x}_0)" /> is local weighting function. It is not specified explicitly in this resampler, but is implicit in this method.

The positivity of sample weights is imposed by using a softplus activation function at the output.
