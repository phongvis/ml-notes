*7th Jan 2024, Phong Nguyen*

<div>
<p align="center">
  <img src="../figures/Convolutional Sequence to Sequence Learning-0.png" style="width:800px"/>
</p>

<a href='https://arxiv.org/abs/1705.03122'><img src='https://img.shields.io/badge/dynamic/json?url=https://api.semanticscholar.org/graph/v1/paper/43428880d75b3a14257c3ee9bda054e61eb869c0?fields=citationCount&query=citationCount&label=ICML%202017&prefix=citation%20'/></a>

</div>

- This paper proposes a CNN Encoder-Decoder architecture for sequence to sequence learning, completely get rid of RNNs.
- CNNs process all tokens at once; therefore, besides token embedding ($w_i$), an extra positional embedding ($p_i$) is encoded provided to represent a sense of order: $e_i=w_i+p_i$. Both emebddings are simple linear layers.
- A one-dimensional convolutional layer is used to process the input embeddings, followed by a Gated Linear Units as shown in the diagram below. These two layers make a convolutional block and multiple blocks are stacked up with residual connection.
- Attention score is calculated using simple dot product.

<p align="center">
  <img src="../figures/Convolutional Sequence to Sequence Learning-1.png" style="width:400px"/>
</p>