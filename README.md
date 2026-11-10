# Bachris phishing research — French dataset and documentation

**Downloadable redacted French text export, with dataset documentation.**

## Download the French CSV

[Download translated_french_redacted.csv](https://raw.githubusercontent.com/cbassono/Bachris-Phishing-Dataset-Documentation/main/data/translated_french_redacted.csv)

The UTF-8 CSV contains **5,732 stored French translations**, including subject
and body text, reference labels, source, and original study split:

- **Training:** 3,361 records.
- **Calibration:** 891 records.
- **Locked test:** 1,480 records.

Email addresses and detected credential-like strings were redacted. See
[export notes](FRENCH_CSV_EXPORT.md) for all transformations and limitations.
This is a text-bearing, redacted derivative, **not an exact benchmark copy**.
The presence of a public download does not establish blanket redistribution
permission or a license for every source. Underlying rights remain as documented.

This repository documents the sources, allocations, translated-French versions,
and reuse boundaries of the Bachris phishing-detector research, and supplies a
redacted export of its original French allocations. It is not a new independent
email collection or independently validated benchmark.

Related software: https://github.com/cbassono/Bachris-LLM-PhishSolution

## Contents

- [Dataset catalogue](DATASETS.csv): source families, roles, and source references.
- [Original allocations](PRIMARY_ALLOCATIONS.csv): source × language × role ×
  A/B/C/D counts, including all 5,732 original translated-French versions.
- [French translation documentation](TRANSLATED_FRENCH.md): original translation
  procedure, later variants, and evidence limits.
- [Later use and reuse](LATER_COHORTS.md): exploratory, repair, and runtime cohorts.
- [Methods and reproducibility](REPRODUCIBILITY.md): fitting/CV roles and
  source-pool fingerprints already recorded in the project.
- [Rights and privacy](RIGHTS_AND_PRIVACY.md): exclusions and redistribution limits.
- [CSV export notes](FRENCH_CSV_EXPORT.md): columns, redaction counts, and safety.
- `SHA256SUMS`: checksums of the public documentation files.

## Original-study language versions

| Role | English | Translated French |
|---|---:|---:|
| Head training | 3,600 | 3,361 |
| Calibration/development | 900 | 891 |
| Locked test | 1,495 | 1,480 |
| Total per language | 5,995 | 5,732 |

These are allocation counts, not a certified count of independent original
emails. Translations share ancestry with English-source records, and later
cohorts reuse some of the same material. Do not sum repeated uses as new emails.
The original translated-French total is not a project-wide total across every
subsequent translation experiment.

## Reference labels

- **A:** source-labelled LLM phishing.
- **B:** traditional-phishing references.
- **C:** source-labelled LLM legitimate email.
- **D:** human-legitimate references.

These are inherited reference/design labels, not independently verified
authorship or security truth for every message. Dataset source, claimed
authorship, and class are not fully crossed.

## Access and permitted use

Obtain source material from its publisher under the applicable terms. Public
download access does not establish permission to republish email bodies,
headers, attachments, or translations. Some catalogue entries have unresolved
source links or content rights; these are explicitly identified rather than
guessed.

The documentation was assembled from existing saved evidence. Preparing the CSV
read the stored French training, calibration, and locked-test files solely for
export and text screening. No training, cross-validation, new translation, model
inference, or evaluation metrics were run. Source-file hashes were unchanged
before and after export. This exposes previously used study data; it does not
create a fresh unseen validation set.
