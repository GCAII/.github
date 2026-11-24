# Global Constrained AI Initiative

An unincorporated research and conformance initiative for AI systems that run
under hard constraints.

It publishes one standard and indexes the author's research. There is no staff,
no funding, no membership, and no fees, and it does not certify, accredit, or
approve deployments.

## The standard

**GCAII-STD-0001 — Constrained On-Device AI Conformance Standard**

v1.0.0 · 2026-11-08 · [DOI 10.5281/zenodo.24089533](https://doi.org/10.5281/zenodo.24089533) · CC BY 4.0

It defines the minimum technical requirements for deploying sub-billion-parameter
language models on resource-constrained hardware with no runtime telemetry,
bounded volatile-memory use, and reproducible evidence. It covers inference
runtimes, local proxies, and packaging. It does not cover model training,
frontier-scale systems, or legal compliance.

Requirements are CORE or CONDITIONAL: 19 apply to every implementation, and 9
are gated by a capability the deployer declares. Cryptographic storage (section 5.6) is
conditional on `stores_data_at_rest`; a deployment that writes no prompt-derived
data reports those four requirements `not_applicable`, with evidence that the
data is absent. `not_applicable` is not a pass, a fail, or a skip.

28 requirements across seven sections:

| Section | Subject | Requirements |
|---|---|---|
| 5.1 | Runtime telemetry isolation | 4 |
| 5.2 | Memory isolation | 6 |
| 5.3 | Personal-data handling | 5 |
| 5.4 | Deterministic execution and reporting | 3 |
| 5.5 | Audit trail and remediation | 3 |
| 5.6 | Cryptographic storage | 4 |
| 5.7 | Supply chain | 3 |

Four requirements define the minimum scope: §5.1.1, §5.1.2, §5.1.4, and §5.2.1.
A report that does not evidence all four is not a report against this standard
at any level.

The specification ships with a JSON conformance-report schema over a closed set
of six capabilities, and with test vectors that include negative cases which
must be rejected.

- [Specification](https://github.com/GCAII/secretariat/blob/v1.0.0/specs/GCAII-STD-0001/spec.md)
- [Conformance model](https://github.com/GCAII/secretariat/blob/v1.0.0/specs/GCAII-STD-0001/conformance.md)
- [Report schema](https://github.com/GCAII/secretariat/blob/v1.0.0/specs/GCAII-STD-0001/schemas/conformance-report.schema.json)
- [Release record](https://github.com/GCAII/secretariat/tree/main/documents/releases/GCAII-STD-0001-1.0.0-2026-11-08)

## Wing repositories

| Repository | Holds | Start here |
|---|---|---|
| [`secretariat`](https://github.com/GCAII/secretariat) | the normative corpus: specification, schema, test vectors, release records, registry, and governance | [specification at v1.0.0](https://github.com/GCAII/secretariat/blob/v1.0.0/specs/GCAII-STD-0001/spec.md) |
| [`research`](https://github.com/GCAII/research) | an index of the author's published research, with DOI and BibTeX records | [README](https://github.com/GCAII/research#published-research) |

The repository is the source of truth for the text; the DOI record is the source
of truth for the version.

## Conformance

A conformance report is evidence about a tested configuration, not a
certificate. It names the deployer, the spec version, the declared capabilities,
and the tested environment.

| Level | State of the evidence |
|---|---|
| L1 | declared by the deployer |
| L2 | verified by a harness |
| L3 | independently reviewed |
| L4 | continuously verified |

The levels describe the state of the evidence, not the quality of an
implementation. L2 is not a higher grade than L1.

Declarations are recorded in
[`documents/registry.yaml`](https://github.com/GCAII/secretariat/blob/main/documents/registry.yaml).
At v1.0.0 the declarations list is empty. Recording is not approval.

## Status

| | |
|---|---|
| Current version | v1.0.0, published 2026-11-08 |
| Declarations recorded | none |
| Open comment window | none |
| Fees, membership, staff | none |

## Citing

Cite the version DOI for the version you used: `10.5281/zenodo.24089533`.
Repositories carry a [`CITATION.cff`](https://github.com/GCAII/secretariat/blob/main/CITATION.cff).

## Licence

Standards and governance corpus: CC BY 4.0. Code, when it lands: Apache-2.0.

## Author

Zeeshan Kayani · [ORCID 0009-0007-6506-1516](https://orcid.org/0009-0007-6506-1516) · [@zz-47](https://github.com/zz-47)

One author, named. No independent review.

## Contact

- Questions, corrections, and comments:
  [issues](https://github.com/GCAII/secretariat/issues)
- Security: [private advisory](https://github.com/GCAII/secretariat/security/policy)
- Correspondence: gcaii.secretariat@outlook.com

---

GCAII is the acronym for Global Constrained AI Initiative and is not affiliated
with any other organisation using the same letters.