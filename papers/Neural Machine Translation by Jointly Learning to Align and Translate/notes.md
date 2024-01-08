*3rd Jan 2024, Phong Nguyen*

<div>
<p align="center">
  <img src="figure1.png" style="width:800px"/>
</p>

<a href='https://arxiv.org/abs/1411.4555'><img src='https://img.shields.io/badge/dynamic/json?url=https://api.semanticscholar.org/graph/v1/paper/fa72afa9b2cbc8f0d7b05d52548906610ffbb9c5?fields=citationCount&query=citationCount&label=ICLR%202015&prefix=citation%20'/></a>

</div>

- The first paper to propose **attention** mechanism for natural language processing, with a different name - alignment.
- Use an RNN Encoder-Decoder architecture as recently proposed: the decoder is trained to predict the next word $y_{i}$ given the context vector $c$ and all previously predicted words $y_1, \dots , y_{i-1}$.
  - Notation: $h_i$ is the encoder hidden state at time $i$ and $s_i$ is the decoder hidden state at time $i$.
  - $p(y_i | \{y_1, \ldots, y_{i-1}\}, c) = g(y_{i-1}, s_i, c)$ where $g$ could be a simple linear layer and $s_i = decoder(y_{i-1}, s_{i-1}, c)$
- The limitation of this architecture is the use of a single fixed-length vector $c$ in decoding at every time step. This paper proposes to use a different vector $c_i$ for each time step $i$, allowing each context vector pays attention to different source words in the input sentence. It's calculated as a weighted sum over all encoder hidden states: $$c_i=\sum_{j=1}^{T_x}{\alpha_{ij}h_j}$$
- $\alpha$ is the weight calculated as softmax of attention score: $$\alpha_{ij}=softmax(score(s_{i-1},h_j))$$
- Attention score is parameterized as a feedforward neural network (a matrix multiplication followed by a non-linear and a vector multiplication to get a scalar): $$score(s,h)=v^\top tanh(Ws+Uh)$$

<p align="center">
  <img src="figure2.png" style="width:400px"/>
</p>