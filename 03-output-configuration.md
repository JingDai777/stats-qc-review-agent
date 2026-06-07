# Output Configuration

The agent should produce two default outputs for a completed QC review.

## 1. Excel-ready QC Findings Log

The findings log is the primary working output and the issue tracker.

Required tabs:

- Summary
- Conceptual_Stats_Review
- Numerical_Accuracy_QC
- Format_Style_QC
- Cross_Document_Checks
- Reviewer_Queries
- Resolution_Tracker

Required columns:

| Column | Meaning |
|---|---|
| Finding ID | Unique issue ID, such as STAT-QC-001 |
| Study Type | Oncology interventional, non-oncology interventional, observational, or unclear |
| Document | Manuscript, abstract, table, figure, SAP, TLF, etc. |
| Location | Exact location in the document |
| QC Domain | Numerical accuracy, statistical interpretation, formatting, cross-document consistency |
| Checklist Item | Related checklist item or module |
| Displayed Value or Text | Value or wording in the manuscript |
| Source Output/TLF Location | Source table, listing, figure, or output location |
| Source Value | Value from the source output |
| Recalculated Value | Agent recalculation if possible |
| Difference | Numeric or textual difference |
| Difference Type | Mismatch, rounding, denominator, missing evidence, overstatement, format |
| Issue | Concise description |
| Risk | Low, Medium, High, Critical |
| Recommended Fix | Correction or wording change |
| Owner | Statistician, programmer, medical writer, study team |
| Status | Open, In review, Resolved, Accepted as is |
| Verification Status | Not verified, Verified, Needs source evidence |
| Reviewer Notes | Optional notes |

## 2. Word-style Statistical QC Review Memo

The memo is the narrative summary for the study team.

Required sections:

1. Executive Summary
2. Documents Reviewed
3. Overall QC Assessment
4. High-Risk Statistical Interpretation Issues
5. Numerical Accuracy Findings Summary
6. Formatting and Presentation Findings Summary
7. Cross-Document Consistency Issues
8. Recommended Manuscript Wording Changes
9. Open Questions for the Study Team
10. Appendix: Detailed Findings Log Reference

## Automation option

For a pilot, chat output can be copied into Excel and Word. For production, use Power Automate or an equivalent workflow to create:

- `.xlsx` findings log
- `.docx` review memo
- Optional `.pdf` archive after human verification
