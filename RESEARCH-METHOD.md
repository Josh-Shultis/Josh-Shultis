# Research method

This page describes my review standard. It is not evidence that any particular security finding is confirmed.

## One claim, one evidence chain

For each finding, identify the actor, controlled input, user action, product behavior, backend operation, persistent result, and demonstrated benefit. A gap in that chain remains a gap in the report.

| Classification | Meaning |
|---|---|
| Verified | An artifact or controlled observation directly supports the statement |
| Inference | An interpretation that needs additional evidence |
| Missing | The required evidence has not been captured or reviewed |

A successful response does not establish persistence. A model statement does not establish a tool operation. An object appearing in a shared interface does not establish ownership or another account's access.

## Authority-source differential

When a claim depends on instructions arriving through external or untrusted content, I separate the authorized control from the actual test condition.

### 1. Trusted positive control

Intentionally configure the workflow and verify the expected authorized behavior. Record the exact trigger, operation, material parameters, target, and resulting state.

The control proves that the workflow works when authorized. It does **not** prove indirect prompt injection.

### 2. Reset / competing-authority check

Remove or disable the matching trusted instruction path where practical. Record that state. If stale trusted configuration cannot be ruled out, keep that limitation explicit.

### 3. Untrusted condition

Move equivalent operational logic into attacker-controlled or otherwise untrusted content while changing as few other variables as practical.

Record every material difference between the control and test runs.

### 4. Parameter provenance

State exactly which material values the victim supplied and which they did not.

When practical, use a harmless run-specific canary that:

- exists in the untrusted source;
- is absent from the victim request and trusted configuration;
- appears in the resulting operation and/or persistent state.

Canary transfer strengthens source-to-effect attribution. It does not automatically prove every step of the chain.

### 5. Negative control

Neutralize the operational instruction while preserving the surrounding retrieval/action path as closely as practical.

A refusal, confirmation prompt, unchanged object, or failed transfer is evidence. If the negative control reproduces the same effect, the untrusted-causality claim must be narrowed or rejected.

### 6. Minimum conclusion

Distinguish at least three outcomes:

- **authority failure supported** — the untrusted-source differential survives the controls;
- **boundary held in the tested condition** — untrusted content was retrieved but did not receive operational authority;
- **causality not established** — an action occurred, but another input or control can independently explain it.

## Keep the primitives separate

Treat these as distinct evidentiary questions unless one is necessary to reproduce the next:

- retrieval;
- instruction uptake;
- operation preparation;
- tool execution;
- persistence;
- cross-account effect;
- confirmation behavior;
- audit/activity behavior.

Native persistent state proves the state exists. It does not, by itself, prove which earlier input caused it.

## Evidence handling

Preserve originals. Analyze copies and record source filenames, hashes, timestamps with timezones, account labels, and relevant object/request IDs. Connect artifacts using content and identifiers rather than timestamp proximity alone. Keep negative results and conflicting observations.

For suspected data transfer, establish source and destination access separately and verify the receiving account can read the resulting data. For confirmation claims, record exactly what the user requested and what the interface displayed.

Prefer evidence in roughly this order when claims conflict:

1. native application state / immutable export;
2. raw request-response or operation record with correlating identifiers;
3. video/screenshot showing account, action, and resulting state;
4. parsed/indexed derivative;
5. research note, model analysis, or report draft.

Lower-authority material can help locate or interpret primary evidence. It does not replace it.

## Public research examples

Use synthetic data or material explicitly authorized for release. Include:

1. The question and scope.
2. Environment and dependency versions.
3. Actor/ownership/ACL model when relevant.
4. Positive control and controlled variable.
5. Reset/trusted-path-absence state when authority source is the question.
6. Exact victim action and parameter provenance.
7. Recorded observations with artifact references.
8. Negative or ambiguous result.
9. Narrow conclusion and limitations.
10. Disclosure status with a primary public link when available.

Never publish credentials, session data, private reports, live research endpoints, operational vendor payloads, or another person's account information. Sanitizing a current file does not sanitize its Git history.

## Tooling and attribution

Automated checks assist review; they do not prove impact or replace inspection of evidence. Describe AI assistance and third-party components when they materially affect the work, and explain the implementation choices I can independently defend.

Model reviewers can search, correlate, challenge, and suggest. They do not promote evidence or decide that a vulnerability is proven.

Vendor recognition, bounty payments, CVEs, and remediation claims belong in a portfolio only when supporting records can be cited or appropriately shared. A later failed test alone does not prove a patch.
