# Keeping AI Work Within Human-Approved Boundaries

**Role:** Founder & Principal Enterprise Architect, Mastermind Group Ventures<br>
**Artifact:** MGV's internal governed AI Dispatch Gateway<br>
**Status:** Internal Gateway prototype with demonstrated local workflows; qualification is specific to the route and environment<br>
**Public guide:** [The Gateway, September 14, 2026](https://mastermindgroupventures.com/work/gateway/index.html)

The visual below is a generalized reference architecture. The linked guide supplies the implementation detail and qualification boundaries for the internal system.

<img src="../assets/human-approved-ai-work.png" alt="Reference architecture for governed AI dispatch and controlled recovery" width="920">

## The Need

Teams can use different AI models and tools for different kinds of work, but the models do not have identical capabilities, access, or reliability. Important decisions still need a clear owner, and failed or incomplete work needs to remain visible instead of being silently promoted.

## What I Designed

I set the architecture, standards, and release decisions for a system that assigns bounded engineering work to agents. The [public engineering description](https://mastermindgroupventures.com/architecture.html#gateway) and illustrated guide describe five responsibilities:

1. A person approves the objective, scope, access, and intended effect.
2. An orchestrator checks context and selects a qualified route for the assignment.
3. The Gateway applies the route's access and change limits while the agent does the work.
4. Output, tests, changes, and Git revision identity support review and evidence acceptance.
5. Recovery uses the recorded state; a person retains authority over advancement and release.

The design keeps consequential choices human-owned while still allowing teams to use specialized AI tools where they add value.

## Implementation Boundaries

| Responsibility | Mechanism described in the public guide |
| --- | --- |
| Workflow state | LangGraph owns supported transitions; the Gateway invokes the agent and records execution. |
| Agent permissions | Read-only review and bounded code changes use separate routes. Coding permissions differ by qualified agent and interface. |
| Code identity | Git identifies the starting and resulting versions so review and acceptance refer to the actual change. |
| Local commit authority | The qualified Codex adapter may create at most one specifically authorized local commit. That authority does not include publishing or deployment. |
| Review records | Recorded advisory routes preserve output and a terminal record. Explicit Open Review is a separate admitted option without that durable record. |
| Recovery | Preserve useful output, check whether a change already occurred, and recover the missing step within its authority. |

Push, pull-request creation, merge, deployment, and release are separately authorized actions.

## The Documented Local Workflow

The guide describes a September 8, 2026 test in a disposable repository:

1. The assignment named `order_summary.py`, a starting revision, and permission for one local commit.
2. Codex changed the permitted file, and the adapter created the authorized commit.
3. Acceptance testing ran against the resulting version.
4. Cline performed independent read-only review, and Dispatch Lead acceptance was bound to that same result.
5. One resume completed the local patch without replaying the agent's work.

The guide identifies the A40-R1 terminal receipt as the evidence for this journey. It documents a bounded local change, test, and review, not a customer production release.

## What the Visual Shows

The reference architecture follows a work request from approval through routing, model execution, evidence review, and the final human decision. A separate recovery path makes failure visible, preserves useful output, and returns authorized work to the same controlled entry point.

## Evidence and Qualification

The [September 14 guide](https://mastermindgroupventures.com/work/gateway/index.html) documents workflows tested in MGV’s macOS environment. Qualification is specific to the route, model, interface, and environment. Linux and multi-tenant operation remain unqualified; another organization requires separate integration and testing.

The guide inspected historical test records rather than rerunning them. This example establishes a bounded local workflow, with customer deployment and production release outside its scope.

[Learn about Mastermind Group Ventures](https://mastermindgroupventures.com/)  
[Evidence index](../EVIDENCE.md) · [Back to the portfolio](../README.md)
