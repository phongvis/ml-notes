*5th Jan 2024, Phong Nguyen*

<div>
<p align="center">
  <img src="../figures/Show and Tell - A Neural Image Caption Generator-0.png" style="width:800px"/>
</p>

<a href='https://arxiv.org/abs/1411.4555'><img src='https://img.shields.io/badge/dynamic/json?url=https://api.semanticscholar.org/graph/v1/paper/d4dc1012d780e8e2547237eb5a6dc7b1bf47d2f0?fields=citationCount&query=citationCount&label=CVPR%202015&prefix=citation%20'/></a>

</div>

- Inspired by the RNN Encoder-Decoder architecture in neural machine translation, this paper extends it for the image captioning task.
- As the output is text, the RNN decoder is still the same as in NMT.
- The encoder is changed to a CNN: it takes an image as input, runs through a CNN for feature extraction, passes the output vector to the RNN as the initial input: $x_{-1}=CNN(img)$.
- The paper found that adding the image vector to each time step performs worse than just the initial one.

<p align="center">
  <img src="../figures/Show and Tell - A Neural Image Caption Generator-1.png" style="width:400px"/>
</p>