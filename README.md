# Josh Shultis

Independent security researcher focused on **AI assistants, agents, tool authorization, and connected applications**.

I research a narrow question: **when an AI system can read untrusted content and act through a user's connected tools, what source is actually being granted authority over the resulting action?**

I work from evidence, not model output. When I test a security boundary, I follow the chain from the exact user action to the backend/tool operation, resulting product state, and the artifacts that prove—or fail to prove—causality.

**Research home:** [shultislabs.com](https://shultislabs.com)

## Selected public work

| Project | What it shows |
|---|---|
| [Security RAG demo](https://github.com/Josh-Shultis/security-rag-demo) | A complete synthetic investigation: controlled vulnerable behavior, a fixed control, source-linked evidence, regression tests, and a short walkthrough. |
| [Evidence Ledger](https://github.com/Josh-Shultis/evidence-ledger) | A local evidence-curation tool that uses hashes, report comparison, and explicit manual-review states so different artifacts are not silently collapsed together. |

Both public projects use synthetic data. Private vendor reports, authenticated captures, active payloads, and unreleased findings stay out of the public repositories.

## Research focus

- AI agent and assistant tool authorization
- Indirect prompt injection and authority from shared/untrusted context
- Parameter provenance: where material tool-action values came from
- Cross-account, ownership, and shared-object boundaries
- Workspace and connected-app state changes
- Persistent mutations, confirmation, and auditability
- Evidence engineering for reproducible vulnerability research

## Authority-Source Differential

A recurring method in my current work is to compare **where operational authority came from**, rather than treating any successful prompt injection as sufficient proof.

```text
trusted positive control
        ↓
remove / verify absence of matching trusted instruction
        ↓
untrusted-content test
        ↓
track material parameter provenance
        ↓
backend/tool record + native before/after state
        ↓
negative control / repeat
        ↓
smallest supported conclusion
```

The positive control proves the authorized workflow works. It does **not** prove the indirect condition.

A state change proves that state changed. It does **not**, by itself, prove which earlier input caused it.

[Research method](RESEARCH-METHOD.md)

## How I work

- Start with one narrow security question.
- Define attacker, victim, object ownership, and the authority boundary.
- Preserve original artifacts and exact identifiers.
- Use a known-good positive control before the adversarial condition when it improves attribution.
- Remove or document competing trusted instruction paths.
- Track which source supplied material action parameters.
- Correlate requests, responses, account context, timestamps, tool records, and native application state.
- Keep negative and ambiguous results instead of filtering them out.
- Separate observations from inference.
- Split different security primitives unless one is required to reproduce the next.
- Build reports around what the evidence proves, not around the strongest possible wording.

## Recognition & programs

- **Microsoft Security Response Center (MSRC)** — Research acknowledged
- **Google Vulnerability Reward Program (VRP)** — Active participant
- **OpenAI Daybreak — Trusted Access for Cyber** — Approved participant

## What to review first

If you want to see how I reconstruct a case from primary evidence, start with the [Security RAG case study](https://github.com/Josh-Shultis/security-rag-demo/blob/main/docs/CASE-STUDY.md). It shows the question, decisive evidence, control, fix, and exact limits of the conclusion.

If you want to inspect the evidence-integrity side, review [Evidence Ledger](https://github.com/Josh-Shultis/evidence-ledger), especially how it preserves distinct files with the same name and forces manual review when a safe automated choice is not possible.

The next public artifact is a fully synthetic agent-authorization differential lab. It will be linked here only after publication review is complete and the repository is publicly accessible.

## Research path

I entered security research through a nontraditional route after more than a decade in land surveying. An unexpected AI behavior during an ordinary conversation in 2026 led me to start testing how instructions and connected tools handle trust.

The method developed experimentally rather than from a pre-existing playbook: direct instruction tests → retrievable/shared state → access-based triggers → exact object targeting → backend/native-state correlation → parameter provenance → negative controls → evidence/claim gates.

I keep the early experiments in the history because the mistakes and ambiguous results explain why the current controls exist.

## Contact

- Research: [shultislabs.com](https://shultislabs.com)
- Email: [joshshultis@gmail.com](mailto:joshshultis@gmail.com)
- GitHub: [Josh-Shultis](https://github.com/Josh-Shultis)
