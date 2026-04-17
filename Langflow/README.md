# Langflow AI Agents

This directory contains exports of Langflow flows designed to assist with Quality Assurance (QA) tasks using AI. You can import these JSON files directly into your Langflow environment.

## 1. QA Buddy (`1_Langflow_AI_Agent_QA_Buddy.json`)

**What it does:**
This agent serves as an experienced QA companion to answer questions and queries strictly related to Quality Assurance.

**Technical Explanation:**
- **Input:** Accepts user messages specifically related to QA questions.
- **Model:** Powered by a Groq Language Model (`GroqModel` component).
- **System Prompt:** It strictly acts as a "QA Engineer with 15 years of experience," filtering responses to only answer queries related to QA.
- **Output:** Returns general text-based guidance or answers through the `ChatOutput` component.

---

## 2. Bug Classifier (`2_Langflow_AI_Agent_Bug_Classifier.json`)

**What it does:**
This agent helps in automated bug triage. It reads a bug report and classifies it by severity and category, while also checking for missing information like steps to reproduce or environment details.

**Technical Explanation:**
- **Input:** Accepts raw bug reports from users.
- **Prompt Template:** Uses a structured prompt template containing strict classification rules:
  - **Severity:** CRITICAL, HIGH, MEDIUM, LOW.
  - **Categories:** UI/UX, FUNCTIONAL, PERFORMANCE, SECURITY, DATA, INTEGRATION, INFRASTRUCTURE.
- **Verification:** Evaluates the bug report for missing components (Steps to Reproduce, Environment, Frequency).
- **Model:** Powered by a Groq Language Model configured as a "Senior QA Lead with 15 years of experience triaging bugs."
- **Output:** Outputs a structured, classified bug report formatted for actionable triage.
