# Governance and Limitations

## What the agent can do

- Assist with numerical QC between manuscript text/tables/figures and TLFs.
- Flag statistical interpretation risks.
- Identify formatting and precision inconsistencies.
- Produce structured findings for human review.
- Summarize high-risk issues in a review memo.

## What the agent cannot do by itself

- Provide final statistical sign-off.
- Replace programming QC or independent analysis replication.
- Confirm prespecification without access to dated protocol/SAP/registry evidence.
- Verify hidden calculations if source denominators or outputs are missing.
- Certify regulatory readiness.

## Required human oversight

High or Critical findings should be reviewed by the responsible statistician or programming lead.

## Version control

Track versions for:

- Companion checklist
- Agent instructions
- Style guide
- Guidance URLs
- Synthetic validation data
- Output schema

## Change log recommendation

Use GitHub Releases or `CHANGELOG.md` entries for each update:

- Added/removed checklist items
- Changed output schema
- Updated external guidance links
- Added validation examples
- Fixed known false positives or false negatives
