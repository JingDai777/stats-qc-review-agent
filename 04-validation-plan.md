# Validation Plan

Use synthetic test files before any production rollout.

## Test pack

Use:

- `test-data/synthetic_manuscript_excerpt.md`
- `test-data/synthetic_tlf_excerpt.csv`
- `test-data/synthetic_sap_excerpt.md`

## Validation prompt

```text
Use the synthetic manuscript excerpt, synthetic SAP excerpt, and synthetic TLF excerpt. QC the manuscript against the outputs, classify the study type, flag numerical discrepancies and statistical interpretation risks, and return the Excel-ready findings log plus a short review memo.
```

## Expected findings

Compare output against:

```text
sample-outputs/expected_qc_findings_log.csv
```

## Acceptance criteria

| Area | Pass condition |
|---|---|
| Checklist selection | Correctly identifies study type or states uncertainty |
| Numerical QC | Finds intentional mismatches in percentages, p-values, HRs, denominators |
| Interpretation QC | Flags unsupported subgroup and no-difference claims |
| Formatting QC | Flags p = 0.000 and inconsistent precision |
| Evidence grounding | Uses source locations and does not invent citations |
| Output format | Returns Excel-ready log and Word-style memo |
| Limitation handling | Marks missing evidence as Needs source evidence |

## Suggested release gate

Do not publish beyond a pilot group until the agent passes at least three validation cycles with different synthetic examples.
