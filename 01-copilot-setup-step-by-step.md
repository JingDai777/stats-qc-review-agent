# Stepwise Instructions: Configure the Stats QC Review Agent in Copilot Studio

## 1. Create the agent

Agent name:

```text
Stats QC and Review Agent
```

Description:

```text
Reviews clinical study manuscripts against statistical outputs/TLFs for numerical accuracy, statistical interpretation, cross-document consistency, and formatting/precision issues. This is a human-in-the-loop QC aid, not final sign-off.
```

## 2. Add the core knowledge source

Add the file:

```text
checklists/Statistics_QC_Review_Checklists_Companion.docx
```

Name it:

```text
Core Statistics QC Companion
```

Description:

```text
Primary operational rubric for oncology interventional, non-oncology interventional, observational, numerical accuracy, formatting, and statistical interpretation QC.
```

## 3. Add optional markdown/CSV versions

LLM retrieval can work well with Markdown and CSV. Add these too if your platform supports multiple knowledge formats:

```text
checklists/stats_qc_checklists.md
checklists/stats_qc_checklists.csv
checklists/numerical_and_format_qc.md
checklists/numerical_and_format_qc.csv
```

## 4. Add supporting official guidance URLs

Use `guidance/guidance_urls.md` as the curated source list. Guidance should support interpretation, but source study documents should control study-specific QC decisions.

## 5. Enable file intake

Enable user file uploads or configure SharePoint/OneDrive study folders so the agent can access:

- Manuscript draft
- TLFs/statistical outputs
- Protocol
- SAP
- Style guide or table shells
- Listings, if available
- CSR or registry entry, if available

## 6. Paste core instructions

Paste the content of `system_instructions.txt` into the agent instructions box.

The important behavior is this:

```text
When the user asks to QC, review, check, validate, or compare a manuscript against uploaded outputs, interpret the request as a full statistical QC review, even if the prompt is brief.
```

## 7. Add starter prompts

Use the short prompts in `prompts.md`, especially:

```text
QC this manuscript against the uploaded outputs.
```

## 8. Create topic routes

Recommended topics:

| Topic | Trigger examples | Scope |
|---|---|---|
| Full Manuscript QC | QC this manuscript; Run stats QC; Compare against outputs | Complete review |
| Numerical Accuracy QC | Check numbers; QC against TLFs | Values, denominators, percentages, p-values, CIs |
| Statistical Concept Review | Review interpretation; Check statistical concepts | Estimands, multiplicity, missing data, subgroups, overclaiming |
| Format and Style QC | Check decimals; Check p-values; Check scientific notation | Formatting, precision, units, footnotes |
| Generate QC Deliverables | Create findings log; Create review memo | Excel-ready log and Word-style memo |

## 9. Configure output behavior

The agent should return:

1. Excel-ready QC Findings Log
2. Word-style Statistical QC Review Memo
3. Open questions or missing source evidence

Use `schema/qc_findings_log_schema.csv` and `templates/review_memo_template.md`.

## 10. Validate before production

Use the synthetic files in `test-data/` and compare against `sample-outputs/expected_qc_findings_log.csv`.

Do not publish broadly until the agent can:

- Select the correct checklist.
- Compare manuscript values to TLFs.
- Flag numerical mismatches.
- Flag overinterpretation.
- Avoid inventing source evidence.
- Produce a consistent findings log and review memo.
