# Translated-French documentation

## Original frozen-study allocations

The original study reports **5,732 translated-French language versions**:

| Role | A | B | C | D | Total |
|---|---:|---:|---:|---:|---:|
| Training | 600 | 600 | 1,200 | 961 | 3,361 |
| Calibration | 150 | 150 | 300 | 291 | 891 |
| Locked test | 250 | 247 | 500 | 483 | 1,480 |

`PRIMARY_ALLOCATIONS.csv` gives the corresponding source-level allocation.
These are English-source translations, **not native-French business email**.
In particular, 456 translated Nazario records supplement B training; they are
part of its 600 records, not 456 additional records above that total.

## Recorded original translation procedure

The original frozen-study account identifies local Argos English-to-French
translation. Its recorded procedure protects entities such as links and email
addresses before translation, restores them afterward, and checks entity-set
preservation. Preparation also included duplicate and language-quality checks.

Entity preservation does not certify full semantic fidelity, fluent natural
French, label truth, or equivalent performance on native-French business mail.
This release documents saved aggregate evidence; it does not rerun those checks.

## Later experiments are separate

Later project records include alternative translation-engine/decoding
diagnostics (including DeepL and Argos variants), parent-role audits, and a
**3,150-record translated-French text-component development cohort** drawn from
permitted historical training allocations. These are not automatically the
original frozen 5,732 versions and must not be pooled into one new dataset count.
The original-study provider claim must not be inferred from an arbitrary later
translation-engine report.

The later French component uses five outer development folds (630 assessment
records per fold, 2,520 fitting records per fold) with internal calibration.
It is not a complete repaired-framework evaluation or independent final test.

## Parent relationships and separation limits

French and English versions share source ancestry. Recorded source-bank
parent-role checks are narrower than an exhaustive comparison with every final
English role. Saved audits identify unresolved ancestry/grouping limitations;
this documentation does not certify global cross-language contamination freedom.

## What is public

Counts, source descriptions, processing descriptions, and aggregate provenance.
**No translated subjects, bodies, headers, attachments, row-level parent IDs,
or private reviewer material are included.** No project-wide total covering
every translation retry and later variant is certified here.

## Evidence

The source project retains the following evidence references (availability on
its public branch is not guaranteed):

- Praxis v58, Appendix L.3, original allocation and translation discussion.
- `DATASET_ASSEMBLY_AND_VALIDATION_ACCOUNT.md`, source-specific allocations.
- `outputs/research-results-2026-10-06/report.md`, original allocation tables.
- `Bachris_Software/data/reports/final/french_translation_provenance_audit.md`.
- `Bachris_Software/data/reports/translation_engine_audit.json`, a later,
  differently scoped engine diagnostic, not the original frozen composition.
