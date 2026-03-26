@"

\# Contracts



Contracts define how decisions are evaluated.



\## Structure



\- intent: purpose of the rule

\- inputs: data used for evaluation

\- outputs: expected result (pass or fail)

\- behavior: evaluation logic

\- errorModel: failure conditions



\## Example (Conceptual)



Rule: Require test updates



\- If source files change and no test files are modified

\- Then result = FAIL

"@ | Set-Content docs/contracts.md

