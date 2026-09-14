# BLACKBOX Architecture

BLACKBOX builds an inspectable incident record from distributed evidence.

## Flow

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
          EVIDENCE      UNCERTAINTY
             │             │
             └──────┬──────┘
                    ▼
             FORENSIC RECORD
```

## Design principles

1. Evidence and interpretation remain separate.
2. Every conclusion retains provenance.
3. Missing evidence is visible.
4. Competing explanations can coexist.
5. The final incident record should be reproducible from its evidence set.