# Progress Tracker

Use this as the single source of truth for phase status and completion health.

## Phase status dashboard

| Phase | Status | Target date | Labs complete | Architecture complete | Evaluation passed |
|---|---|---|---:|---:|---:|
| AI/ML foundations | Not started |  | 0% | 0% | 0% |
| SageMaker | Not started |  | 0% | 0% | 0% |
| Bedrock | Not started |  | 0% | 0% | 0% |
| Enterprise RAG | Not started |  | 0% | 0% | 0% |
| Agentic AI | Not started |  | 0% | 0% | 0% |
| AI security | Not started |  | 0% | 0% | 0% |
| MLOps/LLMOps | Not started |  | 0% | 0% | 0% |
| AI platform | Not started |  | 0% | 0% | 0% |
| Portfolio | Not started |  | 0% | 0% | 0% |

## Status definitions

| Status | Meaning |
|---|---|
| Not started | No committed artifacts or labs |
| In progress | Active work; at least one artifact in flight |
| At risk | Likely to miss target date or quality thresholds |
| Blocked | Cannot proceed due to dependency/constraint |
| Complete | All Definition-of-Done criteria met |

## Weekly update log

| Week | Focus phase | Planned work | Completed work | Risks/blockers | Mitigation | Next week plan |
|---:|---|---|---|---|---|---|
|  |  |  |  |  |  |  |

## Quality gate summary

Track pass/fail against mandatory cross-phase checks.

| Gate | Latest phase reviewed | Result | Notes |
|---|---|---|---|
| Mandatory labs completed |  |  |  |
| Architecture artifacts complete |  |  |  |
| ADRs approved |  |  |  |
| Security controls documented |  |  |  |
| Evaluation thresholds met |  |  |  |
| Cost model documented |  |  |  |
| Runbook tested |  |  |  |
| Evidence linked in README |  |  |  |

## Program health KPIs

| KPI | Formula | Target | Current |
|---|---|---:|---:|
| Schedule adherence | Completed milestones / planned milestones | >= 90% |  |
| Lab completion rate | Completed mandatory labs / mandatory labs | >= 90% |  |
| Evaluation pass rate | Passed evaluations / total evaluations | >= 85% |  |
| Evidence completeness | Completed DoD items with linked proof / total DoD items | 100% |  |
| Rework rate | Reopened artifacts / closed artifacts | <= 15% |  |

## Escalation triggers

- Any phase remains **At risk** for 2 consecutive weekly reviews
- Any mandatory security/evaluation gate is failing for >1 week
- Any milestone slips by >1 week without approved replan