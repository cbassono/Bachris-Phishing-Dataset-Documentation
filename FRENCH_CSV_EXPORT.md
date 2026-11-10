# Downloadable French CSV

[Download the CSV](https://raw.githubusercontent.com/cbassono/Bachris-Phishing-Dataset-Documentation/main/data/translated_french_redacted.csv)

## Coverage

The export contains **5,732 records** from the three stored original French
study allocations: training **3,361**, calibration **891**, and locked test
**1,480**. All retain their original role, source, and A/B/C/D cell.
All 5,732 stored records identify their translation engine as `argos-local`.
No new translation was generated.

This is the complete original French role inventory, not all later translation
retries, DeepL alternatives, or subsequent repair variants. It is not a new
independent corpus. Do not use its training/calibration/locked names to imply
that data exposed in this public export remain unseen by future users/models.

## Columns

| Column | Meaning |
|---|---|
| `release_id` | New sequential public identifier, not an original row ID |
| `study_split` | Original role: training, calibration, or locked_test |
| `language` | fr |
| `cell` | Original A/B/C/D reference group |
| `reference_label` | Three-class reference derived from cell: A llm_phishing; B traditional_phishing; C/D legitimate |
| `stored_label` | Unmodified label field from the stored input; some phishing references use the broader phishing value |
| `source` | Stored source alias |
| `subject_fr` | Stored French subject after the public-export screening |
| `body_fr` | Stored French body after the public-export screening |
| `translation_engine` | Stored translation-engine metadata |
| `redaction_count` | Number of pattern-based removals/replacements in subject/body |
| `spreadsheet_escape_applied` | Whether a leading apostrophe was added to subject or body for spreadsheet safety |

Labels are inherited references, not independently verified authorship/security
truth. `reference_label` is not a fresh annotation.

## Changes from the stored research text

**545 rows** contain pattern-based redactions/removals:

| Detected category | Replacements/removals |
|---|---:|
| Email-address patterns | 1,676 |
| Provider-credential-like patterns | 2 |
| Credential-assignment-like patterns | 28 |
| Sensitive URL query parameters | 35 |
| JWT-like patterns | 1 |
| Disallowed control characters | 1 |

Credential-like matches are not claims that a credential was valid.
Email and credential patterns are replaced by category placeholders.
Headers, attachments, original row IDs, and parent mappings are excluded.
No rows were dropped.

**124 rows** have a spreadsheet escape applied. Text fields whose first
non-whitespace character is `=`, `+`, `-`, or `@` receive a leading apostrophe
to reduce formula-injection risk. Both subject and body must be treated as text
when importing into Excel. These fields may therefore differ from the original
even when `redaction_count` is zero.

The file uses UTF-8 with a BOM, comma delimiters, standard CSV quoting and
quoted multiline body fields. In Excel, import using **Data → From Text/CSV**,
select UTF-8 and comma delimiter, and keep text columns as text.
Use a CSV parser to count records; physical line count is not record count.

## Verification and limitations

- Exported CSV reopened and verified to contain 5,732 unique release IDs and
  exact expected split counts.
- The same credential/email patterns were checked against the exported text.
- Original input-file SHA-256 values matched before and after export.
- No training, inference, CV, metric computation, or locked-test rescoring ran.
- **This is not complete anonymization or a guarantee that no sensitive content
  remains.** Names, organizations, technical details, and URLs may remain.
- Redaction changes model inputs. Historical benchmark scores were measured on
  the research originals, not this derivative; do not claim exact metric replay.
- Licenses and unresolved source permissions are described in
  [RIGHTS_AND_PRIVACY.md](RIGHTS_AND_PRIVACY.md). A public link does not resolve
  those rights.

SHA-256 of `data/translated_french_redacted.csv`:

`8f0612d7a5955b3a1f818db6c113cb923017ffb0de18ef61ea174eb7ad8d2103`
