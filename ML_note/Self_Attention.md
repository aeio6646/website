##### <a href='../note.html'>*Note*</a>

## Self-Attention

Self-attention is a kind of layer / mechanism which is widely used in NLP. It contains three kinds of components:
$$
q_{i} = W_{q}x_{i} \\
k_{i} = W_{k}x_{i} \\
v_{i} = W_{v}x_{i} \\
$$
where $q_{i}$ is query, $k_{i}$ is key and $v_{i}$ is value. The output $o_{i}$ is designed as:
$$
a_{j,i} = softmax\{\frac{k_{j}q_{i}}{\sqrt{d_k}}\} \\
o_{i} = \sum_j v_{j}a_{j,i} \\
$$
where $a_{j,i}$ is the "attention matrix", which means the relation between $v_{j}$ and $o_{i}$. This layer also can be written as matrix form so that the parallel computing is possible. 
$$
Q = W_{q}{\bf x} \\
K = W_{k}{\bf x} \\
V = W_{v}{\bf x} \\
A = softmax\{\frac{K^TQ}{\sqrt{d_k}}\} \\
{\bf o} = VA
$$
<img src="Figure\SA.png" alt="SA" style="zoom:60%;" />

For the multi-head self-attention, it has multiple query ($Q_{\alpha}$) / key ($K_{\alpha}$) / value ($V_{\alpha}$) and thus it has multiple outputs $O_{\alpha}$. The final output is the linear combination of multiple outputs: 
$$
O_{\alpha} = F^{self-attention}_{\alpha}({\bf x}) \\
O = \sum_\alpha w_{\alpha} O_{\alpha}
$$

## Positional Encoding



Truncated self-attention



