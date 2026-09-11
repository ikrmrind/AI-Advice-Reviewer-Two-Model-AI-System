# 🤖 AI Advice Reviewer – Two-Model AI System

A simple **multi-model AI system built with Python and LangChain** where one AI generates advice and a second AI reviews, evaluates, and improves that advice.

## 💡 Project Idea

Instead of trusting a single AI response, this project uses two stages:

**User Input → AI Advice Generator → AI Reviewer → Improved Advice**

### 🤖 Model 1 — Advice Generator

The first model analyzes the user's situation and generates practical, safe, and concise advice.

### 🧠 Model 2 — Advice Reviewer

The second model acts as a critical evaluator.

It checks the generated advice for:

* Factual mistakes
* Incorrect assumptions
* Missing information
* Unsafe recommendations
* Weak reasoning
* Whether the advice actually addresses the user's problem

It then returns:

**Verdict:** Good / Needs Improvement / Unsafe

**Problem:** Identifies the main issue

**Improved Advice:** Provides a corrected version

## 🛠️ Tech Stack

* Python
* LangChain
* ChatPromptTemplate
* Mistral
* Groq
* GPT-OSS-120B
* python-dotenv

## 🏗️ Architecture

```text
                User
                 │
                 ▼
        ┌─────────────────┐
        │     Model 1     │
        │ Advice Generator│
        └────────┬────────┘
                 │
                 ▼
          Generated Advice
                 │
                 ▼
        ┌─────────────────┐
        │     Model 2     │
        │ Advice Reviewer │
        └────────┬────────┘
                 │
        ┌────────┴────────┐
        ▼                 ▼
     Verdict         Improved Advice
```

## 🎯 What I Learned

This project helped me understand how **multiple LLMs can work together instead of relying on a single model**.

The core idea is:

> One model generates the response, while another model evaluates and improves it.

This approach can be extended into larger **AI agents, verification systems, and multi-agent workflows**.

## 🚀 Future Improvements

* Fact verification
* Multiple reviewer models
* Web-based interface using Streamlit
* Logging and evaluation of model performance

## ⚠️ Disclaimer

This project is an educational AI experiment. AI-generated advice should not be treated as a substitute for qualified professional advice, especially for medical, legal, or financial situations.
