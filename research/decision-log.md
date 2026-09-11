# Decision log

## 2026-08-05 — Frontier refresh and technical-map synthesis

- Decision state remains `explore / synthesizing`; no topic is committed.
- Five targeted 2024–2026 query families were run for programming feedback, clarification, code-judge calibration/abstention, requirement alignment, and learning outcomes. OpenAlex and arXiv succeeded; Semantic Scholar returned HTTP 429 in all five runs and is recorded as a coverage failure.
- The global corpus increased from 2,934 to 3,096 records; six direct-neighbor full texts were added for analysis. Formal and preprint evidence remain separate.
- Material update: requirement understanding is now a direct, competitive technical frontier rather than only a conceptual motivation. ICSE 2026 Specine explicitly models specification identification/lifting/alignment; REA-Coder adds pre-generation alignment and post-generation verification. This weakens any novelty claim based only on “adding requirement awareness.”
- Material update: clarification, evidence-grounded rubric execution and calibrated abstention are also active frontiers. ClarifyMT-Bench, RULERS and CodeRefuser supply transferable techniques but do not yet close the student-code-feedback evidence chain.
- Current interpretation: the most defensible intersection is not a universal quality score, but a code-feedback evaluator meta-evaluation task with atomic requirements/claims, independent program evidence, perturbation tests, calibration and abstention. Learning value remains a later external criterion requiring student outcomes.
- Three competing routes remain: (A) CodeFeedbackBench evaluator benchmark, (B) ReqJudge requirement-aware evidence-grounded evaluator, and (C) ClarifyCode ambiguity/clarification benchmark. Provisional sequencing is A before B; C remains independent until closest-work and real-user validity tests discriminate it.
- Synthesis artifact: `research/round3_ai_output_quality_value/frontier-status-and-technical-map-2026-08-05.md`.
- Revisit triggers: pilot teacher-label reliability, simple-baseline headroom, closest-work overlap with CodeJudgeBench/Specine/REA-Coder, and access to independent student outcomes.


## 2026-08-04 — Science-first recentering for the next advisor progress report

- Decision state remains `explore / synthesizing`; no topic is committed.
- The previous evaluator-system formulation is retained only as possible later instrumentation. It no longer leads the research narrative because “build a better multi-source evaluator” is primarily an engineering objective unless it tests a new construct, mechanism, boundary condition, or causal relation.
- Current scientific puzzle: technical correctness, latent-need fit, preference, immediate helpfulness, and downstream value are often treated as interchangeable, but existing evidence shows that their proxies can diverge. The research should identify whether these are empirically distinct constructs, when they agree or disagree, and whether need fit explains outcomes beyond technical correctness.
- The advisor’s “hallucination is mismatch” idea is operationalized as reference-relative mismatch. Source faithfulness, world factuality, explicit-specification compliance, latent-intent fit, and downstream utility remain separate reference relations rather than one unvalidated score.
- Three candidates are retained: (A) construct/measurement science for AI programming feedback; (B) a causal study of immediate help versus unassisted transfer and retention; and (C) ambiguity detection, constraint recovery, and clarification as an independent measure of need understanding.
- Provisional presentation preference: use A as the measurement foundation and B as the strongest causal validation; retain C as an independent alternative or scoped sub-study. This is a reporting recommendation, not a commitment.
- Data boundary: public or controlled programming cases plus teacher pilot labels can support an initial measurement study. Claims about learning value require prospective student behavior, unassisted transfer, or delayed outcomes; expert preference alone is insufficient.
- Reporting artifact: `research/round3_ai_output_quality_value/advisor-progress-report-2026-08-04.md`.
- Revisit triggers: teacher annotation access, participant/course access, pilot construct reliability, baseline headroom, closest-work audit, and primary publication community.

### Venue and title correction

- The broad construct question is retained as an umbrella research problem, not recommended as a general CS paper title.
- General AI/software-engineering paper shapes now retained separately: `CodeFeedbackBench` for benchmark/meta-evaluation, `ReqJudge` for an evidence-grounded requirement-aware evaluator, and `ClarifyCode` for clarification-seeking under ambiguous programming requests.
- A randomized immediate-help-versus-learning study remains legitimate for computing-education/HCI venues, but should not be presented as an algorithm paper.
- Current CS-oriented preference is benchmark first, method second. This preference does not yet establish novelty or feasibility; closest-work search, label reliability and baseline headroom remain decision gates.

## 2026-08-04 — Working proposal narrows to student-code feedback evaluator

- Status remains `explore`; this is a working proposal for writing and feasibility discussion, not a final topic commitment.
- Recommended primary object: AI-generated diagnostic or instructional feedback grounded in student code, rather than a universal AI-content quality score.
- Recommended primary decision: whether a feedback item should be accepted for automatic display, rejected, or escalated to a teacher because evidence is missing or conflicting.
- Proposed contribution bundle: a claim-level benchmark with evidence lineage and paired perturbations; a multi-source evaluator combining executable/program-analysis evidence, code/student-process representations and LLM semantic reasoning; calibration and selective abstention; later external validation against repair, teacher action or unassisted outcomes.
- Data posture: phase A must be executable on public code/education resources and controlled fault injection; phase B adds a small teacher-labeled subset; phase C uses local or newly collected student outcomes only when access and governance are available.
- Innovation boundary: an indicator hierarchy, arbitrary weighted total, longer prompt or multi-agent pipeline is not treated as sufficient novelty without independent labels, strong baselines, risk/coverage evaluation and a falsifiable downstream claim.
- Revisit triggers: closest-work search finds an equivalent atomic-evidence + perturbation + selective-evaluation benchmark; teacher construct labels are unreliable; public-data replay fails; or simple test/late-fusion baselines dominate the proposed method under equal cost.

## 2026-07-27 — Third-round scope: AI output quality, requirement fit and value

- Decision state remains `explore`; no previous research family is promoted to a final topic.
- New decision: study the evaluation of AI-generated artifacts one level above code-specific benchmarks, then test whether the resulting protocol can be instantiated rigorously for generated/student code and programming education.
- Provisional separation: (1) need expression and clarification, (2) intent/constraint understanding, (3) specification satisfaction, (4) intrinsic artifact quality, (5) user–task fit, (6) downstream value/risk, and (7) evaluator validity. These layers may correlate but are not treated as interchangeable.
- The advisor's claim that “hallucination is matching degree” is retained as a falsifiable proposition. Searches must cover factuality/faithfulness, pragmatic relevance, instruction following and user utility, and must seek counterexamples such as pleasing falsehoods, truthful but irrelevant answers, and pedagogically harmful correct answers.
- A Turing-style source-indistinguishability test is treated as one candidate comparator, not the default definition of quality. Its ability to predict requirement satisfaction and downstream value must be established rather than assumed.
- Evidence posture: preserve the 2026-07-12/13 global corpus and notes; write immutable round-3 raw searches under `research/round3_ai_output_quality_value/`; add Chinese scholarly databases and official standards rather than relying only on English CS indexes.
- Revisit trigger: after cross-disciplinary search, full-text evidence notes, a claim-level matrix, explicit disagreement analysis, and at least three competing code/education experiment designs with falsification conditions.

## 2026-07-12 — Workspace initialized

- Decision: start in an exploratory state and retain educational learner/process evaluation, industrial/repository evaluation, and AI-assisted learning as competing branches.
- Reason: the user asked for a research landscape and diggable questions rather than premature commitment to a model or framework.
- Evidence standard: consequential claims require full-text locators; prediction, construct measurement, causal effect and decision utility are kept separate.
- Revisit trigger: after cross-source search, local-data audit and at least three falsifiable direction cards.

## 2026-07-12 — Local data changes the feasible question

- Decision: treat the university data as strong for longitudinal/process-aware validation, but not as an independent mastery ground truth.
- Evidence:
  - latest validated event export: 9,678 rows and 575 students; earlier cleaned snapshot: 17,584 events and 581 students;
  - 15,184 code submissions plus diagnosis, assistant and mastery-update events in the earlier snapshot;
  - substantial overlap with later assignment/exam tables supports future-performance validation;
  - knowledge-point aliases, `problem_id` alignment, cross-platform missingness and system-generated mastery fields require audit.
- Consequence: D01 must use teacher rubrics and future unaided/exam performance as external criteria, student/time/problem-isolated splits, leakage checks and missingness-aware ablations.
- Revisit trigger: if problem mapping or permission to link outcomes fails, narrow the unit from knowledge-point mastery to trace/report factuality and difficulty triage.

## 2026-07-12 — Historical L1–L4 hint effects are not identifiable

- Decision: do not estimate a four-level causal dose response from the current historical sample.
- Evidence: only 93 L1–L4 hint calls from 12 users, with self-selected use and no randomized assignment; missing telemetry and overlap/positivity are unresolved.
- Status: fatal blocker for the retrospective version of D04, not for a future micro-randomized or factorial intervention.
- Acceptable replacement designs: prospective randomization of timing × directness, or a smaller pilot that first establishes treatment overlap and logs independent post-hint outcomes.
- Revisit trigger: a new prospectively instrumented cohort, consent/governance approval, and enough assignments/students for power and subgroup checks.

## 2026-07-12 — First reproducible search and evidence pass completed

- Decision: use the corpus to support a provisional shortlist, not claim an exhaustive systematic review.
- Evidence: 45 immutable cross-source query runs, 992 result appearances and 688 deduplicated/verified corpus records; 40 balanced seeds and 499 additional title includes.
- Failures retained as failures: Semantic Scholar anonymous API returned HTTP 429; OpenAlex anonymous daily budget was exhausted in later runs; one arXiv connection failed. Crossref, ACL Anthology, OSF, publisher PDFs and arXiv full text were used to verify consequential records.
- Coverage retained: classic process data, education assessment reviews, programming knowledge tracing, AI-learning effects, code-generation benchmarks, repository tasks, LLM-judge meta-evaluation, non-functional quality and benchmark-validity counterevidence.
- Revisit trigger: before a formal review paper or proposal submission, repeat 2026/current-year searches, forward-snowball new seeds, add Chinese-language databases and document second-round saturation.

## 2026-07-12 — Provisional shortlist, no final commitment

- Decision state: `shortlist`.
- Current shortlist:
  1. `D01` — externally validated, process-aware student diagnosis;
  2. `D02` — meta-evaluation benchmark for LLM-generated student/code evaluation reports;
  3. `D03` — calibrated, abstaining hybrid judge for repository patches.
- Why these survive:
  - D01 exploits the local longitudinal dataset while addressing the literature’s construct-validity weakness.
  - D02 makes evaluator reliability itself the contribution and can be tested cheaply before training a large model.
  - D03 has strong public counterexample evidence (EvalPlus, CodeJudge, ISSTA judge study and PatchDiff) and a clear risk–coverage–cost evaluation.
- Alternatives retained:
  - `D04` — timing × L1–L4 × learner-state causal assistance study: high scientific value, but prospective-only under current data.
  - `D05` — decision-oriented multidimensional patch quality / time-consistent benchmark variance: long-term value, higher annotation, infrastructure and outcome-access cost.
- Explicit non-decision: a multi-agent pipeline by itself is not treated as a publishable scientific contribution; it must instantiate a validated construct or a falsifiable meta-evaluation claim.
- Cheap-test gate before commitment:
  - D01: 100–200 trajectories, two teacher raters, correctness-only versus process baselines, future unaided/exam criterion and calibration.
  - D02: 30–50 reports, atomized factual claims, teacher labels, order/verbosity/irrelevant-context perturbations and model-version repeats.
  - D03: about 100 public patches with semantic-preserving variants and controlled logic/security/performance faults; compare tests/static tools/LLM/hybrid under risk–coverage–cost.
- Open questions: teacher-annotation access; permission and privacy process; prospective randomization feasibility; public versus proprietary industrial target; thesis horizon, compute/API budget and preferred venue community.
- Revisit trigger: choose one primary direction only after the cheap tests reveal label reliability, baseline headroom, estimated effect/uncertainty and any fatal operational constraint.

## 2026-07-13 — Return to exploration; public evidence first

- Decision state: `explore`. The provisional `D01`/`D02`/`D03` shortlist is retired rather than carried forward as an implicit commitment.
- User rationale: the local OJ/university data has not yet exposed a compelling research question, the eventual landing context (education, industrial software engineering, or a cross-domain problem) remains open, and the next useful step is broad field learning.
- Data posture: public benchmarks, open repositories, published artifacts and reproducible environments are the primary research resources. The local data is only an optional, lightweight validation or transfer case and must not determine the question.
- Scope retained: software quality and maintainability; testing, mutation, fuzzing and program repair; code review; programming education and learning analytics; human–AI programming; code-LLM evaluation; repository agents; LLM judges; and benchmark/measurement science.
- Interpretation of “general evaluation”: do **not** assume that correctness, maintainability, learning, developer utility and repository-task success can be collapsed into a universal `0–100` score. A defensible cross-domain contribution is instead a reusable evaluator-validity protocol: define the unit, construct and decision; separate direct evidence from proxies; audit labels; combine partially independent evidence; calibrate uncertainty and abstention; stress-test semantic-preserving and controlled-fault perturbations; and report risk–coverage–cost plus environment/version lineage.
- External validity remains scenario-specific: educational evaluators ultimately need evidence such as future unaided transfer, retention and instructor judgment; industrial evaluators need patch behavior, complete tests/specifications, security/performance evidence and downstream review/rework/defect outcomes.
- Selection rule: no direction will be chosen during this learning pass. Revisit possible research families only after the field map, survey/classic/recent reading route, public-resource guide and explicit validity gaps have been studied.
- Evidence boundary: the second-round search is a reproducible broad orientation, not a claim of exhaustive systematic-review saturation; current agent/judge work remains a monitoring stream.

## 2026-07-13 — Broad orientation package completed

- Reproducible main search: 40 immutable round-2 query runs, 1,703 pre-filter appearances and 1,353 within-run deduplicated appearances. A checked foundational-seed pass produced a final global corpus of 1,629 records: 85 seeds, 1,009 title includes and 535 scope exclusions.
- Independent branch maps: traditional software quality/testing/APR/review; programming education/learning analytics/human–AI; and code LLM/repository-agent/evaluator research. Branch retrieval counts are reported separately and are not added to the global corpus because their searches overlap.
- Evidence depth: 15 new round-2 full texts (with extracted text), 31 paper notes overall, and 103 unique evidence-matrix claims with direct locators.
- Reusable public resources: 75 catalogued resources plus a cost- and construct-aware selection guide. Public availability is not treated as label validity or guaranteed reproducibility.
- Synthesis outputs: a seven-layer field taxonomy, 2023–2026 frontier/status review, nine-module reading syllabus, and ten unranked research families. No family is promoted to a shortlist.
- Search failures retained: Semantic Scholar anonymous requests returned HTTP 429; OpenAlex exhausted its anonymous quota in four late runs. These are coverage limitations, not zero-result evidence.
- Quality checks: the corpus/state/note/evidence/resource counts, local links and CSV structure were audited; the strict workspace validator completed with zero errors and zero warnings after corrections.
- Next decision gate: read across constructs and try small public-resource replications before choosing a primary community, target decision and research labor type.

## 2026-08-24 — AI-assisted PKT landing plan shortlisted

- Decision state: `shortlist`.
- Primary question: after controlling problem, KC, code, correctness and test evidence, determine whether Human-AI interaction has stable incremental predictive validity for later independent performance.
- Contribution order: observation validity -> representation validity -> dynamic-state modeling. A new AI-aware KT architecture is conditional on earlier gates, not assumed as the starting contribution.
- Data portfolio:
  1. CodeWorkout + TIKTOC for a reproducible traditional PKT/test-aware baseline;
  2. StudyChat + TutorTrace for public AI-dialogue and high-frequency telemetry pilots;
  3. repaired local multi-platform data for longitudinal, course-context validation;
  4. a small RECAP-style prospective collection for suggestion-to-code provenance and independent no-AI verification.
- Local-data boundary: the latest event stream (9,678 rows, 575 learners) supports a limited retrospective predictive study, but not a historical L1-L4 causal dose-response. Task linkage, message-level export, code joins, KC remapping, identity reconciliation and privacy controls are hard prerequisites.
- Experiment gate: begin with transparent baselines and nested feature tiers (traditional KT -> full programming evidence -> AI intensity -> AI behavior -> AI semantics). Advance to adaptors or structured state models only when out-of-learner/time/task gains are calibrated and stable.
- Evidence boundary: no model experiment or treatment-effect estimate was run in this round. Public-data availability was verified from official pages, papers and repositories where possible; access may change and must be frozen with license, date and hash before execution.
- Artifacts: `round4_ai_assisted_pkt_landing/研究计划落地完善与数据集评估_2026-08-24.md`, `dataset-evaluation-matrix.csv`, `local-data-audit-2026-08-24.md`, and the rendered Word proposal in `output/documents/`.
- Revisit trigger: complete the schema/linkage/privacy audit and the CodeWorkout/TIKTOC baseline replication; then decide whether the public AI pilot and local validation have enough outcome independence and sample support to justify a prospective cohort.

## 2026-08-26 — Cross-device state becomes repository-owned

- Decision: Git-tracked project files, rather than Codex chat history, are the authoritative source for current state and handoff between devices.
- Recovery order: read `AGENTS.md`, `EXPERIMENT.md`, `experiments/registry.csv`, `research/state.json`, the latest decision-log entry and the round-4 landing report before taking action.
- Repository boundary: synchronize the original research-plan PDF, reviewed proposal outputs, curated dataset evaluation, aggregate local-data audit and lightweight experiment metadata.
- Privacy boundary: student-level data, names/IDs, complete dialogues, submitted code, database exports, internal database tooling/configuration, credentials, full logs and large artifacts stay outside Git.
- Experiment discipline: each meaningful run receives an ID, frozen config, data manifest, code commit, result summary and notes; only decision-changing summaries are promoted to `EXPERIMENT.md`.
- Git policy: do not push automatically in future turns unless the user explicitly asks; this initialization request explicitly authorizes the initial synchronization.

## 2026-09-07 — Public-data feasibility and novelty reappraisal

- Decision state remains shortlist / E0; no model experiment has run.
- StudyChat v4 §4.1 already compares prior performance plus AI counts and dialogue acts; SQKT already uses questions beyond historical code. A simple feature-addition novelty claim is insufficient.
- Prefer independent-outcome incremental validity with strong available programming baselines, held-out learners/time and explicit label provenance. Retain behavior measurement and a prospective verification intervention as alternatives.
- Change sequencing: AI data access, outcome independence and linkage are immediate gates; full TIKTOC/OKT reproduction is not a prerequisite for auditing them.
- Correct StudyChat access to gated files and latest paper scope to 2,214 dialogues. Record TutorTrace website 664/eight versus paper v1 480/four separately; version relationship is unresolved.
- Add the Bassner classroom assessment package as a public measurement reference; do not mislabel it as a dialogue-KT dataset. ProgFeed remains a feedback-process fallback with lab-specific assignment and delivery caveats.
- Continuous grades require continuous-outcome metrics; a hidden test of AI-assisted code is not a learner's independent verification task. Non-significance alone does not establish zero incremental information.
- Historical local aggregate counts do not establish a usable sample or adequate precision; no database export or private-data change was made.
- Local profile was stale (round-3 explore); a dated current-scope preface now reconciles it with tracked round-4 shortlist state. Historical sections and decisions preserved.
- Evidence and source-review milestone: M20260907-001-direction-review; report at round4_ai_assisted_pkt_landing/方向评估与首轮验证建议_2026-09-07.md. Research corpus/notes remain local caches; portable conclusions and source locators are curated in round4.
- Coverage: bounded refresh with indexed-source rate limits and official full-text/metadata verification, not systematic-review saturation.
- Revisit triggers: StudyChat access and learner/code/grade linkage; TutorTrace release manifest; independent outcome policy; baseline incremental confidence intervals.

## 2026-09-09 — Discussion archive and renewed novelty exploration

- Decision: explore / E0; user remains unconvinced about novelty and requests one to two days of reading before commitment.
- Primary target: future AI-assisted programming competence under explicit tool conditions; unaided results auxiliary, not a universal dataset gate.
- Retain longitudinal prediction, behavior validity and cross-tool assessment as hypotheses. No architecture or synthetic sample budget frozen.
- Closest work includes SQKT, StudyChat, CoTutor, vibe coding proficiency and HAI-Eval. Synthetic student methods do not establish real learner validity.
- TutorTrace uist partly clarifies event counts, not all sample discrepancies; license, scrub confirmation and out-of-scope individual profiling remain access/use gates.
- Current archive and literature map dated 2026-09-09 supersede current-scope assumptions, preserving historical files and decisions.
- User explicitly requests GitHub synchronization of shareable discussion/research artifacts. No private data or database access.
- Artifact stage is synthesizing (schema allowed); decision_state is explore. Documentation milestone M20260909-001, no model completion claim.
- Integrity correction: the prior manifest hashed a mutable matrix without a separately committed dated snapshot; its historical hash no longer resolves to current bytes. Old manifest retained, limitation recorded in M20260909-001 notes; current matrix frozen by the new manifest. Future mutable artifacts need dated snapshots.

## 2026-09-09 — Current-state authority and archival boundary

- Decision: the 2026-09-09 discussion archive and literature map are the only current research-position documents. The 2026-08-24 landing proposal and 2026-09-07 direction review remain as historical evidence, not active plans.
- State correction: `research/state.json` now separates `stage: explore` from `experiment_stage: E0`; no model experiment is running or completed.
- Registry correction: local linkage audit is the next candidate gate; CodeWorkout/TIKTOC baseline is deferred until the reading/novelty gate or a specific falsifiable comparison requires it.
- Synchronization rule: changes to research positioning must update the current archive/map, `EXPERIMENT.md`, `state.json`, registry and this log together. Git never carries private data; cross-device recovery starts with `git pull --ff-only` and the fixed AGENTS reading order.

## 2026-09-11 — State semantics and immutable dated snapshots

- State semantics: keep `stage: synthesizing` for the research-artifact processing phase, `decision_state: explore` for the unresolved research direction, and `experiment_stage: E0` for the pre-model phase. These dimensions must not be collapsed into one value.
- Integrity correction: restore the 2026-09-07 direction-review report to the exact bytes referenced by `public-source-review-20260907.json`; historical explanatory text belongs in the round4 README, not inside a hashed snapshot.
- Handoff rule: dated research documents are immutable snapshots. A new research position creates new dated documents and updates `state.json` current pointers, `EXPERIMENT.md`, registry when needed, and this log. Old manifests and snapshots are not rewritten.
