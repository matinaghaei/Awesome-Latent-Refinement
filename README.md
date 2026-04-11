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

We focus on systems where:

- **Additional internal compute at inference time improves performance**
- Computation is performed via **learned, reusable refinement dynamics over latent state**

The field is organized into two regimes:

- **Supervised latent refinement** — iterative updates are learned directly for reasoning tasks
- **Reinforcement-learned latent refinement** — internal planning and refinement emerge through reward-driven training

---

## 📚 Table of Contents

- [Overview](#-overview)
- [Supervised Latent Refinement](#-supervised-latent-refinement)
- [Reinforcement-Learned Latent Refinement](#-reinforcement-learned-latent-refinement)
- [Inclusion Criteria](#-inclusion-criteria)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🧬 Supervised Latent Refinement

Models that learn to perform **iterative updates over latent state** for reasoning tasks.

---

### 🔁 Recurrent-Depth / Looped Models

- **Scaling up Test-Time Compute with Latent Reasoning: A Recurrent Depth Approach (2025)**  
  [📄 Paper](https://arxiv.org/abs/2502.05171) · [💻 Code](https://github.com/seal-rg/recurrent-pretraining)  
  Introduces recurrent-depth reasoning; performance improves with more inference steps.

- **Scaling Latent Reasoning via Looped Language Models (2025)**  
  [📄 Paper](https://arxiv.org/abs/2510.25741) · [🌐 Project](https://ouro-llm.github.io/) · [🤗 Models](https://huggingface.co/collections/ByteDance/ouro)  
  Trains looped language models that refine latent representations iteratively.

- **Efficient Parallel Samplers for Recurrent-Depth Models and Their Connection to Diffusion Language Models (2025)**  
  [📄 Paper](https://arxiv.org/abs/2510.14961) · [📝 OpenReview](https://openreview.net/forum?id=z62rRFnNaX)  
  Proposes parallel sampling methods to reduce latency in iterative refinement.

- **Parallel Loop Transformer (PLT) for Efficient Test-Time Computation Scaling (2025)**  
  [📄 Paper](https://arxiv.org/abs/2510.24824)  
  Parallelizes looped computation to make latent refinement practical at scale.

---

### 🧠 Recursive Latent Reasoners

- **Hierarchical Reasoning Model (HRM) (2025)**  
  [📄 Paper](https://arxiv.org/abs/2506.21734) · [💻 Code](https://github.com/sapientinc/HRM)  
  Uses interacting recurrent modules to refine internal state for reasoning.

- **Tiny Recursive Model (TRM) / Less is More: Recursive Reasoning with Tiny Networks (2025)**  
  [📄 Paper](https://arxiv.org/abs/2510.04871) · [💻 Code](https://github.com/SamsungSAILMontreal/TinyRecursiveModels)  
  Compact recursive architecture showing strong reasoning from minimal models.

---

### 🚫 Excluded (Supervised)

- Text-based self-refinement methods
- Branching / search-based reasoning
- Diffusion or generative latent refinement not used for reasoning
- Standard feedforward transformers without iterative computation

---

## 🎮 Reinforcement-Learned Latent Refinement

Agents that develop **iterative latent computation** through interaction and reward.

---

### 🧠 Emergent Planning in Model-Free RL

- **An Investigation of Model-Free Planning (2019)**  
  [📄 Paper](https://proceedings.mlr.press/v97/guez19a.html) · [🧩 Boxoban Levels](https://github.com/google-deepmind/boxoban-levels)  
  Demonstrates that model-free recurrent agents can exhibit planning behavior and benefit from additional internal computation.

- **Interpreting Emergent Planning in Model-Free Reinforcement Learning (2025)**  
  [📄 Paper](https://arxiv.org/abs/2504.01871) · [📝 OpenReview](https://openreview.net/forum?id=DzGe40glxs) · [💻 Code](https://github.com/tuphs28/emergent-planning/tree/main) · [🌐 Project](https://tuphs28.github.io/projects/interpplanning/)  
  Provides mechanistic evidence of latent plan refinement within recurrent agents.

---

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

Contributions are welcome!

Please ensure submissions satisfy the **inclusion criteria**. When adding a paper, briefly explain:

- How latent state is iteratively refined
- What computation is shared across steps
- Whether additional compute improves performance

---

## 📜 License

This work is licensed under the **Creative Commons Zero v1.0 Universal (CC0 1.0)** license.

To the extent possible under law, the authors have waived all copyright and related or neighboring rights to this work.
