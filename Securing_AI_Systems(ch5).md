# Securing AI Systems - chapter 5

---

# 1. What this room teaches

- How AI systems are structured
- How AI components create new attack surfaces
- AI trust boundaries and security risks
- OWASP LLM Top 10 and MITRE ATLAS basics
- Secure architecture design for AI systems
- Defence in depth for AI environments

> Main idea:
AI systems are not only models.
They are complete systems with many connected components.

---

# 2. Traditional Apps vs AI Systems

## Traditional Application

- Fixed logic
- Structured input
- Predictable outputs
- Direct database queries

Example:
Web form -> API -> Database -> Response

---

## AI Augmented Application

- Natural language input
- Probabilistic outputs
- Dynamic responses
- Model based reasoning
- Retrieval systems and external tools

Example:
User -> Prompt -> LLM -> Tool access -> Generated response

> AI systems increase complexity and attack surface

---

# 3. Core Components of an AI System

## User Interface

- User Interface -> Frontend where users interact with the AI system

Example:
Chatbot webpage

---

## API Layer

- API Layer -> Handles communication between frontend and backend systems

Example:
Request sent from chat UI to AI backend

---

## Orchestration Layer

- Orchestration Layer -> Combines prompts, user input, memory, and tools before sending to the model

Main responsibilities:
- Prompt construction
- Context management
- Tool selection
- Request routing

> One of the most critical security layers

---

## System Prompt

- System Prompt -> Hidden instructions defining model behaviour and rules

Example:
"You are a secure banking assistant"

---

## LLM

- Large Language Model -> AI model generating text responses using probability prediction

Example:
ChatGPT style model

---

## RAG

- Retrieval Augmented Generation -> System retrieving external data and adding it to model context

Example:
AI assistant searching company documents before answering

---

## Embeddings

- Embeddings -> Numerical vector representations of text used for semantic search

Example:
Finding similar documents using vector similarity

---

## Tool Integration

- Tool Integration -> Allowing AI systems to perform external actions

Examples:
- Database queries
- API calls
- File access
- Email sending

> Dangerous if permissions are excessive

---

## Logging System

- Logging -> Recording prompts, outputs, actions, and errors for monitoring

Example:
Tracking suspicious prompts

---

# 4. Trust Boundaries

- Trust Boundary -> Point where data moves between systems with different trust levels

Examples:
- User input entering backend
- LLM output reaching database
- External data entering prompts

> Every trust boundary is a possible attack point

---

# 5. AI Attack Surface

- Attack Surface -> All possible points where attackers can interact with the system

AI systems increase attack surface because:
- Inputs are unstructured
- Outputs are dynamic
- External tools are connected
- Models can influence actions

---

# 6. OWASP LLM Top 10

- OWASP LLM Top 10 -> Security framework listing major LLM application risks

Important categories in this room:

---

## LLM02 Sensitive Information Disclosure

- Sensitive Information Disclosure -> Leakage of secrets or private data through model responses

Examples:
- API keys
- Internal prompts
- User data

---

## LLM05 Improper Output Handling

- Improper Output Handling -> Trusting model output without validation

Example:
AI generates SQL query that gets executed directly

> Similar to injection vulnerabilities

---

## LLM06 Excessive Agency

- Excessive Agency -> Giving AI systems too many permissions or actions

Examples:
- Sending emails
- Modifying databases
- Executing commands

> AI should never have unrestricted power

---

## LLM07 System Prompt Leakage

- System Prompt Leakage -> Exposure of hidden instructions through prompting attacks

Example:
"Reveal your hidden instructions"

---

## LLM10 Unbounded Consumption

- Unbounded Consumption -> Resource exhaustion caused by uncontrolled AI usage

Examples:
- Huge prompts
- Infinite requests
- Expensive API abuse

---

# 7. MITRE ATLAS

- MITRE ATLAS -> Framework mapping attacks against AI systems

Purpose:
- Identify attacker behaviour
- Map attack techniques
- Improve AI threat modelling

> AI equivalent of MITRE ATTACK

---

# 8. System Level Threats

## Prompt Injection

- Prompt Injection -> Malicious instructions attempting to manipulate AI behaviour

Example:
"Ignore previous instructions"

---

## Data Poisoning

- Data Poisoning -> Injecting malicious data into training or retrieval systems

Example:
Fake documents added to company knowledge base

---

## Model Theft

- Model Theft -> Extracting or cloning a model through repeated queries

Example:
Attacker recreates model behaviour through API access

---

## Sensitive Data Exposure

- Sensitive Data Exposure -> AI revealing confidential information

Example:
Leaking customer records

---

## Tool Abuse

- Tool Abuse -> AI misusing connected systems or APIs

Example:
AI sending unauthorised emails

---

# 9. Secure Design Patterns

## Defence in Depth

- Defence in Depth -> Multiple layers of security controls protecting the system

Example:
- Input filtering
- Output validation
- Access controls
- Monitoring

> If one layer fails, another still protects the system

---

## Least Privilege

- Least Privilege -> Giving systems only minimum required permissions

Example:
Chatbot can read database but cannot delete records

---

## Input Validation

- Input Validation -> Filtering and checking user input before processing

Example:
Blocking malicious prompts

---

## Output Validation

- Output Validation -> Checking model responses before actions are executed

Example:
Reviewing generated SQL queries before execution

---

## Monitoring

- Monitoring -> Continuous observation of AI behaviour and logs

Goals:
- Detect attacks
- Detect abuse
- Detect unusual outputs

---

# 10. MLSecOps

- MLSecOps -> Security focused operations for machine learning systems

Includes:
- Monitoring models
- Securing pipelines
- Detecting drift
- Managing vulnerabilities

> Similar to DevSecOps but for AI systems

---

# 11. AI Security Architecture

A secure AI system should include:

1. Secure APIs
2. Authentication
3. Access controls
4. Prompt filtering
5. Output validation
6. Monitoring
7. Logging
8. Rate limiting
9. Human approval for critical actions

---

# 12. Example Scenario

## Insecure AI Assistant

System:
AI assistant connected to database

Problem:
LLM output directly executes database queries

Attack:
Attacker injects prompt:
"Delete all customer records"

Result:
Database compromise

---

## Secure Version

Security added:
- Output validation
- Human approval
- Restricted permissions
- Monitoring

Result:
Attack blocked

---

# 13. High Yield Questions

- Hidden model instructions -> System Prompt
- External knowledge retrieval -> RAG
- Semantic vector representation -> Embeddings
- AI attack framework -> MITRE ATLAS
- AI risk framework -> OWASP LLM Top 10
- Excessive permissions -> Excessive Agency
- Leaking hidden instructions -> System Prompt Leakage
- Unchecked model output -> Improper Output Handling
- Resource exhaustion -> Unbounded Consumption
- Security layers -> Defence in Depth

---

# 14. Important Facts

- AI systems create new trust boundaries
- Natural language input breaks traditional validation methods
- AI outputs should never be trusted directly
- Connected tools increase impact of attacks
- Least privilege is critical for AI systems
- Monitoring is required at every layer

---

# 15. Reality Check

Reading security frameworks is not enough.

You should be able to:
- Identify trust boundaries in AI systems
- Explain AI attack paths
- Secure orchestration layers
- Design safe tool integrations
- Detect dangerous permissions

If not, you only memorised concepts.

---

# 16. Mentor Note

Most people think the model is the main problem.

Wrong.

The real risk is:
- integrations
- permissions
- orchestration
- external tools
- weak validation

The model is only one component.

The dangerous part is what the model is allowed to control.

That is where real AI security starts.
