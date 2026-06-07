# Knowledge Source Strategy

## Core source

The primary knowledge source should be the companion checklist:

```text
checklists/Statistics_QC_Review_Checklists_Companion_v2_with_Oncology_Checklist.docx
```

## Machine-friendly versions

Also provide the checklists as Markdown and CSV:

```text
checklists/stats_qc_checklists.md
checklists/stats_qc_checklists.csv
checklists/numerical_and_format_qc.md
checklists/numerical_and_format_qc.csv
```

## Supporting external guidance

Add official guidance URLs from:

```text
guidance/guidance_urls.md
```

Use external guidance as reference, not as the source of truth for a specific study.

## Evidence hierarchy for the agent

1. Protocol, SAP, testing hierarchy, estimand section
2. Registry entry
3. TLFs, listings, ADaM/SDTM metadata, programming specs
4. CSR and manuscript
5. Internal style guide and TLF shells
6. External guidance sources

## Public repository caution

Do not store real study documents in this repo. Use synthetic test files only.
