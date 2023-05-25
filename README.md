# Outline2Story

This repository contains source code for paper [Outline to Story: Fine-grained Controllable Story Generation from Cascaded Events](https://arxiv.org/abs/2101.00822):

```
@article{fang2021outline,
  title={Outline to Story: Fine-grained Controllable Story Generation from Cascaded Events},
  author={Fang, Le and Zeng, Tao and Liu, Chaochun and Bo, Liefeng and Dong, Wen and Chen, Changyou},
  journal={arXiv preprint arXiv:2101.00822},
  year={2021}
}
```

0. get source data ([WritingPrompts](https://github.com/pytorch/fairseq/blob/master/examples/stories/README.md), [WikiPlots](https://github.com/markriedl/WikiPlots)).
1. data pre-processing (data/utils.py) -> need the bert_serving client running in order to compute the preprocessing.
2. dataset statistics (dataset_statistics.py)
3. training (choose from several different implementations on parallelism: train.py, train_apex.py, train_dist.py, train_dist_apex.py).
4. generation, evaluation and analysis (generate.py, eval_ppl.py, generate_event_analysis.py).

Contact Le Fang: lefang@buffalo.edu

my email: sofiadipace@gmail.com


Update on 2022:
If you encounter package version issue, sorry for that I don't have a requirements.txt with exact versions. I used this package: https://github.com/nvidia/apex
How to install apex from their Github Repo:

```
git clone https://github.com/NVIDIA/apex
cd apex
pip install -v --disable-pip-version-check --no-cache-dir ./

```



