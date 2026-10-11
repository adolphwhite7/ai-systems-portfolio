# DNA Health Insights

**Role:** Chief Architect  
**Product:** [DNA Health Insights](https://www.dna-health-insights.com/)  
**Status:** Live consumer genomics education platform

## The Need

Consumer DNA files contain a large amount of information, but the raw data is difficult for most people to interpret. The product needed to turn that information into clear educational reports, show where the information came from, and help customers move from individual findings to a more connected understanding.

## What I Led

I have directed the product and technical work across the customer journey, including:

- individual, source-linked reports written in plain language;
- a workspace that combines selected findings into one connected write-up;
- saved reports, customer dashboards, payments, and account workflows;
- guided support and chat experiences informed by curated product and legal guidance; and
- automated testing, live browser checks, production diagnosis, and follow-through on fixes.

The work requires more than generating text. Report content, source handling, customer flow, legal boundaries, support behavior, and system reliability all have to work together as one product.

## Architecture and Data Boundaries

The [live product](https://www.dna-health-insights.com/) and [public engineering description](https://mastermindgroupventures.com/architecture.html#dna-engineering) describe this flow:

1. The person creates or signs into an account before selecting a DNA file.
2. The raw DNA file is processed locally in the browser, rather than uploaded to the application's servers.
3. With consent, report findings are used to generate a plain-language educational reading.
4. Report findings and the reading are saved with the report in the signed-in account.

The distinction is between the raw file and the findings used for reports. Browser-local raw-file processing does not mean that all health-related information stays on the device.

The [MGV work description](https://mastermindgroupventures.com/capabilities.html#dna) also describes account-scoped access to saved findings and reports.

## Engineering Ownership

I direct architecture and product delivery, including implementation review, testing, and follow-through on production issues. I use AI-assisted development to extend delivery capacity while owning architecture, acceptance, and release decisions.

## Why This Work Matters

DNA Health Insights makes complex information easier to explore without hiding the supporting sources. It also gives customers a way to connect findings across separate reports instead of leaving them with a collection of isolated facts.

[Explore DNA Health Insights](https://www.dna-health-insights.com/)

## About This Public Case Study

DNA Health Insights provides educational information; it does not diagnose conditions or prescribe treatment.

The application was created for a family member's business and is presented as an MGV work sample, not an independent client endorsement. Public product features may require account access.

[Evidence index](../EVIDENCE.md) · [Back to the portfolio](../README.md)
