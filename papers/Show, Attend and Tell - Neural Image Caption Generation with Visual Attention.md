*6th Jan 2024, Phong Nguyen*

<div>
<p align="center">
  <img src="../figures/Show, Attend and Tell - Neural Image Caption Generation with Visual Attention-0.png" style="width:800px"/>
</p>

<a href='https://arxiv.org/abs/1502.03044'><img src='https://img.shields.io/badge/dynamic/json?url=https://api.semanticscholar.org/graph/v1/paper/4d8f2d14af5991d4f0d050d22216825cac3157bd?fields=citationCount&query=citationCount&label=ICML%202015&prefix=citation%20'/></a>

</div>

- This paper introduces attention to the CNN-RNN Encoder-Decoder architecture for image captioning. 
- To apply attention, a set of feature vectors is required insead of a single one extracted from the last linear layer as in the previous work. The paper uses the feature map from an earlier convolutional layer such as $14 \times 14 \times 512$ features. So, we have 196 feature vectors, each with 512 dimensions.
- The paper presents hard attention and soft attention. The former focuses on a single feature; whereas the latter smoothly focuses all on features. Hard attention gave better result in their experiments but was harder to train. 

<p align="center">
  <img src="../figures/Show, Attend and Tell - Neural Image Caption Generation with Visual Attention-1.png" style="width:400px"/>
</p>