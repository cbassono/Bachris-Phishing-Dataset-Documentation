# Methods and reproducibility boundaries

## Data roles

Original training fits the encoder's three-class classification head; the
pretrained encoder itself remains frozen. Calibration/development supports
language-specific fusion, temperature fitting, and action-cut selection.
The original locked test is a final single-use assessment, not a fitting pool.

Original fusion development uses five class-stratified shuffled folds per
language (seed 42) with upstream components fixed, followed by a final stacker
fit on all calibration rows. This is **stacker CV**, not full-pipeline,
campaign-held-out, or source-held-out CV. The independent validity of the
original head cannot be inferred from stacker CV alone.

Later grouped five-fold development experiments are separately scoped. They
do not replace original frozen outcomes or create independent confirmation.
Temperature and threshold selection are development uses, not new validation.

## Recorded original pool fingerprints

These SHA-256 values are copied from saved provenance receipts, not newly
computed by reading sealed messages. They identify recorded file bytes; they
do not prove label truth, redistribution rights, or contamination freedom.

| Original source-project file | Recorded SHA-256 |
|---|---|
| `Bachris_Software/data/pools/train.jsonl` | `e3944f75a2772e154a15e928aef42587bf22414425cd5c2ba5fba013bc9b0331` |
| `Bachris_Software/data/pools/train.fr.jsonl` | `8bc32f402ed7391f6066e84664a8106805489f228f1a7c987df91a3d8011b018` |
| `Bachris_Software/data/pools/calibration.jsonl` | `25ff782b6bbbaa2f97379542bc4e3c164f59d51760bd7a33881b68587e65e5d0` |
| `Bachris_Software/data/pools/calibration.fr.jsonl` | `1f83e22497cb5dded06f75b803797c6f363d6630aac9066fb289bd527e8f3f28` |

Source receipts:
`Bachris_Software/data/reports/three_class_head_provenance.json` and
`Bachris_Software/data/reports/calibration_quality.json`.

The later CSV addition includes redacted French text from the original locked
allocation, alongside training and calibration. It does not release model
predictions or original record identifiers. The files were read only for export,
not rescored. No locked scoring should be repeated to build this release.

## Reconstruction is limited

Publisher links alone do not pin every upstream archive slice or recover exact
historical role membership. Some source URLs remain unverified, and raw content
is intentionally absent. Therefore this is a **reproducibility documentation
package**, not a claim that every experiment is reproducible from this
repository alone. Lawful source access, exact historical inputs, compatible
software/model versions, and original study restrictions still apply.

## Documentation integrity

`SHA256SUMS` fingerprints only the published documentation, not a redistributed
dataset. Verify downloaded documentation with:

```sh
sha256sum -c SHA256SUMS
```
