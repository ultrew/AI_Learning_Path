# 🧠 AI/ML Security Threats - chapter 1

---

## 1. What this room teaches
- Basics of AI, ML, Deep Learning  
- How LLMs work  
- AI-specific cyber threats  
- Offensive + defensive use of AI  

---

## 2. Core Concepts  

### AI vs ML vs DL  
- **AI** → Broad field of building systems that simulate human decision-making or intelligence  
- **ML** → Subset of AI where models learn patterns from data instead of explicit rules  
- **DL** → Subset of ML using multi-layer neural networks to learn complex representations  

### ML Types  
- **Supervised Learning** → Model learns from labeled input-output pairs  
- **Unsupervised Learning** → Model finds patterns in unlabeled data  
- **Semi-supervised Learning** → Model trains on small labeled + large unlabeled dataset  
- **Reinforcement Learning** → Agent learns actions via rewards and penalties  

### Neural Networks  
- **Input Layer** → First layer that receives raw feature data  
- **Hidden Layers** → Intermediate layers that transform inputs via weighted computations  
- **Output Layer** → Final layer producing prediction or classification  
- **Synapses (Weights)** → Numerical parameters controlling signal strength between neurons  

---

## 3. LLMs (Critical)  

- **LLMs (Large Language Models)** → Deep neural networks trained on massive text corpora to predict and generate language  
- **Transformer Architecture** → Attention-based neural architecture enabling parallel sequence processing  

### Training Pipeline  
- **Pre-training** → Initial training on large generic datasets to learn language patterns  
- **Fine-tuning** → Task-specific adjustment using curated datasets  
- **RLHF (Reinforcement Learning from Human Feedback)** → Aligns model outputs with human preferences using reward models  

### Use Cases  
- **Chat Systems** → Conversational AI interfaces  
- **Code Generation** → Automated code synthesis from prompts  
- **Content Generation** → Text, media, or data creation  

---

## 4. AI Threats  

### Model-Level Attacks  
- **Prompt Injection** → Malicious input designed to override model instructions or behavior  
- **Data Poisoning** → Inserting manipulated data into training sets to corrupt model behavior  
- **Model Theft (Extraction)** → Reconstructing a model by querying its API outputs  
- **Privacy Leakage** → Exposure of sensitive training data through model responses  
- **Model Drift** → Gradual degradation in model performance due to changing data distributions  

### AI-Enhanced Attacks  
- **Deepfakes** → AI-generated synthetic media mimicking real individuals  
- **AI Phishing** → Highly personalized scam messages generated using AI  

> AI increases scale, realism, and automation of attacks—not new primitives

---

## 5. Framework  

- **MITRE ATLAS** → Knowledge base mapping adversarial tactics and techniques targeting AI systems  

---

## 6. Defense Strategies  

- **RBAC (Role-Based Access Control)** → Restricts system access based on user roles  
- **Encryption** → Protects data and models from unauthorized access  
- **Model Monitoring** → Continuous tracking for anomalies or drift in predictions  
- **Secure ML Pipelines** → Hardening each stage of data and model lifecycle  
- **AI Threat Detection** → Using ML models to detect cyber threats  

---

## 7. ML Lifecycle (Attack Surface)  

1. **Data Collection** → Gathering raw data (risk: poisoning)  
2. **Data Preprocessing** → Cleaning/transformation (risk: manipulation)  
3. **Training** → Model learning phase (risk: backdoors)  
4. **Evaluation** → Testing model performance (risk: biased validation)  
5. **Deployment** → Production use (risk: API abuse, extraction)  
6. **Monitoring** → Ongoing oversight (risk: undetected drift/exploitation)  

> Every stage = distinct attack vector

---

## 8. High-Yield Q&A  

- Semi-labelled + unlabelled → **Semi-supervised Learning**  
- First NN layer → **Input Layer**  
- No labels + auto feature extraction → **Deep Learning**  
- NN connections → **Synapses (Weights)**  
- ChatGPT type → **LLMs**  
- First training stage → **Pre-training**  
- Architecture → **Transformer**  
- AI threat framework → **MITRE ATLAS**  
- Model cloning → **Model Theft (Extraction)**  
- Fake media → **Deepfake**  

---

## ⚠️ Reality Check  

If you cannot:
- Trace how prompt injection bypasses system prompts  
- Simulate model extraction with repeated queries  
- Identify weakest stage in ML pipeline  

Then you do NOT understand this topic yet.
