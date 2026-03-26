# 🤖 Manthan OS

![GitHub last commit](https://img.shields.io/github/last-commit/dip-protocol/manthan-os)
![GitHub issues](https://img.shields.io/github/issues/dip-protocol/manthan-os)
![GitHub stars](https://img.shields.io/github/stars/dip-protocol/manthan-os?style=social)
![License](https://img.shields.io/badge/license-MIT-blue)
![Deterministic](https://img.shields.io/badge/decisions-deterministic-black)
![Enforcement](https://img.shields.io/badge/enforcement-enabled-success)

**Block pull requests that violate your rules.**

Manthan OS evaluates pull requests against defined rules and prevents merges when those rules fail.

> Deterministic. Enforceable. Auditable.

---

## 🔥 Example

**Rule**  
PR must include test updates  

**Pull Request**  
Changed: src/api.js  
No tests updated  

**Result**  
FAIL  
Reason: No test files modified  

→ Merge blocked until fixed  

---

## ⚡ What it does

Manthan turns pull request checks into **enforceable decisions**.

- Evaluates every PR using rules  
- Produces a clear PASS / FAIL decision  
- Blocks merges automatically on failure  

---

## 🧠 Why not just use GitHub checks?

GitHub checks:
- Run tools  
- Show results  

They do not:
- Enforce structured decisions  
- Guarantee consistency  
- Prevent drift  

Manthan OS does.

---

## ⚙️ How it works

```text
Pull Request -> Webhook -> Manthan -> Decision -> Status Check -> Blocked / Allowed
System Flow
📦 Core Concept: Contracts

Manthan evaluates pull requests using decision contracts.

Contracts define what is allowed and what is blocked.

Example Contract
{
  "name": "require-tests",
  "rule": "test_files_changed == true",
  "onFail": "reject"
}
🔍 Features

Deterministic decisions
Same input -> same output

Merge enforcement
Failures automatically block merges

Contract-based rules
Define once, apply everywhere

Clear decision reports
Readable output directly in PRs

Idempotent processing
Consistent results across events

📊 Decision Output
Manthan OS — Decision Report

Status: FAILED

Checks:
- Require test updates: FAILED

Reason:
No test files modified

Result:
Merge blocked
🚀 Getting Started
Install Manthan OS from GitHub Marketplace
Enable it for your repository
Require manthan/decision in branch protection
Open a pull request
📚 Documentation
Getting Started
How It Works
Configuration
Contracts
Example
Architecture
FAQ
Support
📁 Examples
PR Flow
Sample Contract
Decision Report
🔒 Security
GitHub App authentication (JWT)
Scoped installation tokens
HTTPS-only communication
No storage of repository data
✨ Philosophy

Decisions should not be suggestions.
Decisions should be enforced.