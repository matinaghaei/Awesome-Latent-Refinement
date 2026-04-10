# 🧬 Awesome Latent Refinement  
### *Iterative Reasoning & Planning in Latent Space*

A curated list of work on **latent iterative computation**: models and agents that improve performance by repeatedly updating internal representations rather than producing explicit intermediate outputs.

---

## 🧠 Overview

This repository focuses on systems where:

- **Additional internal compute at inference time improves performance**
- Computation is performed via **learned, reusable refinement dynamics over latent state**

We organize the field into two regimes:

- **Supervised latent refinement** — iterative updates are learned directly for reasoning tasks  
- **Reinforcement-learned latent refinement** — internal planning and refinement emerge through reward-driven training  

---

## 🔒 Inclusion Criteria

Papers are included only if they satisfy all of the following:

1. **Iterative refinement of latent state** at inference time  
2. **Shared or recurrent computation** across refinement steps  
3. **Performance improves with additional internal compute**  

---

## 🧬 Supervised Latent Refinement

Models that learn to perform **iterative updates over latent state** for reasoning tasks.

---

### 🔁 Recurrent-Depth / Looped Models

Models that treat depth as **iterative computation**, applying a shared transformation repeatedly at inference time.

- **Scaling up Test-Time Compute with Latent Reasoning (2025)**  
  Introduces recurrent-depth reasoning; performance improves with more inference steps.

- **Scaling Latent Reasoning via Looped Language Models (2025)**  
  Trains looped language models that refine latent representations iteratively.

- **Efficient Parallel Samplers for Recurrent-Depth Models (2025)**  
  Proposes parallel sampling methods to reduce latency in iterative refinement.

- **Parallel Loop Transformer (PLT) for Efficient Test-Time Scaling (2025)**  
  Parallelizes looped computation to make latent refinement practical at scale.

---

### 🧠 Recursive Latent Reasoners

Architectures designed explicitly for **multi-step reasoning through recursive latent updates**.

- **Hierarchical Reasoning Model (HRM) (2025)**  
  Uses interacting recurrent modules to refine internal state for reasoning.

- **Tiny Recursive Model (TRM) / Less is More: Recursive Reasoning with Tiny Networks (2025)**  
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

Agents that exhibit **planning-like behavior** through recurrent latent computation.

- **An Investigation of Model-Free Planning (2019)**  
  Demonstrates that model-free recurrent agents can exhibit planning behavior and benefit from additional internal computation.

- **Interpreting Emergent Planning in Model-Free Reinforcement Learning (2025)**  
  Provides mechanistic evidence of latent plan refinement within recurrent agents.

---

### 🔁 Recurrent Policies & Latent Computation

*(Intentionally sparse — included only when strong evidence of latent refinement is present.)*

---

### 🚫 Excluded (RL)

- Model-based RL relying on explicit planning over learned world models  
- Tree search methods (e.g., MCTS)  
- Policies without iterative internal computation  
- Latent world models used purely for simulation  

---

## 💡 Notes

- This repository emphasizes **mechanism over surface form**  
- Focus is on systems where **reasoning or planning emerges from iterative latent computation**  
- Compared to supervised methods, RL-based latent refinement remains **underexplored**  

---

## ⭐ Contributing

Contributions are welcome, but please ensure submissions satisfy the **strict inclusion criteria**.

When adding a paper, briefly explain:
- How latent state is iteratively refined  
- What computation is shared across steps  
- Whether additional compute improves performance  

---

## 📜 License

This repository is licensed under the **Creative Commons Zero v1.0 Universal (CC0 1.0)**.

You are free to use, modify, and distribute this work without restriction.
