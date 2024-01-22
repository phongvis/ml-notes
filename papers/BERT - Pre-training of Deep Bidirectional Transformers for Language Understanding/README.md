* 2024, Phong Nguyen*

<div>
<p align="center">
  <img src="figure1.png" style="width:800px"/>
</p>

<a href='https://arxiv.org/abs/1810.04805'><img src='https://img.shields.io/badge/dynamic/json?url=https://api.semanticscholar.org/graph/v1/paper/df2b0e26d0599ce3e70df8a9da02e51594e0e992?fields=citationCount&query=citationCount&label=NAACL%202019&prefix=citation%20'/></a>

- BERT is a language representation model that is trained with deep bidrectional transformers for language understanding.
- In the pre-training stage, two tasks are used: masked word prediction and next sentence prediction. The input includes two special tokens `[CLS]` that is designed to aggregate meaning of the input and `[SEP]` to separate two sentences in a pair.
- In the fine-tuning stage, the same architecture is reused with some minimal addition depending on the task. For example, in Question Answering (SQuAD), start vector $S$ and end vector $E$ are added. The fine-tuned model produces probability of each token in the paragraph section to be the start/end marker of the answer: $P_i=\text{softmax}(S.T_i)$.
</div>

<p align="center">
  <img src="figure2.png" style="width:800px"/>
</p>

- BERT is highly related to ELMo and GPT, using the same two-stage process: pre-training and fine-tuning.

| Model | Pre-training | Fine-tuning |
|-------|--------------|-------------|
| ELMo  | LSTM, shallow concatenation of left-to-right and right-to-left LMs. | Providing additional features for model-specific downstream tasks |
| GPT   | Left-to-right transformers, next word prediction | Same architecture with an dditional linear layer |
| BERT  | Bidirectional transformers, masked word prediction & next sentence prediction | Same architecture with an additional linear layer |
<p align="center">
  <img src="figure3.png" style="width:800px"/>
</p>