# Later cohorts, derived views, and reuse

These entries describe saved historical use, not a newly assembled release.
No row-level email content is included. Counts describe the stated role and
must not be added as independent original messages.

| Collection or view | Recorded count and role | Important boundary |
|---|---|---|
| SpamAssassin easy ham | 2,100 accepted English legitimate references | Originally external exploratory scoring, not original training/calibration/locked roles |
| SpamAssassin hard ham | 234 accepted English legitimate references | Same corpus family as easy ham |
| SpamAssassin adaptation | 200 cut-selection and 2,134 holdout references | Reuses the same 2,334; legitimate-only, no new phishing-sensitivity estimate |
| Diverse-negatives v2 added ham | 1,400 training; 467 calibration; 467 holdout | Reuses the same 2,334; not a new independent source |
| Additional E-PhishLLM type 1 | 3,819 English positive references | Same source family; positive-only exploratory scoring |
| PhishFuzzer original seed download | 3,300 publisher-labelled rows: 1,126 phishing; 1,074 spam; 1,100 valid | Download composition is not the scored English cohort |
| PhishFuzzer English diagnostic | 2,156 retained: 1,072 phishing and 1,084 valid | 2,149 distinct subject/body strings; seven duplicate extra rows retained; no independent authorship adjudication |
| Three-part role rotation | 5,975 English cases; partitions 1,992 / 1,991 / 1,992 | Reuses PhishFuzzer diagnostic plus 3,819 additions; not a fresh independent source |
| Kuladeep development comparison | 1,472 English references: 889 phishing; 583 legitimate | Development evidence on previously seen data, not replacement locked test |
| Miltchev supplementary comparison | 100 distinct short bodies: 23 phishing; 77 safe | Publisher-labelled development comparison, not business-mail validation |
| Debian runtime workload | 12 English and 12 native-French bodies | Unlabelled runtime input; not a detection-accuracy cohort |
| Later English repair development | 5,260 records, 4,188 known groups | Historical training-allocation material plus authorized previously examined legitimate-mail development copy; five outer folds |
| Later translated-French text-component development | 3,150 records | Permitted historical training allocation; five outer folds; not complete framework evaluation |
| Greco repair diagnostics | Saved accounts report two repair runs each missing 211 and 478 of 732 phishing references respectively | Do not confuse security target with authorship/spam labels; full cohort inventory not certified by these positive counts |
| Colab internal research cohort | 836 English and 835 French records | Already examined during development; not added as new emails |
| Label-review sample | 180 reused calibration messages | Private review content and reviewer responses excluded; not certified independent annotation evidence |
| Enron Test 2b candidates | 2,000 provisional candidates; zero admitted in the cited preparation account | Not a scored Test 2b evaluation result |
| Perturbation and ablation views | Derived from existing study roles | Not independently acquired datasets |
| Synthetic runtime fixtures | Three encoder-invariance fixtures in the cited diagnostic | Not authentic email or accuracy evidence |

## PhishFuzzer components in the selected English diagnostic

| Publisher component | Phishing references | Legitimate references | Total |
|---|---:|---:|---:|
| CEAS_08 | 0 | 838 | 838 |
| Kaggle SpamAssasin.csv | 8 | 37 | 45 |
| Manual / DataPhish | 91 | 87 | 178 |
| Nazario | 973 | 0 | 973 |
| SpamAssassin.csv | 0 | 122 | 122 |

These labels identify components of one released seed, not five newly verified
independent corpora. Other downloaded spam components were not part of the
selected phishing/valid diagnostic. Spam is not automatically phishing.

Pinned seed source reference recorded in the project:
https://raw.githubusercontent.com/DataPhish/PhishFuzzer/1e21dd4edbe5c64694f156bf5318c97c7c80681c/PhishFuzzer_emails_original_seed_v1.json

This is a source pointer, not a redistribution grant.

## Coverage boundary

This inventory covers the original study and named later uses in the cited
saved accounts and praxis v58. Downloaded/screened candidates are not silently
promoted to used training/evaluation data. It is not a new exhaustive audit of
all filesystem archives, translation retries, or lifetime experiment history.

Evidence: source project's `DATASET_ASSEMBLY_AND_VALIDATION_ACCOUNT.md`;
`docs/DOWNLOADED_DATASET_METRICS_2026-10-08.md`; praxis v58 Appendix L.3,
Sections L.7 and G.9, and historical repair discussion.
