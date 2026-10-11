# Engineering Evidence Index

This index separates my ownership and published accounts from artifacts a technical reviewer can inspect or run. Public descriptions of private systems establish what is claimed; they do not provide independent access to those implementations.

## Capability Map

| Capability and ownership | Direct public artifacts | Date and status | Independently inspectable evidence | Limits |
| --- | --- | --- | --- | --- |
| **Enterprise integration:** Capital One contact-center integration architect; Amazon Connect telephony integration lead working with cloud engineering and information security. | [Career account](https://mastermindgroupventures.com/founder.html); [integration case study](case-studies/enterprise-integration.md). | Capital One employment, October 1999–July 2020. Historical delivery account. | Published roles, scope, design choices, and reported outcomes. Employer implementation records are not included. | Owner-reported experience, not an independent audit or MGV client engagement. Six acquired HSBC sites are distinct from broader career site responsibilities. |
| **Application engineering:** Chief Architect of DNA Health Insights; architecture, delivery, implementation review, testing, and release ownership. | [Live product](https://www.dna-health-insights.com/); [engineering description](https://mastermindgroupventures.com/architecture.html#dna-engineering); [case study](case-studies/dna-health-insights.md). | Live public product and architecture descriptions checked October 11, 2026. | Public interface and published raw-file → findings → reading → saved-account-report flow. Some features require an account. | Product source and runtime privacy controls are not independently verified here. Raw DNA stays local under the described architecture; consented findings leave the device for report generation and storage. Educational use; family-business work sample, not an independent client endorsement. |
| **Governed AI engineering:** MGV founder and principal enterprise architect directing the internal Gateway's architecture, standards, and release decisions. | [September 14 guide](https://mastermindgroupventures.com/work/gateway/index.html); [architecture](https://mastermindgroupventures.com/architecture.html#gateway); [case study](case-studies/human-approved-ai-work.md). | Guide describes a September 8, 2026 local workflow and route-specific macOS qualification. Historical tests were inspected for the guide, not rerun. | Published control design and walkthrough linking an assignment, bounded change, Git revision, acceptance test, independent review, and one resume. | Owner-published account; private source and terminal receipts are not exposed. No independent current runtime check, customer deployment, certification, performance measure, Linux qualification, or multi-tenant qualification is established. |
| **Python implementation:** author of the public Connected Report Demo. | [Source and CLI](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/report_builder.py); [tests](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/tests/test_report_builder.py); [synthetic input](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/examples/findings.json); [sample output](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/examples/connected-report.md). | Commit `126cc37b060118c4d40a9b2ac2f4c533958e73d8`; local checks run October 11, 2026 on Python 3.14.0. | Standard-library CLI, input validation, duplicate rejection, ordered selection, deterministic Markdown rendering, source-link formatting, and seven passing unit tests. | Synthetic operations data and placeholder references. No agent execution, model/API calls, application data store, deployment, or causal inference is demonstrated. |

## Run the Public Python Example

At the linked commit, from the demo repository:

```sh
python3 report_builder.py --input examples/findings.json --select F-101 F-102 F-103 --output connected-report.md
python3 -m unittest discover -s tests -v
cmp connected-report.md examples/connected-report.md
```

Local verification on October 11, 2026 produced the committed example exactly and passed all seven tests. Selecting the unknown ID `F-999` returned the expected error and exit code 2. This records behavior in one environment, not comprehensive compatibility or production performance.

The demo groups shared themes with fixed text templates. Its sample narrative refers to a shared operating issue and an unfixed cause, although grouping by theme does not establish those causal relationships. Treat that wording as a limitation of the sample, not evidence of causal analysis. A separate demo change would be needed to correct it.

## Reading the Public Sources

- **Career account:** I report the work, role, and outcomes. Public GitHub does not disclose private employer material or establish current certification status.
- **Product and Gateway descriptions:** MGV publishes the architecture and lifecycle boundaries. A public narrative or screenshot is not an independent implementation audit.
- **Demo source and tests:** Reviewers can inspect the implementation and reproduce the listed checks. These checks support only the small deterministic example.

[Back to the portfolio](README.md)
