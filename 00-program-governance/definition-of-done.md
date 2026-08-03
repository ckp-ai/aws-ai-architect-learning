# Definition of Done (Phase Gate)

A phase is complete only when all mandatory gates are passed and evidence is linked.

## Mandatory completion criteria

- Study notes are complete
- Mandatory labs run successfully
- Infrastructure can be recreated through code
- Architecture diagrams are stored in the repository
- Relevant ADRs are approved
- Security controls are documented
- Evaluation tests meet defined thresholds
- Cost implications are documented
- A runbook exists
- Evidence is linked from the phase README
- Learner can explain the architecture without notes

## Gate checklist template

| Gate | Pass/Fail | Evidence link | Reviewer notes |
|---|---|---|---|
| Study notes complete |  |  |  |
| Mandatory labs successful |  |  |  |
| Infra reproducibility verified |  |  |  |
| Architecture views complete |  |  |  |
| ADRs approved |  |  |  |
| Security controls documented |  |  |  |
| Evaluation thresholds met |  |  |  |
| Cost model documented |  |  |  |
| Runbook available/tested |  |  |  |
| README evidence linkage complete |  |  |  |
| Verbal architecture defense completed |  |  |  |

## Minimum evidence pack by phase

| Artifact type | Minimum required |
|---|---|
| Study notes | All planned topic notes for phase |
| Labs | All mandatory labs with run output/proof |
| Architecture | Logical + deployment + security/trust view |
| Decisions | ADRs for critical pattern selections |
| Security | Controls mapping + threat model updates |
| Evaluation | Metrics, thresholds, and result summary |
| Operations | Runbook with failure/rollback guidance |
| Cost | Cost model with optimization notes |

## Evaluation threshold policy

- Every phase must define measurable thresholds before execution.
- Thresholds should include at least one **quality**, one **security/safety**, and one **cost/performance** measure.
- If any mandatory threshold fails, the phase remains **In progress** until remediation evidence is added.

## Exit decision

| Decision | Rule |
|---|---|
| Pass | All mandatory gates pass and evidence is complete |
| Conditional pass | Non-critical gaps exist with approved due date <= 1 week |
| Fail | Any critical gate fails or evidence is missing |

**Critical gates:** security controls, evaluation thresholds, and reproducibility.

## Sign-off

- **Learner:** __________________  **Date:** __________
- **Reviewer/Mentor:** ___________  **Date:** __________