# PositiveResampler

Positive weight resampler using DNN for samples with negative sample weights. This can be useful if you are trying to have non-negative sample weights. Similar in spirit to https://arxiv.org/abs/2005.09375, which is a binned version. Using DNN, positive weight is obtained by implicit local averaging of weights.
