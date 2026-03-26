\# 🧭 Architecture



Manthan OS is a deterministic decision engine that integrates with GitHub via webhooks and status checks.



\---



\## 🔄 System Flow



```text

Pull Request → GitHub Webhook → Manthan Engine → Decision → Status Check → Merge Allowed / Blocked

⚙️ Components

1\. GitHub App

Receives webhook events (pull\_request, push)

Authenticates using JWT and installation tokens

2\. Webhook Handler

Validates incoming GitHub events

Ensures idempotent processing (no duplicate decisions)

3\. Decision Engine

Evaluates pull requests using predefined contracts

Produces deterministic decisions (approve / reject)

4\. Enforcement Layer

Posts structured decision reports on pull requests

Sets commit status checks (manthan/decision)

5\. GitHub Branch Protection

Requires status checks to pass before merging

Blocks merges when decisions fail

🔒 Security Model

GitHub App authentication using signed JWT

Installation tokens used for scoped access

HTTPS-only communication

No persistent storage of sensitive user data

🧠 Determinism Principle



Manthan OS guarantees:



Same input → same output

No runtime drift

No probabilistic behavior



This ensures consistency and auditability across all pull requests.

