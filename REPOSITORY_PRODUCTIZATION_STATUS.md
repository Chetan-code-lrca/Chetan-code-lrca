# Public Repository Productization — Implementation Status

Last reviewed: 2026-11-06

This page tracks the first implementation pass after the 46-repository inventory. It is not a declaration that every repository is production-ready. Each change remains in its own pull request unless noted otherwise.

## Pull requests created in this implementation

| Repository | Pull request | Scope | Validation status |
| --- | --- | --- | --- |
| NetraX | [#16](https://github.com/Chetan-code-lrca/NetraX/pull/16) | Do not return raw internal model/flow diagnostics to unauthenticated analysis clients; regression test | CI passed |
| NetraX Dashboard | [#4](https://github.com/Chetan-code-lrca/NetraX-dashboard/pull/4) | Check the actual API health endpoint and report connectivity separately from analysis state | Build passed |
| PhishGuard AI | [#8](https://github.com/Chetan-code-lrca/PhishGuard-AI-ImagineCup2026/pull/8) | Neutral validation states, avoid false “safe” state, document current browser-only heuristic scope | Python/JS test matrix passed |
| AI Study Coach Agents | [#27](https://github.com/Chetan-code-lrca/ai-study-coach-agents/pull/27) | Bound document ingestion; align OpenRouter configuration; disclose optional Azure Blob persistence and session-link risks | Streamlit smoke and targeted Python tests passed |
| Fallback Atlas | [#6](https://github.com/Chetan-code-lrca/fallback-atlas/pull/6) | Enforce streamed JSON byte limits before parse on public API write routes | API tests and build/deploy CI job passed; not a production security sign-off |
| Fit-Match AI | [#5](https://github.com/Chetan-code-lrca/Fit-Match_AI/pull/5) | Bound multipart upload size, validate JPEG/PNG/WebP signatures, reject unbounded request parsing | Unit tests and production build passed |
| StudyFlow AI | [#1](https://github.com/Chetan-code-lrca/studyflow-ai-enhanced/pull/1) | Prevent first-render localStorage write from erasing saved data; validate persisted collections | Unit tests, TypeScript check, and production build passed |
| GreenMile SPSU | [#1](https://github.com/Chetan-code-lrca/GreenMile-SPSU-2026/pull/1) | Document Firestore authorization, data-model, client-side scoring, and institutional deployment blockers | Android build passed; review itself is documentation-only |
| MyOrders | [#2](https://github.com/Chetan-code-lrca/myorders/pull/2) | Implement vehicle filters and amount sorting; label backend-dependent actions as demo-only | Android unit tests and debug build passed |
| Rajasthan Helper | [#3](https://github.com/Chetan-code-lrca/rajasthan-helper/pull/3) | Remove generated Python artifacts, add ignore rules/CLI tests, and verify multiple Python versions | Python 3.8, 3.11, and 3.13 matrix passed |
| Gyaanify | [#1](https://github.com/Chetan-code-lrca/gyaanify/pull/1) | Rebuild static site into a temporary directory and detect drift from committed deployment files | Generated-site consistency check passed |
| SkillSling Demo | [#6](https://github.com/Chetan-code-lrca/skillsling-demo/pull/6) | Make uploaded PDF excerpts participate in chat; bound extraction; remove unsafe detached Streamlit UI thread | Netlify preview checks only; Python tests not verified in CI in this run |
| Sentiment Analysis | [#3](https://github.com/Chetan-code-lrca/SentimentAnalysis/pull/3) | Enforce a 20,000-character inference limit in both UI and preprocessing helper | Python tests passed |
| Fake News Detection | [#2](https://github.com/Chetan-code-lrca/fake-news-detection-genai/pull/2) | Add reproducible train/evaluate/inference pipeline with train-only TF-IDF fitting and duplicate controls | Unit tests passed |
| n8n workflow exports | [#1](https://github.com/Chetan-code-lrca/chetanPA.github.io./pull/1) | Validate JSON structure, unique nodes, connection targets, inactive export state, and common secret formats | Workflow validation passed |
| Chetan portfolio | [#1](https://github.com/Chetan-code-lrca/chetanportfolio.github.io/pull/1) | Correct README file tree and explain GitHub Pages deployment | Documentation-only; no code CI expected |

## Earlier documentation and portfolio PRs

| Repository | Pull request | Scope |
| --- | --- | --- |
| NetraX Dashboard | [#3](https://github.com/Chetan-code-lrca/NetraX-dashboard/pull/3) | Remove citation artifacts and use reproducible frontend install instructions |
| Praxilume (Example2) | [#6](https://github.com/Chetan-code-lrca/Example2/pull/6) | Add Rust quickstart, build/test commands, install guidance, and external-tool boundaries |
| Bakehouse | [#2](https://github.com/Chetan-code-lrca/bakehouse/pull/2) | Disable WhatsApp order links until a valid shop number is configured; add number validation, message encoding tests, and CI | Node tests and Azure Static Web Apps PR build/deploy checks passed |
| Bakehouse | [#1](https://github.com/Chetan-code-lrca/bakehouse/pull/1) | Add shop configuration, local run, WhatsApp-order boundary, deployment checklist |
| AI project index | [#3](https://github.com/Chetan-code-lrca/AI-/pull/3) | Organize public project index and remove inaccessible private link |
| Profile repository | [#2](https://github.com/Chetan-code-lrca/Chetan-code-lrca/pull/2) | Add 46-repository inventory and phased productization standard |

All pull requests above remain unmerged. Draft PRs still require review and merge authorization from the repository owner.

## Existing PRs that overlap with this work

Do not merge both sides of these pairs without first consolidating them:

- **Fake News Detection:** [existing PR #1](https://github.com/Chetan-code-lrca/fake-news-detection-genai/pull/1) adds an offline inference CLI and tests; new [PR #2](https://github.com/Chetan-code-lrca/fake-news-detection-genai/pull/2) also changes `predict.py`, `README.md`, `requirements.txt`, and test/CI files as part of the training-pipeline work.
- **SkillSling:** [existing PR #5](https://github.com/Chetan-code-lrca/skillsling-demo/pull/5) removes the unsafe background Streamlit thread; new [PR #6](https://github.com/Chetan-code-lrca/skillsling-demo/pull/6) includes that same removal as part of the PDF retrieval implementation.
- **Rajasthan Helper:** existing [PR #1](https://github.com/Chetan-code-lrca/rajasthan-helper/pull/1) already adds a CLI test/workflow baseline, and [PR #2](https://github.com/Chetan-code-lrca/rajasthan-helper/pull/2) also edits the README. New [PR #3](https://github.com/Chetan-code-lrca/rajasthan-helper/pull/3) touches the same test, ignore, workflow, and README paths.

These were not merged or closed as part of this pass. Reviewers should consolidate or choose a single merge sequence before merging.

## Repositories deliberately left unchanged in this pass

- **RunMismatch / Example:** preserve the existing pre-registration and frozen research protocol. Do not alter hypotheses, outcomes, or analysis rules after registration.
- **Upstream projects/forks:** Streamlit, scikit-learn, imbalanced-learn, and OWASP Amass should retain upstream ownership, licensing, and release processes. Do not treat forks as original applications.
- **Course material:** NVIDIA Fundamentals of Deep Learning and GitHub Skills exercise repositories should preserve upstream notices and exercise structure.
- **Research/educational baselines:** Titanic Survival Prediction, low-level image feature extraction, RSNA Knee, Python AI, Solaris Expedition, and ARTEMIS already contain meaningful code structure, setup guidance, or tests. Their claims and use-cases should be reviewed individually rather than rewritten for uniformity.
- **Coursework repositories:** assignment templates and submitted documents should preserve the assigned brief and source materials; don't fabricate results or apply a blanket license to team submissions.
- **Personal sites:** keep profile/portfolio facts and personal contact details unchanged unless the owner specifically requests content edits.

## High-priority decisions before real-world deployment

| Repository | Current limitation that must remain visible |
| --- | --- |
| GreenMile | No Firestore Rules/server-side role enforcement or authoritative scoring yet. Do not store real student data until the security migration and Emulator tests are complete. |
| Fallback Atlas | Anonymous reporting, weak area-label throttling, race-prone counters, and retention/moderation gaps remain. Pilot-only. |
| Fit-Match AI | Public filesystem image storage and no user authentication/isolation remain. Do not accept private wardrobe photos in a shared deployment. |
| AI Study Coach | No account/tenant isolation; optional progress is keyed by a shareable session URL. Do not use with sensitive organizational data. |
| PhishGuard | Heuristic indicators are triage only; lower-risk is not proof of safety, and the demo is not a mail/web security control. |
| SkillSling | Local Ollama and session-scoped FAISS index; no organization accounts or durable document library. |
| Fake News Detection | Historical dataset labels are not truth labels; upstream dataset reuse rights are not established; not fact-checking. |
| MyOrders | Demo sample data only; no live booking, payment, invoice, or transport backend. |
| StudyFlow | Browser-local data only; no accounts, cloud sync, or backup service. |

## Rights and privacy blocker

The public `textbooks` repository contains many commercially published textbook PDFs. The repository does not record redistribution licenses or permission for those files. Do not add an open-source license to the archive or promote it as a public download library until each file's rights are verified. The repository owner should restrict public access or remove files that cannot be lawfully redistributed. Coursework repositories containing personal or team information should also be checked before continued public distribution.

## Scope and verification limits

The initial inventory covered 46 public repository roots and confirmed a README at each root. Detailed source review and changes were targeted at the repositories listed above; this page does **not** claim that all 46 repositories have had every file, dependency, deployment, and runtime path audited. Repositories without a PR were either left unchanged for provenance/safety reasons or remain in later audit waves.

A green CI check only proves the checks that ran. It does not mean a deployment is live, a cloud project is configured correctly, or an application is ready for an organization. Each project needs its own threat model, data policy, operational owner, and acceptance criteria before production use.
