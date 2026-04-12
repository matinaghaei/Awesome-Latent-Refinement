# 🧬 Awesome Latent Refinement
### *Iterative Reasoning & Planning in Latent Space*

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
![License: CC0](https://img.shields.io/badge/license-CC0%201.0-lightgrey)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)
![Last Commit](https://img.shields.io/github/last-commit/matinaghaei/awesome-latent-refinement)
![Stars](https://img.shields.io/github/stars/matinaghaei/awesome-latent-refinement?style=social)

> A curated list of resources on latent iterative reasoning and planning.

⭐ If you find this useful, consider starring the repo!

---

## 🧠 Overview

This repository collects work on **latent iterative computation**: models and agents that improve performance by repeatedly updating internal representations rather than producing explicit intermediate outputs.

It focuses on a single core idea:

- **Performance improves through iterative refinement of latent state**
- **Computation is shared or recurrent across refinement steps**
- **Additional internal compute at inference time improves performance**

The field is organized into two regimes:

- **Supervised latent refinement**
- **Reinforcement-learned latent refinement**

---

## 📚 Table of Contents

- [Overview](#-overview)
- [Supervised Latent Refinement](#-supervised-latent-refinement)
  - [Dedicated Reasoners](#-dedicated-reasoners)
  - [Language Models](#-language-models)
- [Reinforcement-Learned Latent Refinement](#-reinforcement-learned-latent-refinement)
  - [Model-Free Planning](#-model-free-planning)
- [Inclusion Criteria](#-inclusion-criteria)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🧬 Supervised Latent Refinement

Models that learn to perform **iterative updates over latent state** for reasoning tasks.

### 🧠 Dedicated Reasoners

- **Hierarchical Reasoning Model (HRM) (2025)**  
  [📄 Paper](https://arxiv.org/abs/2506.21734) · [💻 Code](https://github.com/sapientinc/HRM)  
  Uses interacting recurrent modules to refine internal state for reasoning.

- **Tiny Recursive Model (TRM) / Less is More: Recursive Reasoning with Tiny Networks (2025)**  
  [📄 Paper](https://arxiv.org/abs/2510.04871) · [💻 Code](https://github.com/SamsungSAILMontreal/TinyRecursiveModels)  
  Compact recursive architecture showing strong reasoning from minimal models.

- **Symbol-Equivariant Recurrent Reasoning Models (SE-RRM) (2026)**  
  [📄 Paper](https://arxiv.org/abs/2603.02193) · [💻 Code](https://github.com/ml-jku/SE-RRM)  
  Extends recurrent reasoning models with symbol-equivariant structure for stronger generalization.

### 🔁 Language Models

- **Scaling up Test-Time Compute with Latent Reasoning: A Recurrent Depth Approach (2025)**  
  [📄 Paper](https://arxiv.org/abs/2502.05171) · [💻 Code](https://github.com/seal-rg/recurrent-pretraining)  
  Introduces recurrent-depth reasoning; performance improves with more inference steps.

- **Reasoning with Latent Thoughts: On the Power of Looped Transformers (2025)**  
  [📄 Paper](https://arxiv.org/abs/2502.17416) · [📝 OpenReview](https://openreview.net/forum?id=din0lGfZFd)  
  Shows that looped transformers can support latent thought-like reasoning and scale with effective depth.

- **Scaling Latent Reasoning via Looped Language Models (2025)**  
  [📄 Paper](https://arxiv.org/abs/2510.25741) · [🌐 Project](https://ouro-llm.github.io/) · [🤗 Models](https://huggingface.co/collections/ByteDance/ouro)  
  Trains looped language models that refine latent representations iteratively.

- **Encode, Think, Decode: Scaling test-time reasoning with recursive latent thoughts (2025)**  
  [📄 Paper](https://arxiv.org/abs/2510.07358) · [📝 OpenReview](https://openreview.net/forum?id=jBSye8M3FQ)  
  Enhances language-model reasoning by training a subset of layers to act as a recurrent latent reasoning block.

- **Efficient Parallel Samplers for Recurrent-Depth Models and Their Connection to Diffusion Language Models (2025)**  
  [📄 Paper](https://arxiv.org/abs/2510.14961) · [📝 OpenReview](https://openreview.net/forum?id=z62rRFnNaX) · [💻 Code](https://github.com/seal-rg/recurrent-pretraining)  
  Proposes parallel sampling methods to reduce latency in recurrent-depth generation.

- **Parallel Loop Transformer (PLT) for Efficient Test-Time Computation Scaling (2025)**  
  [📄 Paper](https://arxiv.org/abs/2510.24824)  
  Parallelizes looped computation to make latent refinement more practical at inference time.

### 🚫 Excluded (Supervised)

- Text-based self-refinement methods
- Branching / search-based reasoning
- Diffusion or generative latent refinement not used for reasoning
- Standard feedforward transformers without iterative computation

---

## 🎮 Reinforcement-Learned Latent Refinement

Agents that develop **iterative latent computation** through interaction and reward.

### 🧠 Model-Free Planning

- **An Investigation of Model-Free Planning (2019)**  
  [📄 Paper](https://proceedings.mlr.press/v97/guez19a.html) · [🧩 Boxoban Levels](https://github.com/google-deepmind/boxoban-levels)  
  Demonstrates that model-free recurrent agents can exhibit planning behavior and benefit from additional internal computation.

- **Planning in a recurrent neural network that plays Sokoban (2024)**  
  [📄 Paper](https://arxiv.org/abs/2407.15421) · [💻 Analysis Code](https://github.com/AlignmentResearch/learned-planner) · [💻 Training Code](https://github.com/AlignmentResearch/train-learned-planner)  
  Revisits model-free planning in recurrent agents and studies how additional computation affects planning performance.

- **Interpreting Emergent Planning in Model-Free Reinforcement Learning (2025)**  
  [📄 Paper](https://arxiv.org/abs/2504.01871) · [📝 OpenReview](https://openreview.net/forum?id=DzGe40glxs) · [💻 Code](https://github.com/tuphs28/emergent-planning/tree/main) · [🌐 Project](https://tuphs28.github.io/projects/interpplanning/)  
  Provides mechanistic evidence of latent plan refinement within recurrent agents.

- **On Computation and Reinforcement Learning (2026)**  
  [📄 Paper](https://arxiv.org/abs/2602.05999) · [🌐 Project](https://rajghugare19.github.io/computation-rl/index.html)  
  Studies how policies with fixed parameters but variable compute can solve harder RL problems and generalize better with more computation.

### 🚫 Excluded (RL)

- Model-based RL relying on explicit planning over learned world models
- Tree search methods (e.g., MCTS)
- Policies without iterative internal computation
- Latent world models used purely for simulation

---

## 🔒 Inclusion Criteria

Papers are included only if they satisfy all of the following:

1. **Iterative refinement of latent state** at inference time
2. **Shared or recurrent computation** across refinement steps
3. **Performance improves with additional internal compute**

---

## 🤝 Contributing

Contributions are welcome.

Please ensure submissions satisfy the **inclusion criteria**. When adding a paper, briefly explain:

- How latent state is iteratively refined
- What computation is shared across steps
- Whether additional compute improves performance

---

## 📜 License

This work is licensed under the **Creative Commons Zero v1.0 Universal (CC0 1.0)** license.

To the extent possible under law, the authors have waived all copyright and related or neighboring rights to this work.
