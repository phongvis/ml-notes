*9th Jan 2024, Phong Nguyen*

<div>
<p align="center">
  <img src="figure1.png" style="width:800px"/>
</p>

<a href='https://arxiv.org/abs/1802.05365'><img src='https://img.shields.io/badge/dynamic/json?url=https://api.semanticscholar.org/graph/v1/paper/3febb2bed8865945e7fddc99efd791887bb7e14f?fields=citationCount&query=citationCount&label=NAACL%202018&prefix=citation%20'/></a>

</div>

- This is one of the earliest papers that pretrains language models and applies the results for a variety of downstream tasks. 
- Previous approaches that learn word representations such as Word2Vec are static (a single vector for each word that could have multiple meanings depending on the context) and are learned with a limited context window.
- This paper uses a multi-layer bidirectional LSTM to pretrain word embeddings with language modelling task (predicting next word). A combination of the hidden states in all layers is used instead of the last layer alone: $R_k=\{x_k^{LM},\overrightarrow{h}_{k,j}^{LM},\overleftarrow{h}_{k,j}^{LM} | j=1,\cdots,L\}$.
- For each downstream task, the addition of ELMo representation was shown to boost the performance of all tasks to SoTA:
  - ELMo representation is learned as a softmax-normalized-weighted sum $\text{ELMo}_k = \gamma \sum_{j=0}^{L} s_j \cdot h_{k,j}$. 
  - The representation is then concatenated with context-independent representation like Word2Vec $[x_k;\text{ELMo}_k]$.