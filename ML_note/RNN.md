## Markov Chain (MC) 

 Consider the variable ${\bf y_{(t)} }$ is the vector (state) at time $t$. The Markov chain has the following form: 

$$
{\bf y_{(t)} } = A {\bf y_{(t-1)} }
$$
where $A$ is the transition matrix. 

<img src="C:\Users\aeio6646\Desktop\ML_note\Figure\MC.png" alt="MC" style="zoom:60%;" />

## Hidden Markov Model (HMM)

Similar to Markov chain. The Hidden Markov model has an additional hidden vector (state):
$$
{\bf h_{(t)} } = A {\bf h_{(t-1)} }\\
{\bf y_{(t)} } = B {\bf y_{(t-1)}}
$$
where ${\bf h_{t} }$ is the "hidden" vector (state) at time $t$.

<img src="C:\Users\aeio6646\Desktop\ML_note\Figure\HMM.png" alt="HMM" style="zoom:60%;" />

## Recurrent Neural Network (RNN)

$$
{\bf h_{(t)} } = \sigma ({W\bf x_{(t)} }+U{\bf h_{(t-1)}}+{\bf b})\\
{\bf o_{(t)} } = \sigma (V{\bf h_{(t)}}+{\bf b})\\
$$

where ${\bf x_{i}}$ is the input, ${\bf o_{i}}$ is the output and $\sigma$ is the activation function.

<img src="C:\Users\aeio6646\Desktop\ML_note\Figure\RNN.png" alt="RNN" style="zoom:60%;" />

## Long Short-Term Memory (LSTM)

LSTM is the modified version of RNN, which additionally has memory cell state $c_t$. 
$$
c_{(t)}=f_{(t)} \cdot c_{(t-1)} + i_{(t)} \cdot \tilde{c}_{(t)}
$$
where $f_{t}$ is the forget gate, $i_t$ is the input gate and $\tilde{c_t}$ is the cell input.
$$
f_{(t)} = \sigma(W_f{\bf x_{(t)}}+U_f{\bf h_{(t-1)}}+{\bf b_f}) \\
i_{(t)} = \sigma(W_i{\bf x_{(t)}}+U_i{\bf h_{(t-1)}}+{\bf b_i}) \\
\tilde{c}_{(t)} = \sigma(W_c{\bf x_{(t)}}+U_c{\bf h_{(t-1)}}+{\bf b_c}) \\
$$
The hidden state $h_{(t)}$ and output $o_{(t)}$ are defined as
$$
h_{(t)}=o_t \cdot \sigma(c_{(t)}) \\
o_{(t)} = \sigma(W_o{\bf x_{(t)}}+U_o{\bf h_{(t-1)}}+{\bf b_o}) \\
$$
<img src="C:\Users\aeio6646\Desktop\ML_note\Figure\LSTM.png" alt="LSTM" style="zoom:60%;" />





