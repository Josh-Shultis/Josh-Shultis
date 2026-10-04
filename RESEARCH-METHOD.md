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

## Evidence handling

Preserve originals. Analyze copies and record source filenames, hashes, timestamps with timezones, account labels, and relevant object/request IDs. Connect artifacts using content and identifiers rather than timestamp proximity alone. Keep negative results and conflicting observations.

For suspected data transfer, establish source and destination access separately and verify the receiving account can read the resulting data. For confirmation claims, record exactly what the user requested and what the interface displayed.

## Public research examples

Use synthetic data or material explicitly authorized for release. Include:

1. The question and scope.
2. Environment and dependency versions.
3. Controls and the single variable being tested.
4. Recorded observations with artifact references.
5. Narrow conclusion, limitations, and negative results.
6. Disclosure status with a primary public link when available.

Never publish credentials, session data, private reports, or another person's account information. Sanitizing a current file does not sanitize its Git history.

## Tooling and attribution

Automated checks assist review; they do not prove impact or replace inspection of evidence. Describe AI assistance and third-party components when they materially affect the work, and explain the implementation choices I can independently defend.

Vendor recognition, bounty payments, CVEs, and remediation claims belong in a portfolio only when supporting records can be cited or appropriately shared. A later failed test alone does not prove a patch.
