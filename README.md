# ChatGPT Deep Research: Completed Runs with Zero Displayed Searches and Citations

**In the runs documented here, ChatGPT Deep Research displayed “Research completed” with 0 searches and 0 citations while producing substantive, source-specific output. These observations do not establish whether retrieval occurred or identify an internal root cause.**

I ran or coordinated this black-box reliability investigation after research tasks on my account began returning that combination. I preserved screenshots, available requests, and exports, then reduced the task and compared selected conditions. This repository presents a small public subset of that record. It documents an externally observable provenance problem and a separate scope-completion problem; it is not a measurement of product-wide reliability.

Read this page for the case, [CANARY.md](CANARY.md) for the reproduction protocol, [PRIOR-REPORTS.md](PRIOR-REPORTS.md) for external context, and the [evidence index](evidence/README.md) for provenance and limitations. The [run summary](data/runs-summary.csv) is a derived ledger, not an independent witness.

## From an operational baseline to completed 0/0

Nine historical runs on my primary Plus account displayed **2,835 searches and 477 citations** in total. Their preserved exports contained native citation-marker syntax. The [baseline contact sheet](evidence/historical/healthy-telemetry.png) retains the original completion-counter pixels, with labels outside each crop.

I call this an operationally “healthy” baseline: nonzero displayed provenance telemetry and citation-bearing export behavior. I did not independently validate factual correctness, completeness, or every research requirement. Several baseline reports expressly disclosed partial completion or reported browsing limits. Those disclosures matter when comparing them with later omissions.

In my recorded sequence, all six Batch-6 runs then displayed completed status with **0 searches and 0 citations**, after six to ten minutes. The [Batch-6 contact sheet](evidence/historical/batch6-telemetry.png) shows all six results. Their preserved exports contained substantive output but no native citation-marker syntax. Zero displayed searches does not establish zero source access.

| Recorded stage | Visible result | Qualification |
|---|---|---|
| Historical baseline, reported 24–25 October | Nine nonzero-counter results | Earlier source-bearing behavior, not a matched contemporary control |
| Batch 6, reported 25 October | Six completed 0/0 results | Ordering and chronology partly retrospective |
| Historical reduced task, reported 25–26 October | Completed 0/0 on desktop and native iOS | Account, plan, network, and input attribution have limits |
| Fresh runs, 29 October | Plus 4m/0/0; Free 3m/0/0 | Separate Phase-2 captures |
| Instrumented Plus run, 29 October | 2m/0/0 and a client warning | Network capture retained privately |

Dates describe the investigator's reporting record, not authenticated job clocks. Historical screenshots were sometimes collected after execution; their filenames do not independently establish onset or ordering. I make no claim of meaningful simultaneous overlap for 6c/6d. Standalone executions are operator-recorded, which weakens concurrency as necessary at manifestation while leaving earlier triggering effects unresolved.

## Reducing the task

The original tasks were large, so task complexity was an obvious explanation to challenge. I reduced them to this intended request:

> Compare the current policy rates of the U.S. Federal Reserve, European Central Bank and Bank of Canada using only their official websites. Give the latest decision date for each. You must use the live public web and include inline citations. If no web sources are retrieved, do not answer from memory; report that research failed.

This removed the private subject matter and much of the task's scope while retaining a live-web and citation requirement. It is a useful reduction, not an unpredictable-fact experiment: familiar or correct facts could come from paths other than retrieval during the run.

The [Free-B request capture](evidence/canary/free-b-prompt.png) visibly preserves the submitted prompt. Generated copies of the shared canary template do not prove identical submitted bytes in every historical execution. The [Plus-A](evidence/canary/plus-a-result.png) and [Free-B](evidence/canary/free-b-result.png) result crops show substantive central-bank output alongside completed 0/0 telemetry.

The [Free-B export excerpt](evidence/canary/free-b-export-excerpt.md) contains official-domain links despite zero displayed citations. A generated URL or claim of source use is evidence of generated content, not a retrieval log. Plain URLs, exported citation markers, displayed citation counters, and client content-reference objects are distinct representations.

## Reproduction across conditions

Historical captures show the symptom on desktop web and in the [native iOS app](evidence/canary/ios-c-result.png), attributed to Plus A and separate Free B/C accounts. A further reproduction was supplied by another operator; its screenshot is deliberately excluded from public V1. One Think-enabled historical attempt on B also returned 0/0, but its execution date is unresolved. This does not establish that Think can never affect the outcome.

Account identity, plan, and independence partly rely on operator reporting. A/B network switching lacks per-run pairing. The original iOS captures show Wi-Fi despite a mobile-data report, so execution connectivity remains unknown. Different accounts or clients do not establish independent geography, backend routing, or rollout cohorts.

A separate Work/web result on A showed official-source chips. I treat it only as a cross-surface contrast: no full export or retrieval trace is preserved, and equivalent infrastructure is unestablished. Its ordinary Deep Research counters were not exposed.

The later Phase-2 captures show [Plus at 4m/0/0](evidence/fresh/plus-result.png) and [Free at 3m/0/0](evidence/fresh/free-result.png). Their full source screenshots visibly include the request and respective plan labels; identifying interface elements are excluded from these public crops. These are additional selected observations, not a sampling denominator or evidence that every user would reproduce the issue.

## Instrumented reproduction and client warning

A separate Plus canary completed at **2m/0/0** while I captured browser diagnostics. Approximate submission was **29 October 2026, 02:07:32 Asia/Karachi**, equivalent to **28 October, 21:07:32 UTC**. The [public derivative](evidence/fresh/plus-har-run.png) explicitly separates two unscaled crops from one preserved screenshot: the result and this client console message:

```text
[deep-research] Report contains citation markers but no content references; rendering without inline citations.
```

The supported interpretation is narrow: **the client observed citation-marker structure without corresponding content references required for inline citation rendering**. It does not establish whether retrieval occurred, whether references existed earlier server-side, where a mismatch originated, or why search telemetry was zero. The historical export observation and this later client message concern different representations and executions.

The sanitized HAR remains private vendor-support evidence. It is not included here, nor are request bodies, conversation identifiers, or unrelated console errors. Capture existence does not itself establish any internal mechanism.

## A separate scope-completion finding

I also compared complete preserved requests and outputs for two larger runs. In **6c**, three programmes were requested; the output materially addressed Politecnico di Milano while Paris-Saclay and KTH coverage was absent. In **6d**, four Aalto programmes were requested; the output materially addressed Computer Science without the separately required programme-specific research for the other three.

The Aalto request permitted shared D/E/F material. I do not count valid shared sections as omissions. Both outputs appeared completed without a clear declaration that the remaining programme scope had not been reached. This differs from baseline reports that openly disclosed partial work.

The [scope comparison](evidence/historical/scope-comparison.md) is a compact derived inspection record. Private briefs and complete report bodies are withheld, so it does not expose every source line needed to independently verify every absence. This secondary finding does not establish the same cause as the 0/0 symptom.

## Evidence and interpretation

| Level | What this record supports |
|---|---|
| Observation | Displayed completion/counters, generated source-specific text and links, export-marker differences, and the quoted client message |
| Bounded inference | Large prompt complexity is unnecessary at manifestation; one browser/account is weakened as a complete explanation; completed status and prose do not satisfy my requested research contract |
| Unresolved hypothesis | Retrieval failure, counter/display defects, provenance propagation problems, route-dependent behavior, account/allowance state, shared service/cohort conditions, or multiple mechanisms |

I cannot establish retrieval or its absence, an internal root cause, a particular lightweight/fallback model, quota causation, prevalence, or effects on all users. Correct source facts verified later cannot prove earlier retrieval. Allowance state and internal routes were not measured, and no matched contemporaneous healthy Chat Deep Research control was preserved.

Six historical exact requests remain unavailable. The dataset is retrospective and selected, with incomplete timing and execution-condition records. Public crops intentionally omit private context; some rows rely on investigator reporting or privately held material. SHA-256 demonstrates consistency with the published checkpoint, not authenticity of displayed telemetry or factual correctness of research.

## Prior reports and contribution

Similar behavior was reported publicly before this investigation. Earlier reports already include small unrelated prompts, cross-account controls, and private HAR escalation. A prior central-bank comparison also appears in the September community thread. I claim neither discovery nor a globally novel mechanism. [Dated reports and distinctions](PRIOR-REPORTS.md) identify the overlaps.

This case contributes a preserved, privacy-limited investigation record: the baseline, six-run cluster, task reduction, qualified condition comparisons, fresh Plus/Free observations, client warning, separate scope finding, and engineering lessons. Its contribution is that inspectable case record rather than proof that these investigative methods or symptoms are new.

## Engineering lessons and what I would change

Evidence acquisition and interpretation need separate records. Screenshots establish displayed state; exports establish generated text; a ledger explains attribution. Copying one into another does not create corroboration. Completion, inspectable provenance, and requested scope should each have explicit acceptance checks.

My initial supporting checker became too dependent on natural-language interpretation. The investigation improved when I reduced it to explicit, deterministic provenance/telemetry checks and removed it from the central evidentiary claim. That scope reduction made its responsibilities clearer. Passing software tests checks implemented rules; it does not validate research quality. The checker is intentionally absent here.

I would search prior reports earlier, preserve exact run identifiers and timestamps from the start, establish a known-working control earlier, and design the public/private evidence boundary before collection. I would also preserve exact submitted inputs and UI/export pairs immediately, and avoid expanding semantic automation when explicit observations can answer the core question.

## Vendor status and authorship

As of **30 October 2026**, the case had been escalated through OpenAI Support. Support subsequently requested the privately retained sanitized HAR to inspect conversation request IDs and response data associated with the missing citations. The HAR was provided through the requested secure sharing method; a technical explanation was still pending. This is an investigator-reported support status, not engineering confirmation of a root cause.

I collected or coordinated the underlying observations and take responsibility for this account. AI assistance supported organization, analysis, and drafting; tool-generated prose is not independent evidence. Generated report excerpts are identified as such. [Evidence provenance and rights](evidence/README.md) explain the public subset; original authored text is licensed under [CC BY 4.0](LICENSE), and original configuration/code under [MIT](LICENSE-CODE), with evidence exclusions.

### Contact

For questions about this case study or related AI reliability work: `ma.sharif.waqas@gmail.com`
