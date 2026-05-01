# 🧠 AI Models & Data - chapter 2

---

## 1. What this room teaches

* How AI models depend on training data
* Risks in data sourcing and preprocessing
* Model building decisions and their security impact
* Why AI models are opaque (black box problem)
* Supply chain risks in AI systems

> Core idea: **Model = Data + Decisions**

---

## 2. Training Data (Critical Foundation)

* **Training Data** → Dataset used to teach a model patterns and relationships

* **Data Provenance** → Ability to track origin, history, and modification of data

* **Common Crawl** → Large public web dataset widely used to train major AI models

* **ML-BOM (Machine Learning Bill of Materials)** → Documentation of datasets, sources, licenses, and processing steps

### Key Insight

Most modern AI systems are trained on **“datasets of datasets”**, meaning origin and licensing are often unknown ([Medium][1])

---

## 3. Data Risks

* **PII Exposure** → Personal data embedded into training datasets and potentially leaked by models
* **Credential Leakage** → Secrets (API keys, passwords) unintentionally included in datasets
* **License Risk** → Using data without proper legal rights due to poor documentation
* **Data Contamination** → Inclusion of malicious or low-quality data affecting model behavior

> Poor data = permanent risk baked into model weights

---

## 4. Model Building Concepts

* **Epoch** → One complete pass of training over the entire dataset
* **Overfitting** → Model memorises training data instead of learning general patterns
* **Underfitting** → Model fails to learn meaningful patterns from data
* **Generalisation** → Model’s ability to perform well on unseen data

### Optimization Techniques

* **Quantisation** → Reducing numerical precision of model weights to improve efficiency
* **Fine-tuning** → Adapting a pre-trained model to a specific task using new data
* **Federated Learning** → Training across multiple devices without centralising data

---

## 5. The Inheritance Problem

* **Model Inheritance** → Risks transferred from pre-trained models into fine-tuned models

### Why it matters

* Hidden biases
* Embedded sensitive data
* Unknown vulnerabilities

> You inherit everything—including what you don’t see

---

## 6. The Black Box Problem

* **Black Box Model** → Model whose internal decision-making process is not interpretable

### Issues

* Lack of transparency

* Difficult to audit decisions

* Hard to detect malicious behavior

* **Model Cards** → Documentation describing model purpose, data, and limitations

> Model cards help—but don’t fully solve opacity

---

## 7. AI Supply Chain Risk

### Components

1. Data sources
2. Preprocessing pipelines
3. Pre-trained models
4. Fine-tuning datasets
5. Deployment infrastructure

### Risks

* Unknown upstream data
* Third-party dependencies
* Hidden vulnerabilities

> AI supply chain ≈ software supply chain, but worse (less visibility)

---

## 8. Security Weak Points

* Data ingestion (poisoning risk)
* Training datasets (hidden sensitive info)
* Pre-trained models (inherited risk)
* APIs (model extraction risk)

> Attack surface starts BEFORE deployment

---

## 9. Example (Realistic)

### Scenario: Chatbot trained on web data

* Data source → Common Crawl
* Issue → Includes leaked credentials and PII
* Model behaviour → Occasionally outputs sensitive info

### Result

* Privacy breach
* Legal liability
* Reputation damage

---

## 10. High-Yield Q&A

* Data origin tracking → **Data Provenance**
* Large web dataset → **Common Crawl**
* AI SBOM equivalent → **ML-BOM**
* One training pass → **Epoch**
* Memorising data → **Overfitting**
* Reducing precision → **Quantisation**
* Risk from pre-trained models → **Inheritance Problem**
* Non-transparent model → **Black Box**

---

## 🔥 What actually matters (mentor note)

Everyone focuses on **models**. That’s wrong.

Real attack surface =
👉 **DATA PIPELINE**

If you compromise:

* dataset → you control behaviour
* pre-trained model → you inject backdoors
* fine-tuning → you override safeguards

---

## ⚠️ Reality Check

If you cannot:

* Explain how bad data ends up inside model weights
* Identify risks of fine-tuning external models
* Describe why model outputs may leak secrets

Then you don’t understand AI security—you just memorised terms.





