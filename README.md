# BLACKBOX

**Forensic reconstruction of complex incidents.**

> What actually happened?

BLACKBOX explores how distributed evidence can be assembled into an inspectable incident narrative without pretending that incomplete evidence is complete.

## What it does

- collect incident evidence
- normalize events across systems
- correlate timelines
- reconstruct causal candidates
- preserve provenance and uncertainty
- produce an inspectable incident record

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