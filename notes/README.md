From __Probabilistic Machine Learning: An Introduction__ _(Kevin Murphy, 2021)_:
> $$y_i = Attn(x_i, (x_1, x_1), ..., (x_n, x_n))$$
where the query is $$x_i$$, and the keys and values are all the (valid) inputs $$x_1,..., x_n$$.

To use this in a decoder, we can set $$x_i = y_i-1$$, and $$n = i - 1$$, so all the previously generated outputs are avaialble. At training time, all the outputs are already known, so we can evaluate the above function in parallel, overcoming the sequential bottleneck of using RNNs.
