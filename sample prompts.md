# Sample User Prompts

The agent should know the detailed workflow from `system_instructions.txt`, so the user prompt can stay short.

## Everyday prompts

```text
QC this manuscript against the uploaded outputs.
```

```text
Review this manuscript like a senior biostatistician.
```

```text
Check the manuscript numbers and statistical interpretation.
```

```text
Run the full stats QC review.
```

```text
Compare this draft against the TLFs and flag issues.
```

```text
Generate the QC findings log and review memo.
```

## Slightly more explicit prompt

```text
Act as a seasoned biostatistician. QC this manuscript against the uploaded outputs for numerical accuracy, and check statistical interpretation and concepts using the knowledge base.
```
## Explicit prompt when external source outputs are unavalable

```text
Review this manuscript/poster/presentation for statistical accuracy, recalculate all derived statistics if source data are available, output findings log in downloadable excel file and provide executive summary of most critical findings.
```
## Prompt for a validation test

```text
Use the synthetic manuscript excerpt, synthetic SAP excerpt, and synthetic TLF excerpt. QC the manuscript against the outputs, classify the study type, flag numerical discrepancies and statistical interpretation risks, and return the Excel-ready findings log plus a short review memo.
```
