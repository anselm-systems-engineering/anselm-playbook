# Day-Zero Agreement Layer

> **Purpose:** the smallest founding contract for an ANSELM engagement — one
> table of terms, one closed list of cell types, one closed list of
> commitment types, and the oracle that checks them. Everything descriptive
> waits to be derived from conversation.
>
> **Consumer test:** every row and every type below must name the act that
> uses it. **Throw-away test:** the whole layer must be small enough to
> discard in an afternoon.

## Controlled terms

| Term | Aliases | Canonical meaning (one sentence) | Consumer |
| ---- | ------- | -------------------------------- | -------- |
| limp-home mode | failsafe mode | Locomotion state entered on single-point sensor failure | commitment checker |

## Cell types (closed)

```yaml
cell_types: [need, function, component, decision, constraint, interface]
```

## Commitment relation types (closed)

```yaml
relations: [satisfies, refines, constrains, conflicts, derives_from, decides]
```

## Oracle

A deterministic checker validates every cell (schema + vocabulary) and every
relation (closed types, references, domain/range). It runs mechanically;
it never judges by judgment. See the Tier 0–1 reference implementation:

- <https://github.com/anselm-systems-engineering/handoff-tax-experiment/tree/main/tier01>
