# ChatGPT Deep Research: Completed Runs with Zero Displayed Searches and Citations

**In the runs documented here, ChatGPT Deep Research displayed “Research completed” with 0 searches and 0 citations while producing substantive, source-specific output. These observations do not establish whether retrieval occurred or identify an internal root cause.**

I investigated this from outside the product after Deep Research tasks on my account, which had previously been showing hundreds of searches and dozens of citations, began finishing with zero displayed searches and citations. I reduced the issue to a short three-central-bank prompt that explicitly told Deep Research to report failure if it retrieved no web sources. It reproduced the same completed-0/0 state across Plus and Free accounts, on desktop web and iOS, and again several days later. The reports neither displayed the requested citations nor reported failure. During one instrumented run, the ChatGPT client logged that the report contained citation markers but no content references. OpenAI Support later requested and received the sanitized network capture from that run; no technical explanation had been provided when this case study was published.

This repository is a privacy-limited public subset of the investigation. It also documents a separate completion problem: two larger reports silently skipped most of the requested programme scope. It does not measure how often either behavior occurs.

Read this page for the case, [CANARY.md](CANARY.md) for the reproduction protocol, [PRIOR-REPORTS.md](PRIOR-REPORTS.md) for external context, and the [evidence index](evidence/README.md) for provenance and limitations. The [run summary](data/runs-summary.csv) is a summary of the screenshots and exports, not separate evidence.

## From an operational baseline to completed 0/0

Nine historical runs on my primary Plus account displayed **2,835 searches and 477 citations** in total. Their preserved exports contained native citation-marker syntax. The [baseline contact sheet](evidence/historical/healthy-telemetry.png) retains the original completion-counter pixels, with labels outside each crop.

I call this an operationally “healthy” baseline: nonzero displayed provenance telemetry and citation-bearing export behavior. I did not independently validate factual correctness, completeness, or every research requirement. Several baseline reports expressly disclosed partial completion or reported browsing limits. Those disclosures matter when comparing them with later omissions.

In my recorded sequence, all six Batch-6 runs then displayed completed status with **0 searches and 0 citations**, after six to ten minutes. The [Batch-6 contact sheet](evidence/historical/batch6-telemetry.png) shows all six results. Their preserved exports contained substantive output but no native citation-marker syntax. Zero displayed searches does not establish zero source access.

| Recorded stage | Visible result | Qualification |
|---|---|---|
| Historical baseline, reported 24–25 October | Nine nonzero-counter results | Earlier source-bearing behavior, not a matched contemporary control |
| Batch 6, reported 25 October | Six completed 0/0 results | Ordering and chronology partly retrospective |
| Historical reduced task, reported 25–26 October | Completed 0/0 on desktop and native iOS | Account, plan, network, and input attribution have limits |
| Fresh captures, 29 October Karachi / 28 October UTC | Plus 4m/0/0; Free 3m/0/0 | Captured after the original private record was closed |
| Instrumented Plus run, 28 October 21:07 UTC | 2m/0/0 and a client warning | Network capture retained privately |

Dates come from my investigation records, not authenticated platform timestamps. Some historical screenshots were captured after execution, so filenames alone do not prove when runs began or in what order. I started some earlier runs close together, but the records do not establish meaningful overlap between 06c and 06d. I also ran 06e and 06f separately, and both showed the same completed-0/0 result. Simultaneous launching was therefore not necessary for the visible symptom; the record does not resolve whether earlier activity had any triggering effect.

## Reducing the task

The original tasks were large, so task complexity was an obvious explanation to challenge. I reduced them to this intended request:

> Compare the current policy rates of the U.S. Federal Reserve, European Central Bank and Bank of Canada using only their official websites. Give the latest decision date for each. You must use the live public web and include inline citations. If no web sources are retrieved, do not answer from memory; report that research failed.

This removed the private subject matter and much of the task's scope while retaining a live-web and citation requirement. It is a useful reduction, not an unpredictable-fact experiment: familiar or correct facts could come from paths other than retrieval during the run.

The [Free-B request capture](evidence/canary/free-b-prompt.png) visibly preserves the submitted prompt. For the other historical canary runs I have the shared prompt text but no capture of every submission, so I cannot prove that the wording was identical each time. The [Plus-A](evidence/canary/plus-a-result.png) and [Free-B](evidence/canary/free-b-result.png) result crops show substantive central-bank output alongside completed 0/0 telemetry.

The [Free-B export excerpt](evidence/canary/free-b-export-excerpt.md) contains official-domain links despite zero displayed citations. A generated URL or claim of source use is evidence of generated content, not a retrieval log. Plain URLs, exported citation markers, displayed citation counters, and client content-reference objects are distinct representations.

## Reproduction across conditions

Historical captures show the symptom on desktop web and in the [native iOS app](evidence/canary/ios-c-result.png), on my Plus account (A) and separate Free accounts (B and C). Another person reproduced it on their own Free account (D); that screenshot is not published. One attempt on B with Think enabled also returned 0/0, although its historical date remains unresolved.

Account identity, plan, and independence partly rely on the participants' reports. I used both Wi-Fi and a mobile hotspot during the A/B testing but did not preserve a per-run network mapping. The iOS screenshots themselves show Wi-Fi despite a contemporaneous mobile-data report, so the execution network for that run remains unknown. Different accounts or clients do not establish independent geography, backend routing, or rollout cohorts.

The same canary run through ChatGPT's separate Work surface on account A finished in about 19 seconds and showed official-source chips. I treat it only as a cross-surface contrast: no full export or retrieval trace is preserved, and the comparison does not establish equivalent infrastructure. Its ordinary Deep Research counters were not exposed.

Fresh runs after I closed the original private record show [Plus at 4m/0/0](evidence/fresh/plus-result.png) and [Free at 3m/0/0](evidence/fresh/free-result.png). Their full source screenshots visibly include the request and respective plan labels; identifying interface elements are excluded from these public crops. These are additional selected observations, not a measure of how often the issue occurs.

## Instrumented reproduction and client warning

A separate Plus canary completed at **2m/0/0** while I captured browser diagnostics. Approximate submission was **29 October 2026, 02:07:32 Asia/Karachi**, equivalent to **28 October, 21:07:32 UTC**. The [published image](evidence/fresh/plus-har-run.png) shows two unscaled crops from the same screenshot: the completed result and this console message:

```text
[deep-research] Report contains citation markers but no content references; rendering without inline citations.
```

The supported interpretation is narrow: **the client observed citation-marker structure without corresponding content references required for inline citation rendering**. It does not establish whether retrieval occurred, whether references existed earlier server-side, where a mismatch originated, or why search telemetry was zero. This does not conflict with the historical exports lacking citation-marker syntax: those were exported files from earlier runs, while this warning describes the client's in-browser rendering of a later run.

The sanitized HAR remains private vendor-support evidence. It is not included here, nor are request bodies, conversation identifiers, or unrelated console errors.

## Later check of the fresh-run facts

The canary was designed as a reduction, not as a freshness test. The three fresh completed-result screenshots were captured on 28 October UTC, corresponding to the early hours of 29 October in Karachi. Exact submission timing is preserved only for the instrumented run, at about 21:07 UTC. On 30 October 2026, I checked the policy claims in these reports against the central banks' official sites:

- The [28 October Federal Reserve statement](https://www.federalreserve.gov/newsevents/pressreleases/monetary20261028a.htm) was released at 2:00 p.m. EDT / 18:00 UTC and maintained the target range at 3.75%–4.00%. The range itself was already in force; the fresh fact was the October 28 decision to maintain it.
- The Bank of Canada [announced a 25-basis-point increase in the overnight-rate target to 2.50%](https://www.bankofcanada.ca/2026/10/fad-press-release-2026-10-28/). Its [public release time was 09:45 Eastern Time / 13:45 UTC on October 28](https://www.bankofcanada.ca/2026/10/fad-announcement-release-mpr-2026-10-28/).
- The [10 September ECB decision](https://www.ecb.europa.eu/press/pr/date/2026/html/ecb.mp260910~314e508016.en.html) set the main refinancing operations (MRO) rate at 2.65%, effective September 16. It was still the latest published ECB policy decision during the instrumented run; the [29 October decision](https://www.ecb.europa.eu/press/pr/date/2026/html/ecb.mp261029~9a493adf17.en.html) came later.

The instrumented 0/0 run therefore contained accurate information that had been published only hours earlier, including the Bank of Canada's same-day rate increase. The other two fresh reports contain the same checked policy facts, although I did not preserve exact submission times for those runs. This temporal freshness means the zero search counter should not be interpreted as proof that no current information reached the response. It still does not show how the information reached the model, whether a search or retrieval tool ran, why the counters were zero, or where citation references were lost.

## A separate scope-completion finding

I also compared complete preserved requests and outputs for two larger runs. In **6c**, three programmes were requested; the output materially addressed Politecnico di Milano while Paris-Saclay and KTH coverage was absent. In **6d**, four Aalto programmes were requested; the output materially addressed Computer Science without the separately required programme-specific research for the other three.

The Aalto request permitted shared D/E/F material. I do not count valid shared sections as omissions. Both outputs appeared completed without a clear declaration that the remaining programme scope had not been reached. This differs from baseline reports that openly disclosed partial work.

The [scope comparison](evidence/historical/scope-comparison.md) is a compact derived inspection record. Private briefs and complete report bodies are withheld, so it does not expose every source line needed to independently verify every absence. This secondary finding does not establish the same cause as the 0/0 symptom.

## Evidence and interpretation

| Level | What this record supports |
|---|---|
| Observation | Completed status with zero displayed searches and citations, source-specific generated text and links, differences in citation-marker syntax between exports, and the quoted client warning |
| Bounded inference | A large prompt is not required to produce the symptom; a single browser or account is unlikely to explain the whole record; a completed status and fluent, source-specific prose did not satisfy the research contract I requested. |
| Unresolved hypotheses | Retrieval failure, counter/display defects, lost citation references, plan- or route-dependent behavior (including any lighter Deep Research mode), usage-allowance state, shared service or cohort conditions, or several mechanisms together. |

I cannot establish whether retrieval happened, what the internal cause is, which model or route served the runs, or how often this occurs. Correct source facts verified later cannot prove earlier retrieval.

One material confound is plan and usage state. The non-Plus reproductions were on Free accounts, while the Plus 0/0 runs occurred after substantial Deep Research use on that account. I did not preserve the actual allowance state, and I have no matched healthy Chat Deep Research control from the same period, so I cannot determine whether plan or allowance state contributed.

The exact prompts for six historical baseline runs were not preserved, and I did not reconstruct them. The record is retrospective and selected, with incomplete timing and execution-condition records. Public crops intentionally omit private context; some rows rely on my reporting or privately held material. SHA-256 demonstrates consistency with the published checkpoint, not authenticity of displayed telemetry or factual correctness of research.

## Prior reports and contribution

Similar behavior was reported publicly before this investigation. Earlier reports already include small unrelated prompts, cross-account controls, and private HAR escalation. A 22 October post in a thread started in September also describes a three-central-bank comparison. I claim neither discovery nor a globally novel mechanism. [Dated reports and distinctions](PRIOR-REPORTS.md) identify the overlaps.

What this case adds is one investigation preserved end to end: a measured baseline, reduction to a small reproduction, fresh and instrumented observations, a later fact check, a separate scope-completion finding, and vendor escalation, with an explicit boundary between public and private evidence.

## Vendor status

As of 30 October 2026, I had contacted OpenAI Support and the case had been escalated. Support requested the sanitized HAR from the instrumented run to inspect conversation request IDs and response data associated with the missing citations, and I provided it through the secure sharing method Support requested. No technical explanation had been given. This is my account of the exchange; OpenAI has not confirmed a cause.

## Engineering lessons and what I would change

Evidence acquisition and interpretation need separate records. Screenshots establish displayed state; exports establish generated text; a ledger explains attribution. Copying one into another does not create corroboration. Completion, inspectable provenance, and requested scope should each have explicit acceptance checks.

My initial supporting checker became too dependent on natural-language interpretation. The investigation improved when I reduced it to explicit, deterministic provenance/telemetry checks and removed it from the central evidentiary claim. That scope reduction made its responsibilities clearer. Passing software tests checks implemented rules; it does not validate research quality. The checker is intentionally absent here.

I would search prior reports earlier, preserve exact run identifiers and timestamps from the start, establish a known-working control earlier, and design the public/private evidence boundary before collection. I would also preserve exact submitted inputs and UI/export pairs immediately, and avoid expanding semantic automation when explicit observations can answer the core question.

## Authorship and contact

**Waqas Sharif.** I ran the Deep Research tasks documented here, apart from one reproduction performed by another person. I collected and preserved the evidence, made the investigative and publication decisions, and handled the vendor escalation. I used AI tools extensively to organize the record, draft and review documents, and build the supporting checker and verification code. I checked the published claims against the preserved evidence and am responsible for them. Generated report excerpts are identified as AI output.

Text is licensed under [CC BY 4.0](LICENSE) and code/configuration under [MIT](LICENSE-CODE); screenshots, platform UI, and generated excerpts are excluded from those blanket grants as explained in the [evidence index](evidence/README.md).

Contact: `ma.sharif.waqas@gmail.com`
