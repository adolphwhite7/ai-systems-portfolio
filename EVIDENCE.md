# Engineering Evidence Index

Use this index to follow each capability from my role and delivery responsibilities to the architecture, examples, source, and tests available for review.

## Enterprise Integration

- **Role:** Capital One contact-center integration architect and Amazon Connect telephony integration lead, working with cloud engineering and information security.
- **Evidence:** [Career account](https://mastermindgroupventures.com/founder.html) and [integration case study](case-studies/enterprise-integration.md).
- **Review focus:** Integration across six acquired HSBC sites; network address translation and firewall simplification from roughly 4,000 rules to 30; cloud storage-policy access controls and PCI collaboration.
- **Status:** Historical delivery during Capital One employment, October 1999–July 2020. The six acquired sites are distinct from broader career site responsibilities.

## DNA Health Insights

- **Ownership:** Chief Architect; architecture, delivery, implementation review, testing, and release decisions.
- **Evidence:** [Live product](https://www.dna-health-insights.com/), [engineering description](https://mastermindgroupventures.com/architecture.html#dna-engineering), and [case study](case-studies/dna-health-insights.md).
- **Review focus:** Browser-local raw-file processing, consented findings used for report generation, and account-scoped saved findings and reports.
- **Status:** Live public product and architecture descriptions checked October 11, 2026. Educational application created for a family member's business; some features require an account.

## Governed AI Gateway

- **Ownership:** MGV founder and principal enterprise architect directing the internal Gateway prototype's architecture, standards, and release decisions.
- **Evidence:** [September 14 guide](https://mastermindgroupventures.com/work/gateway/index.html), [architecture](https://mastermindgroupventures.com/architecture.html#gateway), and [case study](case-studies/human-approved-ai-work.md).
- **Review focus:** LangGraph transitions, bounded changes, Git revision identity, acceptance testing, independent review of the resulting revision, and one resume without replay.
- **Status:** Guide describes a September 8, 2026 local workflow and route-specific macOS qualification. Historical tests were inspected for the guide, not rerun. Linux and multi-tenant operation remain unqualified; a customer environment requires separate integration and testing.

## Runnable Python Example

- **Ownership:** Project owner of the public Connected Report Demo.
- **Inspect:** [Source and CLI](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/report_builder.py), [tests](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/tests/test_report_builder.py), [synthetic input](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/examples/findings.json), and [sample output](https://github.com/adolphwhite7/connected-report-demo/blob/126cc37b060118c4d40a9b2ac2f4c533958e73d8/examples/connected-report.md).
- **Review focus:** Standard-library CLI, input validation, duplicate rejection, ordered selection, deterministic Markdown rendering, source-link formatting, and seven unit tests.
- **Status:** Commit `126cc37b060118c4d40a9b2ac2f4c533958e73d8`; local checks run October 11, 2026 on Python 3.14.0. Synthetic data and placeholder references; no agent or model execution. Template grouping does not verify relationships or causation.

From the demo repository at the linked commit:

```sh
python3 report_builder.py --input examples/findings.json --select F-101 F-102 F-103 --output connected-report.md
python3 -m unittest discover -s tests -v
cmp connected-report.md examples/connected-report.md
```

Local verification on October 11, 2026 produced the committed example exactly and passed all seven tests. Selecting the unknown ID `F-999` returned the expected error and exit code 2. These checks record behavior in the stated environment.

## Evidence Legend

Career and internal-system histories are first-person accounts. Public product and architecture pages describe the systems; private employer records, product source, and Gateway receipts are not published here. The Python source and tests are directly inspectable and reproducible.

[Back to the portfolio](README.md)
