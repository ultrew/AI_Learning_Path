# 🧠 AI/ML Security Threats — Minimal Notes

---

## 1. What this room teaches
- Basics of AI, ML, Deep Learning
- How LLMs work
- AI-specific cyber threats
- Offensive + defensive use of AI

---

## 2. Core Concepts

### AI vs ML vs DL
- **AI** → machines mimic intelligence
- **ML** → learns from data (no hardcoding)
- **DL** → neural networks + large datasets

### ML Types
- **Supervised** → labeled data
- **Unsupervised** → no labels
- **Semi-supervised** → mix of labeled + unlabeled
- **Reinforcement** → reward-based learning

### Neural Networks
- **Input Layer** → raw data input
- **Hidden Layers** → processing
- **Output Layer** → result
- **Synapses** → weighted connections

---

## 3. LLMs (Critical)

- **LLMs = Large Language Models**
- Based on **Transformer architecture (2017)**

### Training Pipeline
1. Pre-training
2. Fine-tuning
3. RLHF

### Use Cases
- Chat systems
- Code generation
- Content generation

---

## 4. AI Threats

### Model-Level Attacks
- **Prompt Injection** → manipulate instructions
- **Data Poisoning** → corrupt training data
- **Model Theft** → extract model via API
- **Privacy Leakage** → sensitive data exposure
- **Model Drift** → performance degradation

### AI-Enhanced Attacks
- **Deepfakes** → fake voice/video
- **AI Phishing** → realistic scams

> AI mainly amplifies existing attack vectors

---

## 5. Framework

- **MITRE ATLAS** → AI attack mapping framework

> Equivalent to MITRE ATT&CK for AI systems

---

## 6. Defense Strategies

- Role-based access control (RBAC)
- Encryption of data/models
- Model monitoring (drift detection)
- Secure ML pipelines
- AI-based threat detection

---

## 7. ML Lifecycle (Attack Surface)

1. Data collection
2. Data preprocessing
3. Training
4. Evaluation
5. Deployment
6. Monitoring

> Every stage can be attacked

---

## 8. High-Yield Q&A

- Semi-labelled + unlabelled → **Semi-supervised**
- First NN layer → **Input layer**
- No labels + auto feature extraction → **Deep Learning**
- NN connections → **Synapses**
- ChatGPT type → **LLMs**
- First training stage → **Pre-training**
- Architecture → **Transformer**
- AI threat framework → **MITRE ATLAS**
- Model cloning → **Model theft**
- Fake media → **Deepfake**

---

## ⚠️ Reality Check

Reading ≠ understanding.

You should be able to:
- Identify attack surfaces in ML pipelines
- Explain prompt injection practically
- Describe model extraction via APIs

If not, revisit and practice hands-on.

---

## Next Step

- Build attack scenarios
- Simulate prompt injection
- Analyze real AI threat cases
