# AI Forensics - Chapter-4

---

# 1. What this room teaches

- How AI is used in digital forensics and incident response
- How machine learning helps investigators analyse large data
- Benefits and risks of AI in DFIR
- AI assisted anomaly detection
- Ethical and legal concerns in AI forensics

> Main idea:
AI helps investigators process huge amounts of forensic data faster

---

# 2. What is DFIR

- DFIR -> Digital Forensics and Incident Response
- Digital Forensics -> Investigating digital devices to collect and analyse evidence
- Incident Response -> Process of identifying and handling security incidents

Goals:
- Detect attacks
- Preserve evidence
- Understand attacker actions
- Recover systems

---

# 3. Why AI Matters in DFIR

Modern systems generate massive amounts of:
- Logs
- Network traffic
- User activity
- Cloud events
- Endpoint telemetry

Human analysts cannot manually process everything efficiently.

AI helps by:
- Finding anomalies
- Detecting patterns
- Automating analysis
- Correlating events

> AI turns huge datasets into manageable investigations

---

# 4. AI Capabilities in Forensics

## Anomaly Detection

- Anomaly Detection -> Identifying behaviour different from normal patterns

Example:
AI detects unusual login activity at midnight

Uses:
- Insider threat detection
- Malware detection
- Suspicious user behaviour

---

## Pattern Recognition

- Pattern Recognition -> Detecting repeated or related behaviours in data

Example:
AI links multiple failed logins across systems

---

## Correlation Analysis

- Correlation Analysis -> Connecting events from different data sources

Example:
Combining firewall logs and endpoint logs to rebuild attack timeline

---

## Automation

- Automation -> AI performing repetitive analysis tasks automatically

Example:
Automatically sorting suspicious files

---

# 5. AI Techniques Used in DFIR

## Machine Learning

- Machine Learning -> Models learning patterns from forensic data

Example:
Learning normal user behaviour

---

## NLP

- NLP -> Natural Language Processing used for analysing text data

Uses:
- Chat analysis
- Email analysis
- Social media investigation

Example:
Detecting phishing language in emails

---

## Sentiment Analysis

- Sentiment Analysis -> Determining emotional tone in messages

Example:
Analysing threatening messages in chats

---

## CNN

- CNN -> Convolutional Neural Network commonly used for image and video analysis

Uses:
- Deepfake detection
- Image classification
- Video forensics

> CNNs learn spatial patterns in images

---

# 6. AI in Image and Video Forensics

AI helps detect:
- Manipulated images
- Deepfakes
- Edited videos
- Object recognition

Example:
AI identifies face manipulation in a fake video

Challenges:
- High quality deepfakes
- False positives
- Compression artifacts

---

# 7. AI in Malware Analysis

AI can:
- Detect malicious patterns
- Classify malware families
- Analyse behaviour automatically

Example:
AI detects ransomware behaviour from system activity

Benefits:
- Faster triage
- Large scale analysis
- Behaviour based detection

---

# 8. AI in Log Analysis

AI systems analyse:
- Authentication logs
- Network logs
- Endpoint logs
- Cloud logs

Example:
AI detects impossible travel login behaviour

> Very useful for large environments

---

# 9. User and Entity Behaviour Analytics

- UEBA -> User and Entity Behaviour Analytics
- UEBA monitors behaviour patterns for anomalies

Example:
Employee downloads massive data unexpectedly

AI learns:
- Normal login times
- Typical locations
- Usual device usage

Then flags unusual behaviour

---

# 10. AI and Threat Hunting

- Threat Hunting -> Proactive search for hidden threats

AI helps:
- Prioritise alerts
- Detect hidden patterns
- Reduce investigation time

Example:
AI identifies suspicious PowerShell execution patterns

---

# 11. Precision and Recall

## Precision

- Precision -> Percentage of flagged results that were actually correct

High precision:
Few false positives

Example:
10 alerts triggered
9 are real threats
Precision = 90 percent

---

## Recall

- Recall -> Percentage of actual threats successfully detected

High recall:
Few missed attacks

Example:
100 attacks exist
90 detected
Recall = 90 percent

---

# 12. Deterministic vs Non Deterministic AI

## Deterministic

- Deterministic -> Same input always gives same output

Example:
Traditional rule based system

---

## Non Deterministic

- Non Deterministic -> Same input may produce different outputs

Example:
LLM responses changing slightly each run

> Common in modern AI systems

---

# 13. Challenges of AI in DFIR

## False Positives

- False Positive -> Benign activity incorrectly flagged as malicious

Example:
Legitimate admin activity detected as attack

---

## False Negatives

- False Negative -> Real attack missed by detection system

Example:
Malware not detected

---

## Bias

- Bias -> AI producing unfair or inaccurate outcomes due to training data

Example:
Model trained on incomplete datasets

---

## Hallucinations

- Hallucination -> AI generating incorrect information confidently

Example:
AI invents fake indicators of compromise

---

# 14. Ethical and Legal Concerns

## Privacy Issues

AI systems may process:
- Personal messages
- Emails
- User behaviour
- Sensitive logs

Risk:
Privacy violations

---

## Evidence Integrity

- Evidence Integrity -> Maintaining original evidence without modification

Problem:
AI generated analysis may not always be reproducible

---

## Explainability

- Explainability -> Ability to understand why AI made a decision

Problem:
Black box models are difficult to audit

---

# 15. Human Analysts Still Matter

AI cannot replace investigators because:
- AI lacks real understanding
- AI can hallucinate
- AI may miss context
- Legal decisions require human validation

> AI assists analysts
> It does not replace them

---

# 16. Example Scenario

## Traditional Investigation

Analyst manually reviews:
- 5 million logs
- Multiple endpoints
- Email records

Time:
Days or weeks

---

## AI Assisted Investigation

AI:
- Detects anomalies
- Correlates events
- Flags suspicious activity
- Builds timeline automatically

Result:
Faster investigation

---

# 17. Real World Example

Scenario:
Employee account compromised through phishing

AI detects:
- Unusual login location
- Suspicious email attachment
- Abnormal file access
- Data exfiltration pattern

Investigator confirms:
- Phishing attack
- Stolen credentials
- Source code theft

---

# 18. Important Terms

- IOC -> Indicator of Compromise
- UEBA -> User and Entity Behaviour Analytics
- DFIR -> Digital Forensics and Incident Response
- NLP -> Natural Language Processing
- CNN -> Convolutional Neural Network

---

# 19. High Yield Questions

- AI finding unusual behaviour -> Anomaly Detection
- Emotional tone analysis -> Sentiment Analysis
- Image and video neural network -> CNN
- AI text processing -> NLP
- Correct positive results -> Precision
- Same output every time -> Deterministic
- Different outputs possible -> Non Deterministic
- AI assisted user monitoring -> UEBA
- AI generated fake information -> Hallucination

---

# 20. Important Facts

- AI helps process massive forensic datasets
- AI improves scalability in DFIR
- CNNs are heavily used in image forensics
- NLP helps analyse emails and chats
- AI systems are probabilistic
- Human validation is still required
- False positives remain a major challenge

---

# 21. Reality Check

Reading AI DFIR concepts is not enough.

You should be able to:
- Explain how anomaly detection works
- Identify AI limitations in investigations
- Understand precision vs recall
- Detect risks of AI hallucinations
- Validate AI findings manually

If not, you only memorised terminology.

---

# 22. Mentor Note

Most beginners think AI magically solves investigations.

Wrong.

AI mainly does:
- filtering
- prioritising
- correlating
- pattern recognition

The investigator still matters.

Bad analysts blindly trust AI.
Good analysts verify everything.

That difference decides whether evidence stands or collapses.
