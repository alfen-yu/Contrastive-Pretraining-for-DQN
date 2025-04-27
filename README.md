# Pretraining DQN with Contrastive Learning for Sparse-Reward Environments

This project investigates an approach to improve the performance of Deep Q-Networks (DQN) by **pretraining** the convolutional layers with **contrastive learning** on **unlabeled observations** collected from the environment. After pretraining, the DQN is **fine-tuned** using traditional reinforcement learning.

The goal is to enhance:
- **Sample efficiency**: Learn faster with fewer environment steps.
- **Generalization**: Perform better in challenging, sparse-reward environments.

---

## Motivation

Classic DQN agents often struggle in **sparse reward settings** because the initial random exploration provides little learning signal. Inspired by advances in **self-supervised learning** (e.g., SimCLR), this project proposes using contrastive learning to **pretrain representations** *before* reinforcement learning starts, improving learning dynamics without altering the DQN architecture.

---

## Key Ideas

- **Unsupervised pretraining**: Use contrastive learning (e.g., InfoNCE loss) on raw observations without reward labels.
- **Decoupled training**: Pretraining and RL happen separately.
- **Sparse reward focus**: Designed for difficult environments like Montezuma’s Revenge, Pitfall, etc.

---

## Goals

- Improve DQN performance on sparse-reward Atari games.
- Compare standard DQN vs contrastive-pretrained DQN.
- Evaluate sample efficiency and final performance.

---
