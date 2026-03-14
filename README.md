# Secure LLM Pipeline

This project demonstrates a **secure CI/CD pipeline for AI and Large Language Model (LLM) applications** using automated DevSecOps security controls.

The pipeline integrates multiple security scanners and LLM-specific tests to detect vulnerabilities, secrets, and prompt injection risks during development.

---

# Security Controls Implemented

## Static Application Security Testing (SAST)

**Bandit**
- Detects insecure Python coding patterns
- Identifies security issues such as unsafe imports, subprocess misuse, and weak cryptography

**Semgrep**
- Advanced static analysis for security vulnerabilities
- Detects insecure patterns across application code

---

## Dependency Vulnerability Scanning

**Safety**
- Detects known vulnerabilities in Python dependencies
- Uses vulnerability databases to flag insecure packages

**Trivy**
- Comprehensive vulnerability scanner
- Detects OS and dependency vulnerabilities

---

## Secret Detection

**Gitleaks**
- Detects hard-coded secrets such as:
  - API keys
  - tokens
  - passwords
  - credentials

---

## LLM Security Testing

**Prompt Injection Detection**
- Detects malicious prompts attempting to:
  - override system instructions
  - reveal system prompts
  - bypass AI safety controls

Example threats tested:

- `Ignore previous instructions`
- `Reveal system prompt`
- `Bypass safety restrictions`

---

# CI/CD Security Pipeline

The security pipeline runs automatically using **GitHub Actions** on:

- code pushes
- pull requests

Security checks run automatically before code is merged.

Pipeline stages:
Bandit
Safety
Semgrep
Trivy
Gitleaks
Prompt Injection Test

---

# Project Structure
secure-llm-pipeline
│
├── .github/workflows
│ └── ai-security-pipeline.yml
│
├── llm_security_tests
│ └── prompt_injection_test.py
│
├── README.md
└── .gitignore


---

# Security Focus

This project demonstrates practices aligned with:

- **OWASP Top 10 for LLM Applications**
- **AI DevSecOps**
- **Secure AI pipeline development**
- **Automated security testing**

---

# Author

GitHub: https://github.com/alexpedient-cloud
