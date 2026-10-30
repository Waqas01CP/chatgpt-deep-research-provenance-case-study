# Public evidence index and provenance

This is a deliberately small set of public derivatives. Originals remain privately preserved. Images contain platform UI and generated report content; new labels, contact-sheet framing, and derived summaries were prepared by the investigator with tool assistance. None is an independent product execution by a reviewer.

## Derivative rules

Originals were read only. Public images use deterministic rectangular cropping, lossless PNG encoding, and removal of unnecessary metadata. Retained UI pixels were not rescaled or generated. Labels sit outside the original crops; no generative image alteration was used. The iOS JPEG was decoded to RGB and saved as PNG, preserving the decoded crop pixels rather than the original compressed file bytes.

Browser tabs, sidebars, account details, private conversation identifiers, unrelated diagnostic output, and personal research material are excluded. The instrumented-run image contains two explicitly separated panels from one source capture; it is not a continuous original screenshot. Account labels in the full fresh sources are not included in the result crops, so public plan attribution relies on the investigator's source inspection/reporting.

Dates are reported execution labels unless otherwise stated. The reporting timezone is Asia/Karachi (UTC+5); filename, device-clock, transfer, and execution times are not interchangeable. Historical chronology is partly retrospective. Original private paths and diagnostic identifiers are intentionally omitted from this index.

Crop rectangles below use source-image pixels `(left, top, right, bottom)`, with right/bottom exclusive and origin at the upper-left corner. These document transformations without exposing private paths.

## Historical telemetry contact sheets

[healthy-telemetry.png](historical/healthy-telemetry.png) is assembled from nine separately preserved result screenshots. Original telemetry pixels are retained; run labels were added outside the crops. “Healthy” denotes nonzero displayed provenance telemetry, not validated research quality. Each crop contains only the completion/runtime/citation/search line; private report cards and conversation text are excluded.

| Private source category / run | Crop rectangle |
|---|---|
| Historical result, brief-01 | `(20,44,800,66)` |
| Historical result, brief-02 | `(12,35,790,58)` |
| Historical result, brief-03 | `(20,38,795,58)` |
| Historical result, brief-04 | `(20,45,790,66)` |
| Historical result, brief-05a | `(20,38,790,58)` |
| Historical result, brief-05b | `(20,38,800,60)` |
| Historical result, brief-05c | `(20,38,800,60)` |
| Historical result, brief-05d | `(20,43,830,65)` |
| Historical result, brief-05e | `(17,49,790,73)` |

[batch6-telemetry.png](historical/batch6-telemetry.png) contains six separate result captures showing completed status with zero displayed searches and citations. Their ordering follows the investigator's retrospective run record; capture filenames do not independently establish execution order. Labels are outside unscaled original telemetry crops.

| Private source category / run | Crop rectangle |
|---|---|
| Batch-6 result, brief-06a | `(29,48,805,69)` |
| Batch-6 result, brief-06b | `(40,40,850,60)` |
| Batch-6 result, brief-06c | `(56,45,829,67)` |
| Batch-6 result, brief-06d | `(22,39,800,60)` |
| Batch-6 result, brief-06e | `(29,42,820,64)` |
| Batch-6 result, brief-06f | `(20,42,820,64)` |

Both contact sheets support visible telemetry, not internal retrieval counts, verified execution times, or report quality. Labels are derived investigator attribution, not platform pixels.

## Other public derivatives

| Public artifact | Private source category and transformation | Supported claim and limits / origin |
|---|---|---|
| [scope-comparison.md](historical/scope-comparison.md) | Complete 6c/6d preserved requests and exports; manual derived coverage comparison, with personal details and full bodies withheld. | Investigator-authored summary of missing requested programme scope. All source lines needed to verify absence are not public; valid shared Aalto sections are respected. |
| [plus-a-result.png](canary/plus-a-result.png) | Historical Plus-A result, crop `(20,59,1005,455)`. | Platform completion 3m/0/0 with generated source-specific opening. Full submitted request is not captured here; plan/account attribution is partly operator-reported. |
| [free-b-prompt.png](canary/free-b-prompt.png) | Historical Free-B plan/request capture, crop `(310,39,852,218)`. | Investigator-submitted request inside platform UI. Unlike a shared template, this visibly preserves the submitted wording. Planner/start controls are omitted. |
| [free-b-result.png](canary/free-b-result.png) | Historical Free-B result, crop `(22,43,920,354)`. | Platform completion 4m/0/0 and generated report opening, paired by the investigator with the B request/export. |
| [free-b-export-excerpt.md](canary/free-b-export-excerpt.md) | Three Markdown link substrings extracted verbatim from the preserved B export table; surrounding report omitted; new explanatory framing. | Generated official-domain links despite zero displayed citations. Link existence or source-use wording does not establish retrieval or correct facts. |
| [ios-c-result.png](canary/ios-c-result.png) | Native iOS result JPEG, crop `(20,75,574,667)`, decoded RGB saved as PNG. | Platform completion 2m/0/0 with generated opening. Status bar/composer removed. Originals show Wi-Fi despite a mobile-data report; execution network remains unknown. |
| [plus-result.png](fresh/plus-result.png) | Phase-2 Plus source, crop `(382,478,1040,970)`. | Platform completion 4m/0/0 and generated result. Full original includes submitted request and Plus label; neither account identity nor private conversation UI is published. |
| [free-result.png](fresh/free-result.png) | Phase-2 Free source, crop `(338,383,1045,825)`. | Platform completion 3m/0/0 and generated result. Full original includes request and Free label. Think is highlighted in the source composer; that alone does not authenticate execution settings. |
| [plus-har-run.png](fresh/plus-har-run.png) | One Phase-2 diagnostic screenshot: result crop `(20,531,514,1018)` and warning crop `(535,1749,950,1779)` on a labeled new canvas. | Platform completion 2m/0/0, generated report, and verbatim client warning. Labels are investigator-added. Unrelated Network/console details and source-location label are excluded. Plus attribution and capture association also rely on operator records. |

The fresh instrumented run's approximate submission was 2026-10-29 02:07:32 Asia/Karachi / 2026-10-28 21:07:32 UTC. This is an investigator-recorded anchor, not a clock established by the cropped screenshot. The privately retained sanitized HAR and all support records are excluded. The warning establishes the client-observed rendering condition described in the [case study](../README.md), not its origin.

## Dataset dictionary

[runs-summary.csv](../data/runs-summary.csv) is a sanitized derived ledger containing 24 selected records: nine baseline, six Batch-6, five historical canary, one cross-surface contrast, and three fresh runs. It is not a frequency/prevalence dataset. Deleted artifact-free invocation attempts are excluded from completed-run records.

| Field | Meaning |
|---|---|
| `run_alias` | Public investigator-assigned alias; not a private conversation identifier. |
| `phase` | Historical baseline, Batch 6, canary, cross-surface contrast, or Phase 2. |
| `attributed_account_plan` | Anonymized account alias and operator-attributed plan. A/B were investigator-controlled; C was separately attributed on iOS; D was another operator. |
| `client` | Captured or reported client/surface; not a backend route. |
| `reported_date` | ISO reported execution date, or `unknown`. |
| `date_basis` | Attribution basis, not authenticated timing. Think's conflicting historical labels remain unresolved. |
| `displayed_runtime` | Visible runtime, not an absolute timestamp. Work uses a different “Worked for” display. |
| `displayed_status` | Visible completion wording, or `not_exposed`. |
| `displayed_searches`, `displayed_citations` | Captured counter values. `unknown` means insufficient knowledge; `not_exposed` means the relevant display was absent. Neither means zero. |
| `prompt_provenance` | Preserved input artifact, bundle-derived request, visible submission capture, shared-template attribution, or unavailable historical exact input. |
| `public_evidence` | Public path for supporting evidence, or `not_published`; does not imply all underlying artifacts are public. |
| `qualification` | Row-specific condition, publication, or provenance limit. |

Public summaries and labels were derived by the investigator; they are not additional independent witnesses. Historical baseline exports have native citation-marker syntax; preserved Batch-6 and historical canary exports lack it. The small published link excerpt alone cannot independently verify that whole-corpus comparison. Other-operator, Think, and Work captures are not published. No public file establishes independent backend sampling or matched contemporaneous controls.

## Integrity

SHA-256 demonstrates byte consistency against the published checkpoint; it does not establish authenticity of displayed telemetry or factual correctness of generated research.

[SHA256SUMS](../SHA256SUMS) covers every published file beneath `data/` and `evidence/`, including this index. These are public-derivative hashes, not private original hashes. On a Linux checkout, run `sha256sum --check --strict SHA256SUMS`. CI also checks exact manifest coverage and rejects duplicate paths. A changed file accompanied by a changed checkpoint requires substantive review; hashing is not a privacy detector or authenticity signature.

## Rights and publication boundary

Original investigator-authored narrative and derived summaries are under [CC BY 4.0](../LICENSE), to the extent applicable. Original code/configuration is under [MIT](../LICENSE-CODE).

Platform UI, screenshots, generated report excerpts where rights may be limited, trademarks, third-party material, and verbatim platform messages are excluded from blanket relicensing. Their inclusion documents observed product behavior and does not grant rights the investigator does not hold. Generated report content is identified as AI output, not presented as verified financial guidance or investigator-authored source research. No affiliation, endorsement, or jurisdiction-specific legal guarantee is implied.

This subset omits private identifiers, full large reports, raw briefs, diagnostic captures, support material, and another operator's screenshot. Withholding those originals limits independent public verification; publishing more private material would not remove the black-box limits.
