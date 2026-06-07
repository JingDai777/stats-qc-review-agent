# Numerical Accuracy and Format QC Modules

## Numerical Accuracy QC

| # | Check | Why | Evidence | Checked |
|---:|---|---|---|---|
| 1 | Source-to-output traceability | Each manuscript value should trace to a source output or listing. | TLF number, listing, analysis dataset, output path. |  |
| 2 | Denominator and percentage recalculation | Incorrect denominators or rounding are common manuscript QC issues. | n/N values, table denominators, recalculated percentages. |  |
| 3 | Summary statistic verification | Means, SDs, medians, ranges, and IQRs can be transcribed incorrectly. | TLFs, analysis output, listings. |  |
| 4 | CI, p-value, and effect estimate verification | P-values, CIs, HRs, RRs, ORs, and differences drive conclusions. | Primary and secondary endpoint TLFs. |  |
| 5 | Time-to-event output checks | KM estimates, events, censoring, HRs, and median follow-up must align. | KM tables, censoring tables, survival figures. |  |
| 6 | Safety count and rate checks | Safety denominators and exposure-adjusted rates are often inconsistent. | Safety population, exposure tables, AE summaries. |  |
| 7 | Cross-document numerical consistency | Abstract, text, tables, figures, supplements, CSR, and registry should align. | All manuscript sections and outputs. |  |
| 8 | Unit conversions and scale factors | Unit or scale errors can create clinically meaningful inaccuracies. | Units, footnotes, data dictionary, outputs. |  |

## Format and Precision QC

| # | Check | Why | Evidence | Checked |
|---:|---|---|---|---|
| 9 | Decimal-place consistency | Inconsistent precision distracts and can imply false accuracy. | Style guide, TLF shells, journal rules. |  |
| 10 | Scientific notation consistency | Scientific numbers should use one defined style across the document. | Style guide and examples in manuscript. |  |
| 11 | Leading and trailing zero rules | Values such as .25 or inconsistent trailing zeros should follow style rules. | Style guide and tables/figures. |  |
| 12 | P-value display | Avoid formats such as p = 0.000; use appropriate thresholds and precision. | Style guide, statistical convention, output p-values. |  |
| 13 | Confidence interval formatting | CI notation, separators, brackets, and decimal places should be consistent. | Style guide, endpoint TLFs. |  |
| 14 | Percent/rate/ratio display | Percent signs, rate units, ratio labels, and denominator footnotes should be clear. | TLF shells, manuscript tables, figure legends. |  |
| 15 | Missing-value symbols and footnotes | Missing symbols, N/A, NE, NR, and NA need consistent definitions. | TLF shell, abbreviations, footnotes. |  |
| 16 | Final rendered-output proofing | PDF/Word rendering can introduce line breaks, missing symbols, or table misalignment. | Final PDF/Word proof, tables, figures. |  |
