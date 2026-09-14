# BLACKBOX

**Forensic reconstruction of complex incidents.**

> What actually happened?

BLACKBOX explores how distributed evidence can be assembled into an inspectable incident narrative without pretending that incomplete evidence is complete.

## Why it exists

After a serious incident, the important problem is often reconstruction: evidence is distributed across logs, metrics, changes, snapshots, and systems with different clocks and levels of reliability.

BLACKBOX turns that evidence into an inspectable record while keeping **provenance, gaps, uncertainty, and competing explanations** visible.

## What it does

- collect incident evidence
- normalize events across systems
- correlate timelines
- reconstruct causal candidates
- preserve provenance and uncertainty
- produce an inspectable incident record

## Use cases

| Use case | Question answered |
| --- | --- |
| Incident review | What actually happened? |
| Timeline reconstruction | In what order did observable events occur? |
| Evidence preservation | What supports each part of the reconstruction? |
| Post-incident analysis | Which explanations are supported or contradicted? |
| Audit / forensics | Can another investigator inspect the reasoning? |

## Architecture

```text
LOGS + EVENTS + METRICS + CHANGES + SNAPSHOTS
                    │
                    ▼
             EVIDENCE NORMALIZATION
                    │
                    ▼
              TIMELINE CORRELATION
                    │
                    ▼
             INCIDENT RECONSTRUCTION
                    │
             ┌──────┴──────┐
             ▼             ▼
          EVIDENCE       UNCERTAINTY
             │             │
             └──────┬──────┘
                    ▼
            FORENSIC RECORD
```

## Ecosystem

BLACKBOX sits after TRACE in the investigation chain and provides evidence-rich context to RECOVER and FIRSTLIGHT.

## Status

Early research and architecture.

- [Architecture](docs/architecture.md)
- [Roadmap](docs/roadmap.md)

## License

MIT.