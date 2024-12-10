# SILMM
<h3><a href="">SILMM: Self-Improving Large Multimodal Models for Compositional Text-to-Image Generation</a></h3>

[Leigang Qu](https://leigang-qu.github.io/), [Haochuan Li](), [Wenjie Wang](https://wenjiewwj.github.io/), [Xiang Liu](https://lebronlambert.github.io/), [Juncheng Li	](https://person.zju.edu.cn/juncheng), [Liqiang Nie](https://liqiangnie.github.io/), and [Tat-Seng Chua](https://www.chuatatseng.com/)

<a href='https://silmm.github.io/'><img src='https://img.shields.io/badge/Project-Page-Green'></a> <a href='https://arxiv.org/abs/2412.05818'><img src='https://img.shields.io/badge/Paper-Arxiv-red'></a>

This repository contains code and links to the **SILMM** method for compositional text-to-image (T2I) generation to improve text-image alignment. In this work, we introduce a model-agnostic iterative self-improvement framework that can enable LMMs to provide helpful and scalable self-feedback and optimize text-image alignment via Direct Preference Optimization (DPO). To adapt SILMM to LMMs with continuous features, we propose a diversity mechanism to obtain diverse representations and a **kernel-based continuous DPO (KC-DPO)** for alignment. Extensive experiments on three compositional text-to-image generation benchmarks validate the effectiveness and superiority of SILMM, showing **improvements exceeding 30% on T2I-CompBench++ and around 20% on DPG-Bench**.



## Introduction

Schematic illustration of **SILMM**, comprising five steps: 1) LMMs generate compositional prompts by sampling based on provided instructions. 2) Diverse representations and images are generated using either discrete nucleus sampling or the proposed continuous DivDrop. 3) LMMs divide each compositional prompt into semantic units and generate questions for each unit. 4) VQA is conducted to answer these questions, with the answers and likelihoods aggregated into alignment scores as self-feedback. 5) For alignment tuning, DPO is applied for discrete LMMs, while the proposed KC-DPO is used for continuous LMMs

![](assets/framework.png)



## Release

- [ ] Release the training code. 
- [ ] Release the inference code for compositional text-to-image synthesis. 
- [x] Release the paper of SILMM on [arXiv](https://arxiv.org/pdf/2412.05818.pdf). 



## Citation

If you find our work useful in your research, please consider citing DPT:

```tex
@article{qu2024silmm,
  title={SILMM: Self-Improving Large Multimodal Models for Compositional Text-to-Image Generation},
  author={Qu, Leigang and Li, Haochuan and Wang, Wenjie and Liu, Xiang and Li, Juncheng and Nie, Liqiang and Chua, Tat-Seng},
  journal={arXiv preprint arXiv:2412.05818},
  year={2024}
}
```

## Acknowledgement

We thank the authors of [SEED-LLaMA](https://github.com/AILab-CVC/SEED) and [DreamLLM](https://github.com/RunpeiDong/DreamLLM), for making their code available. 
