# Josh Shultis — AI Security Research & Evidence-First Method

This is the public researcher profile and navigation page. It describes research focus and links to selected public, synthetic projects; it is not a code or evidence-processing platform.

Independent security researcher focused on AI assistants, agents, tool use, and connected applications.

I work from evidence, not model output. When I test a security boundary, I try to follow the full chain: what the user asked, what the system actually did, what changed, and which artifacts prove it.

## Selected work

| Project | What it shows |
|---|---|
| [Security RAG demo](https://github.com/Josh-Shultis/security-rag-demo) | A complete synthetic investigation: controlled vulnerable behavior, a fixed control, source-linked evidence, regression tests, and a short walkthrough. |
| [Evidence Ledger](https://github.com/Josh-Shultis/evidence-ledger) | A local evidence-curation tool that uses hashes, report comparison, and explicit manual-review states so different artifacts are not silently collapsed together. |

Both public projects use synthetic data. Private vendor reports, authenticated captures, and unreleased findings stay out of the public repositories.

## Open-source contributions

- **MCP filesystem effective-root logging ([issue #4912](https://github.com/modelcontextprotocol/servers/issues/4912))** — I identified and documented an operator-visibility gap: after client-provided MCP Roots changed the effective filesystem allowlist, the server logged a count but did not provide one clear summary of the active directories and their source. I retested the access-control behavior on Ubuntu and Windows and confirmed the tested restrictions continued to work; I did not report an access-control bypass. The maintainer implemented the requested logging in [PR #5390](https://github.com/modelcontextprotocol/servers/pull/5390), which was merged into `v2/main` on October 29, 2026. The repository's v2.3.0 release was published on November 4 with filesystem package version 2.2.0; the [filesystem changelog](https://github.com/modelcontextprotocol/servers/blob/main/src/filesystem/CHANGELOG.md) explicitly lists #5390 and commit `6017ed3`. The maintainer closed issue #4912 as completed. This was an accepted operator-observability improvement; the merged implementation was authored by the project maintainer.

## Research focus

- AI assistant and agent tool authorization
- Indirect prompt injection and shared-context behavior
- Cross-account and ownership boundaries
- Workspace and connected-app state changes
- Auditability, provenance, and reproducible evidence
- Local tooling for large evidence sets

## How I work

- Start with one narrow security question.
- Preserve original artifacts and exact identifiers.
- Correlate requests, responses, account context, timestamps, and native application state.
- Use controls to separate expected behavior from the behavior under test.
- Keep observations separate from inference.
- Build reports around what the evidence proves, not around the strongest possible wording.

[Research method](RESEARCH-METHOD.md)

## Recognition & programs

- **Microsoft Security Response Center (MSRC)** — Research acknowledged
- **Google Vulnerability Reward Program (VRP)** — Active participant
- **OpenAI Daybreak — Trusted Access for Cyber** — Approved participant

## What to review first

If you want to see how I approach a case, start with the [Security RAG case study](https://github.com/Josh-Shultis/security-rag-demo/blob/main/docs/CASE-STUDY.md). It shows the question, decisive evidence, control, fix, and the exact limits of the conclusion.

If you want to see the evidence-handling side, review [Evidence Ledger](https://github.com/Josh-Shultis/evidence-ledger), especially how it preserves different files with the same name and forces manual review when a safe automated choice is not possible.

## Contact

- Email: [joshshultis@gmail.com](mailto:joshshultis@gmail.com)
- GitHub: [Josh-Shultis](https://github.com/Josh-Shultis)
