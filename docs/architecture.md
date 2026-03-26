@"

\# Architecture



Manthan OS is a deterministic decision engine that integrates with GitHub via webhooks and status checks.



\## System Flow



Pull Request -> GitHub Webhook -> Manthan Engine -> Decision -> Status Check -> Merge Allowed or Blocked



\## Components



1\. GitHub App

\- Receives webhook events

\- Authenticates using JWT and installation tokens



2\. Webhook Handler

\- Validates incoming events

\- Ensures idempotent processing



3\. Decision Engine

\- Evaluates pull requests using contracts

\- Produces pass or fail decisions



4\. Enforcement Layer

\- Posts results on pull requests

\- Sets commit status checks



5\. Branch Protection

\- Blocks merge if checks fail



\## Security



\- JWT authentication

\- Scoped installation tokens

\- HTTPS communication

\- No storage of sensitive data



\## Determinism



\- Same input -> same output

\- No runtime drift

\- No randomness

"@ | Set-Content docs/architecture.md

