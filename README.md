# AI Research Sandbox

## Repository Overview

This repository serves as a comprehensive learning environment for deep learning fundamentals and modern AI architectures. It contains hands-on implementations of core machine learning algorithms, from foundational backpropagation mechanics to advanced transformer architectures.

## Repository Review

### Strengths

**1. Foundational Understanding Focus**
- The repository demonstrates a bottom-up learning approach, starting with fundamental concepts like automatic differentiation before moving to complex architectures
- The inclusion of micrograd provides excellent insight into how backpropagation actually works at a granular level
- Clear progression from basic attention mechanisms to full GPT implementations

**2. Practical Implementation**
- Working implementations rather than just theoretical notes
- Jupyter notebooks that combine code with explanations and visualizations
- Experimental code in `GPT/experiments/attention/` showing active exploration and testing

### Repository Structure

```
.
├── GPT/                          # GPT implementation and experiments
│   ├── experiments/attention/    # Attention mechanism experiments
│   ├── src/                      # Source code
│   ├── data/                     # Training data
│   └── train_gpt.ipynb          # GPT training notebook
├── backpropagation/             # Backpropagation fundamentals
│   ├── micrograd/               # Autograd engine implementation
│   └── micrograd_lecture_*.ipynb # Educational notebooks
├── attention_mechanism/          # Attention mechanism studies
│   ├── basics_attention.ipynb   # Basic attention concepts
│   └── extras_attention.ipynb   # Advanced attention topics
├── Transformer/                  # Transformer architecture (WIP)
```

### Key Components

**Micrograd (backpropagation/micrograd/)**
- Tiny autograd engine implementing reverse-mode autodiff
- ~100 lines of code for the core engine
- Small neural network library with PyTorch-like API
- Excellent for understanding backpropagation mechanics
- Includes visualization tools for computation graphs

**GPT Implementation**
- Character-level or word-level language model implementation
- Attention mechanism experiments
- Training notebooks and utilities
- Currently in active development

**Attention Mechanism Studies**
- Dedicated notebooks exploring attention mechanisms
- Covers both basic and advanced concepts
- Large text corpus (input.txt) for experimentation

