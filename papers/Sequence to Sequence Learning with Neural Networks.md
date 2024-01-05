*2nd Jan 2024, Phong Nguyen*

<div>
<p align="center">
  <img src="../figures/Sequence to Sequence Learning with Neural Networks-0.png" style="width:800px"/>
</p>

<a href='https://arxiv.org/abs/1411.4555'><img src='https://img.shields.io/badge/dynamic/json?url=https://api.semanticscholar.org/graph/v1/paper/cea967b59209c6be22829699f05b8b1ac4dc092d?fields=citationCount&query=citationCount&label=NeurIPS%202014&prefix=citation%20'/></a>

</div>

- One of the first paper that proposes an end-to-end neural network architecture for machine translation.
- The same RNN Encoder-Decoder architecture but different from *Learning Phrase Representations using RNN Encoder–Decoder for Statistical Machine Translation* in a few points:
  - The RNN uses a stack of 4 LSTM layers 
  - Context vector $c$ is only used as the initial hidden state of the decoder whereas it is used as an extra input in every decoding step in the other paper.
  
<p align="center">
  <img src="../figures/Sequence to Sequence Learning with Neural Networks-1.png" style="width:800px"/>
</p>