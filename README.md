# Bachris phishing research — dataset documentation

**Documentation-only public release. No email text is distributed.**

This repository documents the sources, allocations, translated-French versions,
and reuse boundaries of the Bachris phishing-detector research. It is not a new
email corpus, not an independently validated benchmark, and not permission to
redistribute the underlying messages.

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

The aggregate documentation was assembled from existing saved evidence.
No training, cross-validation, translation, scoring, or locked-test access was
performed to prepare this release. Original study/model artifacts were not
changed. Exact message-level reconstruction is not provided by this repository.
