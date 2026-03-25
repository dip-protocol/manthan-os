\# 🤖 Manthan OS



\*\*Deterministic PR decision engine that enforces merge policies.\*\*



Manthan OS is a Decision Operating System for GitHub that evaluates pull requests using predefined contracts and enforces outcomes through required status checks.



> Every decision is traceable, auditable, and built for trust.



\---



\## 🚀 What is Manthan OS?



Manthan OS transforms pull request evaluation from advisory checks into a deterministic enforcement system.



Instead of suggesting improvements, Manthan enforces decisions — automatically blocking merges when conditions fail.



\---



\## 🔍 Key Features



\- \*\*Deterministic decisions\*\*  

&#x20; Same input always produces the same result. No randomness, no drift.



\- \*\*Merge blocking enforcement\*\*  

&#x20; Failing conditions automatically prevent merges using GitHub status checks.



\- \*\*Structured decision reports\*\*  

&#x20; Clear, human-readable feedback directly in pull requests.



\- \*\*Contract-based evaluation\*\*  

&#x20; Define rules as contracts and apply them consistently across repositories.



\- \*\*Idempotent processing\*\*  

&#x20; Ensures consistent results even with repeated webhook events.



\---



\## ⚙️ How it Works



```text

Pull Request → Webhook → Manthan Engine → Decision → Status Check → 🚫 / ✅

A pull request is opened or updated

GitHub sends a webhook event

Manthan evaluates the PR using contracts

A decision report is posted

A status check is set

If failed → merge is blocked

📊 Example Decision Report

\## 🤖 Manthan OS — Decision Report



\### ❌ REJECTED



Some checks failed. Please review the details below.



\### 📊 Summary

\- Total checks: 1

\- Failed: 1

\- Passed: 0



▶ View detailed decision breakdown

🎯 Use Cases

Enforce pull request description requirements

Apply governance rules across repositories

Standardize review criteria across teams

Build auditable decision pipelines

🧠 Why Manthan OS?



Traditional CI tools run checks.



Manthan OS enforces decisions.



It ensures that:



Decisions are deterministic

Outcomes are enforceable

Behavior is consistent across all pull requests

🚀 Getting Started

Install Manthan OS from GitHub Marketplace

Configure branch protection rules

Require the manthan/decision status check

Open a pull request

Observe deterministic enforcement

🔒 Security



Manthan OS uses GitHub App authentication with signed JWT tokens.



No personal data is stored

All decisions are computed in real time

HTTPS-only communication

Secure token handling

📦 Contracts (Example)

{

&#x20; "name": "pr-description-required",

&#x20; "rule": "description\_length > 20",

&#x20; "onFail": "reject"

}

📁 Repository Structure

docs/         → Architecture and concepts  

contracts/    → Example contract definitions  

examples/     → Sample decision outputs  

🧭 Architecture



See: docs/architecture.md



📄 License



MIT (or your preferred license)



🌐 Links

GitHub App: (add your marketplace link after approval)

Documentation: (this repository)

✨ Philosophy



Manthan OS is built on one principle:



Decisions should not be suggestions.

Decisions should be enforceable.

