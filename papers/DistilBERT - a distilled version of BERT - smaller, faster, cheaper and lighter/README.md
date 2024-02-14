* 2024, Phong Nguyen*

<div>
<p align="center">
  <img src="figure1.png" style="width:800px"/>
</p>

<a href='https://arxiv.org/abs/1910.01108'><img src='https://img.shields.io/badge/dynamic/json?url=https://api.semanticscholar.org/graph/v1/paper/a54b56af24bb4873ed0163b77df63b92bd018ddc?fields=citationCount&query=citationCount&label=2020&prefix=citation%20'/></a>

- This paper proposes a lighter version (40% smaller) of BERT with comparable performance (97%). 
- It applies a teacher-student training mechanism with the student having the same architecture as BERT but with half of the layers.
- The objective loss includes language modelling, distillation (cross-entropy between predicted probabilities produced by the teacher and student) and cosine distance (probability alignment).
</div>