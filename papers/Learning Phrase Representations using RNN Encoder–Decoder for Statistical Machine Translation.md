<div style="margin-bottom:10px">
<img src="../figures/Learning Phrase Representations using RNN Encoder–Decoder for Statistical Machine Translation-0.png" style="display:block;margin-left:auto;margin-right:auto;margin-bottom:10px;width:800px"/>

<div style="display: flex; justify-content: space-between;">
<a href='https://arxiv.org/abs/1406.1078'><img src='https://img.shields.io/badge/dynamic/json?url=https://api.semanticscholar.org/graph/v1/paper/0b544dfe355a5070b60986319a3f51fb45d1348e?fields=citationCount&query=citationCount&label=EMNLP%202014&prefix=citation%20'/></a>
<i>1st Jan 2024, Phong Nguyen</i>
</div>
</div>

- This is probably the earliest paper that applies neural networks for machine translation.
- Proposing an RNN Encoder-Decoder architecture: learns to encode a variable-length sequence $\textbf{x}=(x_1,x_2,\ldots,x_T)$ into a fixed-length vector representation $c$ using an RNN and then to decode $\textbf{c}$ back into a variable-length sequence $\textbf{y}=(y_1,y_2,\ldots,y_{T'})$ using another RNN.
  - Encoder: $h_t = f(h_{t-1}, x_{t})$, then $c=h_T$
  - Decoder: $s_t = f(s_{t-1}, y_{t-1}, c)$
- For the choice of RNN, this paper introduces GRU (gated recurrent unit) as a comparable alternative to LSTM.
- This is not an end-to-end machine translation model. The model is used to calculate probability of a pair of source and target phrases, which is then used as an additional feature in an SMT system.

<img src="../figures/Learning Phrase Representations using RNN Encoder–Decoder for Statistical Machine Translation-1.png" style="display:block;margin-left:auto;margin-right:auto;width:400px" />