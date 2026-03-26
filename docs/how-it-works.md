@"

\# How It Works



Manthan evaluates pull requests against defined decision rules and blocks merges when rules fail.



\## Flow



1\. Pull request event received from GitHub

2\. Decision contract loaded from /contracts

3\. Evaluation executed

4\. Result posted as a PR comment

5\. Status check updated



\## Guarantees



\- Deterministic (same input -> same output)

\- Idempotent (no duplicate effects)

\- Auditable (every decision is traceable)

"@ | Set-Content docs/how-it-works.md

