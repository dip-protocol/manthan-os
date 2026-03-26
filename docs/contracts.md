\# 📜 Contracts



Contracts define the rules used by Manthan OS to evaluate pull requests.



Each contract represents a deterministic condition that must be satisfied.



\---



\## 🧩 Example Contract



```json

{

&#x20; "name": "pr-description-required",

&#x20; "rule": "description\_length > 20",

&#x20; "onFail": "reject"

}

🔍 Contract Structure

name: Unique identifier for the rule

rule: Condition evaluated against the pull request

onFail: Action when condition fails (reject or warn)

🎯 Common Contract Types

PR Metadata

Description length

Title format

Linked issues

Repository Governance

Required labels

Branch naming rules

Code Rules (future)

File-level constraints

Change restrictions

🧠 Deterministic Evaluation



Contracts are evaluated:



Independently

Without randomness

With consistent outcomes



This ensures predictable and auditable decisions.



🚀 Extensibility



Manthan OS is designed to support:



Custom contract definitions

Multi-contract evaluation

Policy-based rule sets



Contracts are the foundation of deterministic decision-making in Manthan OS.

