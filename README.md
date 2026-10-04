# Josh Shultis

Independent security researcher focused on AI assistants, agents, tool use, and connected applications.

I investigate how instructions, user authority, and application permissions interact. My approach is to trace a claim from the original input through the observed operation to its resulting state, and keep missing evidence visible.

## Research approach

- Define one hypothesis and vary one input at a time.
- Preserve original artifacts and correlate requests using IDs and content.
- Separate requested operations, successful responses, and independently verified persistence.
- Distinguish verified observations from inference, including negative results and contradictions.
- Publish only material that is authorized for disclosure and reviewed for sensitive data.

[How I evaluate evidence](RESEARCH-METHOD.md)

## Recognition & Programs

- **Microsoft Security Response Center (MSRC)** — Research acknowledged
- **Google Vulnerability Reward Program (VRP)** — Active participant
- **OpenAI Daybreak — Trusted Access for Cyber** — Approved participant

## Work to review

| Project | What it covers | Access |
|---|---|---|
| [Security research portfolio](https://github.com/Josh-Shultis/security-research-portfolio) | Synthetic MCP filesystem boundary checks with recorded results and explicit limits | Private; link requires access |
| [Security RAG](https://github.com/Josh-Shultis/security-rag) | Local-first evidence retrieval, source references, case-scoped search, and report-review tooling | Private research prototype |

These repositories are currently private. Public readers can review my methodology here and the [MCP effective-root logging issue](https://github.com/modelcontextprotocol/servers/issues/4912). Repository links do not imply public access, independent validation, or a confirmed vulnerability.

## What I aim to make reviewable

A useful research example includes the question, environment, exact observations, supporting artifacts, limitations, and what the result does **not** establish. A blocked boundary test is worth documenting alongside a successful reproduction.

My interests include prompt injection, tool authorization, account boundaries, evidence provenance, and responsible disclosure. I do not publish private vendor reports, authenticated captures, or unreleased vulnerability details here.

## Contact

- Email: [joshshultis@gmail.com](mailto:joshshultis@gmail.com)
- GitHub: [Josh-Shultis](https://github.com/Josh-Shultis)
