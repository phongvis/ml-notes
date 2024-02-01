* 2024, Phong Nguyen*

<div>
<p align="center">
  <img src="figure1.png" style="width:800px"/>
</p>

<a href='https://arxiv.org/abs/1909.11942'><img src='https://img.shields.io/badge/dynamic/json?url=https://api.semanticscholar.org/graph/v1/paper/7a064df1aeada7e69e5173f7d4c8606f4470365b?fields=citationCount&query=citationCount&label=ICLR%202020&prefix=citation%20'/></a>

- ALBERT proposes two techniques to lower memory consumption and improve training speed of BERT.
- Factorized embedding parameterization: splitting the embedding matrix $O(V \times H)$ into two matrices for a much smaller number of parameters $O(V \times E + E \times H)$ with
  - $V$: vocabulary size (~30,000)
  - $E$: vocabulary embedding size
  - $H$: model hidden size
- Cross-layer parameter sharing: just one set of parameters shared between all layers. The more parameters to share (attention, FFN, or all) the faster the model is but the worse it performs. Sharing parameters of a larger model gives SOTA results.
- ALBERT also suggests using sentence-order prediction instead of next sentence prediction. The model has to distinguish between consecutive segments and swapped consecutive ones, which is harder than distinguishing the next sentence and a random one.
</div>