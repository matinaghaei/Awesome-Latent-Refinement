<h1 align="center">🧬 Awesome Latent Refinement</h1>
<h3 align="center"><em>Iterative Reasoning & Planning in Latent Space</em></h3>

<p align="center">
  <a href="https://awesome.re">
    <img src="https://awesome.re/badge.svg"/>
  </a>
  <a href="https://github.com/matinaghaei/awesome-latent-refinement/stargazers">
    <img src="https://img.shields.io/github/stars/matinaghaei/awesome-latent-refinement.svg?style=social&label=Star"/>
  </a>
  <a href="https://github.com/matinaghaei/awesome-latent-refinement/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg"/>
  </a>
  <a href="https://github.com/matinaghaei/awesome-latent-refinement/blob/main/CONTRIBUTING.md">
    <img src="https://img.shields.io/badge/PRs-Welcome-brightgreen.svg"/>
  </a>
</p>

<p align="center">
  <img src="cover.jpg" width="650"/>
</p>

<br/>

<p align="center">
  ⭐ If you find this useful, please consider giving the repo a star!
</p>

---

## 🧠 Overview

- [🎯 Aim of the Project](#-aim-of-the-project)
- [🧬 Supervised Latent Refinement](#-supervised-latent-refinement)
  - [🧠 Dedicated Reasoners](#-dedicated-reasoners)
  - [🔁 Language Models](#-language-models)
- [🎮 Reinforcement-Learned Latent Refinement](#-reinforcement-learned-latent-refinement)
  - [🗺️ Model-Free Planning](#️-model-free-planning)
- [🔒 Inclusion Criteria](#-inclusion-criteria)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)

---

## 🎯 Aim of the Project

Latent refinement has recently emerged across both supervised reasoning and reinforcement learning. In these systems, performance improves not by producing explicit intermediate outputs, but by repeatedly updating internal representations using shared or recurrent computation.

This repository aims to:

- organize research on **iterative refinement of latent state**
- highlight the connection between **supervised reasoning** and **reinforcement-learned planning**
- track systems where **additional inference-time compute improves performance**
- provide a focused, high-signal resource for researchers interested in latent iterative computation

---

## 🧬 Supervised Latent Refinement

Models that learn to perform **iterative updates over latent state** for reasoning tasks.

### 🧠 Dedicated Reasoners

- **HRM**: "Hierarchical Reasoning Model". [![arXiv](https://img.shields.io/badge/arXiv-2506.21734-b31b1b.svg)](https://arxiv.org/abs/2506.21734) [![Code](https://img.shields.io/badge/Code-GitHub-green.svg)](https://github.com/sapientinc/HRM)

- **TRM**: "Less is More: Recursive Reasoning with Tiny Networks". [![arXiv](https://img.shields.io/badge/arXiv-2510.04871-b31b1b.svg)](https://arxiv.org/abs/2510.04871) [![Code](https://img.shields.io/badge/Code-GitHub-green.svg)](https://github.com/SamsungSAILMontreal/TinyRecursiveModels)

- **SE-RRM**: "Symbol-Equivariant Recurrent Reasoning Models". [![arXiv](https://img.shields.io/badge/arXiv-2603.02193-b31b1b.svg)](https://arxiv.org/abs/2603.02193) [![Code](https://img.shields.io/badge/Code-GitHub-green.svg)](https://github.com/ml-jku/SE-RRM)

### 🔁 Language Models

- **Scaling up Test-Time Compute with Latent Reasoning: A Recurrent Depth Approach**. [![arXiv](https://img.shields.io/badge/arXiv-2502.05171-b31b1b.svg)](https://arxiv.org/abs/2502.05171) [![Code](https://img.shields.io/badge/Code-GitHub-green.svg)](https://github.com/seal-rg/recurrent-pretraining)

- **Reasoning with Latent Thoughts: On the Power of Looped Transformers**. [![arXiv](https://img.shields.io/badge/arXiv-2502.17416-b31b1b.svg)](https://arxiv.org/abs/2502.17416) [![OpenReview](https://img.shields.io/badge/OpenReview-Paper-8E44AD.svg)](https://openreview.net/forum?id=din0lGfZFd)

- **Ouro**: "Scaling Latent Reasoning via Looped Language Models". [![arXiv](https://img.shields.io/badge/arXiv-2510.25741-b31b1b.svg)](https://arxiv.org/abs/2510.25741) [![Website](https://img.shields.io/badge/Website-Link-blue.svg)](https://ouro-llm.github.io/) [![HuggingFace](https://img.shields.io/badge/HuggingFace-Models-yellow.svg)](https://huggingface.co/collections/ByteDance/ouro)

- **Encode, Think, Decode: Scaling test-time reasoning with recursive latent thoughts**. [![arXiv](https://img.shields.io/badge/arXiv-2510.07358-b31b1b.svg)](https://arxiv.org/abs/2510.07358) [![OpenReview](https://img.shields.io/badge/OpenReview-Paper-8E44AD.svg)](https://openreview.net/forum?id=jBSye8M3FQ)

- **Efficient Parallel Samplers for Recurrent-Depth Models and Their Connection to Diffusion Language Models**. [![arXiv](https://img.shields.io/badge/arXiv-2510.14961-b31b1b.svg)](https://arxiv.org/abs/2510.14961) [![OpenReview](https://img.shields.io/badge/OpenReview-Paper-8E44AD.svg)](https://openreview.net/forum?id=z62rRFnNaX) [![Code](https://img.shields.io/badge/Code-GitHub-green.svg)](https://github.com/seal-rg/recurrent-pretraining)

- **Parallel Loop Transformer (PLT) for Efficient Test-Time Computation Scaling**. [![arXiv](https://img.shields.io/badge/arXiv-2510.24824-b31b1b.svg)](https://arxiv.org/abs/2510.24824)

### 🚫 Excluded (Supervised)

- text-based self-refinement methods
- branching or search-based reasoning
- diffusion or generative latent refinement not used for reasoning
- standard feedforward transformers without iterative computation

---

## 🎮 Reinforcement-Learned Latent Refinement

Agents that develop **iterative latent computation** through interaction and reward.

### 🗺️ Model-Free Planning

- **An Investigation of Model-Free Planning**. [![Paper](https://img.shields.io/badge/Paper-PMLR-blue.svg)](https://proceedings.mlr.press/v97/guez19a.html) [![Code](https://img.shields.io/badge/Code-Boxoban-green.svg)](https://github.com/google-deepmind/boxoban-levels)

- **Planning in a recurrent neural network that plays Sokoban**. [![arXiv](https://img.shields.io/badge/arXiv-2407.15421-b31b1b.svg)](https://arxiv.org/abs/2407.15421) [![OpenReview](https://img.shields.io/badge/OpenReview-Paper-8E44AD.svg)](https://openreview.net/forum?id=ORxjH9kTp8) [![Code](https://img.shields.io/badge/Code-Analysis-green.svg)](https://github.com/AlignmentResearch/learned-planner) [![Code](https://img.shields.io/badge/Code-Training-green.svg)](https://github.com/AlignmentResearch/train-learned-planner)

- **Interpreting Emergent Planning in Model-Free Reinforcement Learning**. [![arXiv](https://img.shields.io/badge/arXiv-2504.01871-b31b1b.svg)](https://arxiv.org/abs/2504.01871) [![OpenReview](https://img.shields.io/badge/OpenReview-Paper-8E44AD.svg)](https://openreview.net/forum?id=DzGe40glxs) [![Website](https://img.shields.io/badge/Website-Link-blue.svg)](https://tuphs28.github.io/projects/interpplanning/) [![Code](https://img.shields.io/badge/Code-GitHub-green.svg)](https://github.com/tuphs28/emergent-planning/tree/main)

- **On Computation and Reinforcement Learning**. [![arXiv](https://img.shields.io/badge/arXiv-2602.05999-b31b1b.svg)](https://arxiv.org/abs/2602.05999) [![Website](https://img.shields.io/badge/Website-Link-blue.svg)](https://rajghugare19.github.io/computation-rl/index.html)

### 🚫 Excluded (RL)

- model-based RL relying on explicit planning over learned world models
- tree search methods such as MCTS
- policies without iterative internal computation
- latent world models used purely for simulation

---

## 🔒 Inclusion Criteria

A paper is included only if it satisfies all of the following:

1. **Iterative refinement of latent state** at inference time
2. **Shared or recurrent computation** across refinement steps
3. **Performance improves with additional internal compute**

---

## 🤝 Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md).

---

## 📜 License

This work is licensed under the [Creative Commons Zero v1.0 Universal (CC0 1.0)](https://github.com/matinaghaei/awesome-latent-refinement/blob/main/LICENSE).
