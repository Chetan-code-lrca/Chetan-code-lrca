# Public Repository Productization Roadmap

This document is the working quality plan for the public repositories in the Chetan-code-lrca account. It distinguishes deployable products from research, learning material, portfolio sites, and upstream projects. A repository must not be described as production-ready until its operational requirements have been tested.

## Productization standard

Every applicable project should have:

1. A precise problem statement, intended users, supported use cases, and explicit non-goals.
2. A reproducible installation path with supported OS/runtime versions and pinned or bounded dependencies.
3. A configuration reference and safe example configuration; secrets must never be committed.
4. A working quick start with expected output and a smoke test.
5. Architecture and data-flow documentation, including external services and trust boundaries.
6. Unit/integration tests and CI checks for the critical paths.
7. Operational guidance: deployment, upgrades, backups where applicable, logging, monitoring, recovery, and troubleshooting.
8. Security and privacy notes, data retention, permissions, and responsible-use boundaries.
9. License, attribution, dataset/model provenance, and third-party notices appropriate to the actual contents.
10. Contribution guidelines, issue reporting, release notes, and versioning appropriate to the project's maturity.

A checklist item is not considered complete merely because a document exists. It must be verified against the implementation.

## Portfolio inventory and intended treatment

### Product and application candidates

| Repository | Intended treatment | Priority |
|---|---|---|
| NetraX | Security analysis product; validate API, detector behavior, evidence, model provenance, resource limits and safe deployment | Critical |
| NetraX-dashboard | Frontend companion; validate API contract, configuration, accessibility, error states and deployment | High |
| fallback-atlas | Community resilience application; validate shared reporting, abuse controls, privacy, freshness and operational deployment | High |
| ai-study-coach-agents | Study assistant; validate each application surface, data isolation, provider behavior and deployment | High |
| PhishGuard-AI-ImagineCup2026 | Phishing analysis prototype; separate heuristic demo from ML/API capabilities and validate safe handling | High |
| Fit-Match_AI | Wardrobe/outfit application; validate uploads, file handling, privacy, API behavior and deployment | High |
| studyflow-ai-enhanced | Browser study application; validate local persistence, accessibility, data export and hosting | Medium |
| GreenMile-SPSU-2026 | Android sustainability app; validate Firebase rules, authentication, permissions, data integrity and release build | High |
| myorders | Android order-history demo; clearly separate sample data from real commerce functionality | Medium |
| bakehouse | Static digital menu/order-message builder; verify shop configuration and WhatsApp order flow | Medium |
| gyaanify | Static learning platform; validate content accuracy, navigation, accessibility and deployment | Medium |
| solar_exp | Educational browser game; validate controls, responsive behavior, performance and browser support | Medium |
| rajasthan-helper | Python CLI; validate package installation, API failure behavior, output and command tests | Medium |
| skillsling-demo | Local-model study assistant; validate Ollama setup, model compatibility, PDF handling and resource requirements | Medium |
| Praxilume (currently Example2) | Creative-engine control plane; validate permissions, adapters, protocols, persistence and upstream isolation | High |

### AI, ML and research projects

| Repository | Intended treatment |
|---|---|
| fake-news-detection-genai | Reproducible NLP baseline, dataset provenance, evaluation and inference interface |
| SentimentAnalysis | Reproducible classifier, preprocessing parity, model compatibility and inference tests |
| Titanic_Survival_Prediction | Beginner ML reference with reproducible pipeline and honest evaluation |
| low-level-image-feature-extraction | Reusable image feature library, documented descriptors, examples and numerical tests |
| rsna-knee-public | Reproducible medical-imaging research; strict research-only boundary and model/data provenance |
| pythonAI | Organised Python AI/ML examples with runnable instructions and tests |
| Example | Identify the actual intended product and validate its protocol, analysis and test boundaries before expanding scope |

### Developer, infrastructure and learning projects

| Repository | Intended treatment |
|---|---|
| agentic-ai-workshop | Reusable human-approval and risk-policy demonstration |
| artemis | Reproducible WSL2/Android emulator setup guide |
| programming-with-c-and-cpp-v2 | Structured course examples with compiler checks |
| CPP_using_OOP | Focused C++ learning example |
| Web-Technology | Runnable web examples with browser tests |
| Chetan-code-spsu-cse-module-1-tasks-1-10 | Organised coursework archive |
| Chetan-code-spsu-cse-module2-tasks-1-4 | Organised coursework archive |
| CT-DT-SPSU-CSE-A-CONCEPT-CRAFTERS-TASK-1-PRODUCT-FAILURE-ANALYSIS | Coursework/report archive |
| CT-DT-SPSU-CSE-A-CONCEPT-CRAFTERS-TASK-2-COMPLEX-PROBLEM-TABLE | Coursework/report archive |
| -CT-DT-SPSU-BATCH-NO-2-TEAM-3-TASK-1-PRODUCT-FAILURE-ANALYSIS- | Team coursework archive |
| skills-introduction-to-git | Completed GitHub Skills exercise; preserve exercise identity |
| skills-hello-github-actions | Completed GitHub Skills exercise; preserve exercise identity |
| textbooks | Audit redistribution rights and provenance before treating as a public resource library |

### Portfolio and personal sites

| Repository | Intended treatment |
|---|---|
| Chetan-code-lrca | GitHub profile and portfolio entry point |
| Chetan-code-lrca.github.io | TechSideHustle landing site |
| chetan.github.io | Identify current site identity and consolidate or clarify its purpose |
| chetanPA.github.io. | Personal-assistant configuration archive; audit secrets and privacy before publishing |
| chetanportfolio.github.io | Portfolio website |
| AI- | Public AI project index |

### Upstream repositories and course material

| Repository | Intended treatment |
|---|---|
| streamlit | Upstream fork; preserve upstream license, history and contribution workflow |
| scikit-learn | Upstream fork; preserve upstream license, history and contribution workflow |
| imbalanced-learn | Upstream fork; preserve upstream license, history and contribution workflow |
| amass | OWASP Amass upstream project; preserve original project identity and license |
| fundamentals-of-deep-learning | NVIDIA DLI course material; preserve course attribution, notices and license terms |

## Execution order

### Phase 1 — Safety and repository hygiene
- Inspect committed secrets, credentials, personal data, generated artifacts and oversized files.
- Audit licenses, third-party notices, datasets, model weights and media provenance.
- Identify broken links, missing setup files, stale instructions and misleading project claims.
- Do not delete user data or rewrite upstream history as part of cleanup.

### Phase 2 — Reproducibility
- Reproduce installation in a clean environment.
- Run existing tests and builds.
- Add missing smoke tests and CI checks for critical workflows.
- Record supported runtime versions and known failures.

### Phase 3 — Real-world readiness
- Validate authentication, authorization, input validation, rate limits and data handling where applicable.
- Add operational configuration, structured logs, health checks, monitoring guidance and recovery instructions where appropriate.
- Test deployment and rollback paths for deployable services.
- Document external dependencies and service costs.

### Phase 4 — Documentation and release quality
- Complete the project-specific README, architecture notes, examples and troubleshooting.
- Add contribution, security reporting and issue templates where justified.
- Use versioned releases and changelogs for software that is ready to be consumed.
- Publish screenshots or demos only when they accurately represent the current implementation.

## Licensing policy

Do not apply a blanket license to all repositories. For original code, choose and verify a license based on ownership and intended reuse. MIT may be suitable for some original standalone projects; Apache-2.0 may be preferable where explicit patent terms are desired. Coursework, team contributions, datasets, textbooks, model weights, media, upstream forks and third-party material require separate provenance and permission checks. No license should be added where ownership or redistribution rights are unclear.

## Definition of done

A project is complete only when its intended user can follow the documented setup on a clean supported environment, run a verified happy path, understand its limitations and data handling, and obtain help or report a defect through a documented route. Production readiness additionally requires a project-specific security, reliability and operational review.
