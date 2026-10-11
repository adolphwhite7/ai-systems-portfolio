# Engineering Evidence Index

Use this index to follow each capability from my role and delivery responsibilities to the architecture, examples, source, and tests available for review.

## Capability Map

| Capability and ownership | Direct public artifacts | Date and status | Independently inspectable evidence | Limits |
| --- | --- | --- | --- | --- |
| **Enterprise integration:** Capital One contact-center integration architect; Amazon Connect telephony integration lead working with cloud engineering and information security. | [Career account](https://mastermindgroupventures.com/founder.html); [integration case study](case-studies/enterprise-integration.md). | Capital One employment, October 1999–July 2020. Historical delivery account. | Published roles, scope, design choices, and reported outcomes. | Capital One employment, not an MGV client engagement. Six acquired HSBC sites are distinct from broader career site responsibilities. |
| **Application engineering:** Chief Architect of DNA Health Insights; architecture, delivery, implementation review, testing, and release ownership. | [Live product](https://www.dna-health-insights.com/); [engineering description](https://mastermindgroupventures.com/architecture.html#dna-engineering); [case study](case-studies/dna-health-insights.md). | Live public product and architecture descriptions checked October 11, 2026. | Public interface and published raw-file → findings → reading → saved-account-report flow. Some features require an account. | Raw DNA stays local under the described architecture; consented findings leave the device for report generation and storage. Educational use; family-business work sample, not an independent client endorsement. |
| **Governed AI engineering:** MGV founder and principal enterprise architect directing the internal Gateway's architecture, standards, and release decisions. | [September 14 guide](https://mastermindgroupventures.com/work/gateway/index.html); [architecture](https://mastermindgroupventures.com/architecture.html#gateway); [case study](case-studies/human-approved-ai-work.md). | Guide describes a September 8, 2026 local workflow and route-specific macOS qualification. Historical tests were inspected for the guide, not rerun. | Published control design and walkthrough linking an assignment, bounded change, Git revision, acceptance test, independent review, and one resume. | Internal macOS workflows; Linux and multi-tenant operation are not qualified. A customer environment requires separate integration and testing. |
| **Public Python example:** project owner of the Connected Report Demo. | [Source and CLI](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/report_builder.py); [tests](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/tests/test_report_builder.py); [synthetic input](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/examples/findings.json); [sample output](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/examples/connected-report.md). | Commit `126cc37b060118c4d40a9b2ac2f4c533958e73d8`; local checks run October 11, 2026 on Python 3.14.0. | Standard-library CLI, input validation, duplicate rejection, ordered selection, deterministic Markdown rendering, source-link formatting, and seven passing unit tests. | Synthetic data and placeholder references; no agent or model execution. Template grouping does not verify relationships or causation. |

## Run the Public Python Example

At the linked commit, from the demo repository:

```sh
python3 report_builder.py --input examples/findings.json --select F-101 F-102 F-103 --output connected-report.md
python3 -m unittest discover -s tests -v
cmp connected-report.md examples/connected-report.md
```

Local verification on October 11, 2026 produced the committed example exactly and passed all seven tests. Selecting the unknown ID `F-999` returned the expected error and exit code 2. This records behavior in one environment, not comprehensive compatibility or production performance.

## Reading the Public Sources

- **Career account:** My published account of roles, scope, and outcomes; supporting employer records remain private.
- **Product and Gateway descriptions:** Owner-published architecture and workflow accounts. Independent access to private implementations and runtime privacy verification is not provided here.
- **Demo source and tests:** Public implementation and reproducible checks at the linked commit. Results cover the deterministic synthetic example in the stated environment.

[Back to the portfolio](README.md)
