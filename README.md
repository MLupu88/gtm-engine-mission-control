<div align="center">

# GTM Action Web

### **The account-level decision layer between website activity and GTM action**

**Know which accounts are moving—and whether marketing or sales should act next.**

</div>

<p align="center">
  <img src="./assets/gtm-action-web.gif" alt="Animated GTM Action Web journey from paid and organic website activity through identity resolution, account understanding, ICP evaluation, a human-approved marketing or sales decision, and result capture" width="100%">
</p>

GTM Action Web takes behavioral signals from paid and organic website traffic, keeps the campaign, source and content context attached, and resolves the company or person behind the activity when the evidence supports it. It then combines that behavior with activity from other people at the same organization, CRM context and research to build one current account picture.

That account—not an isolated click or lead—is evaluated against a versioned ICP and current intent evidence. GTM Action Web recommends the next appropriate move for marketing or sales, a person decides whether it should happen, and the result becomes part of the account history.

**It is not scoring one visit and calling it buying intent. It is turning multiple pieces of evidence into an explainable account-level decision.**

<div align="center">

*Working internal product designed and built by [Mihail Lupu](https://github.com/MLupu88). Public portfolio presentation using synthetic data and sanitized visuals.*

</div>

---

## The missing layer between traffic and action

Website analytics could show that traffic increased. Campaign platforms could show which message or asset earned a click. De-anonymization could sometimes identify a visitor or company. HubSpot could show what sales already knew. Yet the operator still had to assemble those fragments manually before answering the question that mattered:

> **What is actually happening at this account, and what should we do about it now?**

GTM Action Web grew around that gap. It connects campaign and content context to identifiable behavior, groups supported activity around the canonical account, evaluates the resulting account against the appropriate ICP and turns that assessment into work. Strong fit and meaningful intent may call for sales review, an owner alert or prepared outreach. Earlier or incomplete evidence may call for marketing nurture, research, retargeting or simply watching the account. No action is also a legitimate decision.

It is not a CRM replacement, a lead-scoring dashboard or an AI layer performing confidence over messy data. **The account is the center of the model—not the event, the lead or the vendor that produced it.**

---

## One account, even when the evidence arrives in pieces

A campaign touch, a return visit, an identified person, a company property and an open opportunity may all describe the same commercial story. They are not automatically the same kind of truth.

<p align="center">
  <img src="./assets/account-story.gif" alt="An animated account story in which campaign activity, website behavior, identity and CRM context accumulate around one canonical account" width="100%">
</p>

GTM Action Web keeps the source and timestamp of each observation, resolves identity explicitly and reconciles comparable facts before they become the current account picture. New evidence can strengthen the story, expose a conflict or leave an important question unanswered. Missing context is allowed to remain missing.

That is the structural difference. The product does not simply collect signals. It gives them somewhere durable to accumulate and rules for becoming operationally useful.

---

## From movement to action

The operator does not begin with ingestion health or a wall of metrics. The Daily Brief begins with movement: which canonical accounts changed, what caused the change and which ones now need a decision.

<p align="center">
  <img src="./assets/operator-journey.svg" alt="A four-scene operator journey from Daily Brief to account understanding, human decision and confirmed result" width="100%">
</p>

Opening an account reveals the commercial story behind the movement: current company and CRM truth, verified people across the organization, recent activity, campaign and content context, ICP assessment, missing evidence and the provenance behind each claim. The official evaluation uses the relevant published ICP version; another profile can be tested as a preview without quietly replacing production truth.

The queues follow the job in front of the person—**decide, prepare, research or watch**—rather than asking them to translate another abstract score into work.

---

## The system recommends. The operator decides.

<p align="center">
  <img src="./assets/decision-surface.svg" alt="A synthetic account decision surface with current account state, an explainable recommendation, missing context and explicit human decision controls" width="100%">
</p>

Recommendations are versioned projections over current account truth, production ICP evaluation, verified people and unresolved review items. They show the proposed posture, supporting reasons, blockers, confidence and the next safe step.

The operator accepts, modifies or rejects that recommendation and records why. The response remains tied to the exact recommendation version it answered, so changed evidence cannot quietly inherit an old approval.

An accepted next move can prepare a grounded outreach draft or call brief. Preparation, approval, execution handoff and provider-confirmed execution remain separate states. If a real recipient cannot be verified, GTM Action Web does not invent one. Research, watch and no action are valid decisions too.

---

## Campaign tracking and GA4 answer different questions

GA4 is the source of truth for aggregate website traffic: reach, sessions, users and engagement across anonymous and known visitors. It cannot, by itself, create One Account Truth.

Campaign and UTM context therefore travel separately with identifiable behavioral evidence when that evidence can be defensibly associated with a lead, person or canonical account.

<p align="center">
  <img src="./assets/campaign-account-outcome.svg" alt="A synthetic view of GA4 aggregate traffic alongside campaign-linked account evidence and a GTM Action Web decision" width="100%">
</p>

The product direction is to carry a campaign beyond top-of-funnel reporting: **which known leads and accounts arrived, which assets they engaged with, how interest accumulated across the organization, which ICP they fit, what GTM Action Web recommended, what a person chose and which outcomes were later confirmed**.

This is not an attempt to force anonymous GA4 sessions into named accounts or claim universal multi-touch attribution. Aggregate performance and account-bound evidence stay distinct until identity and provenance can support the connection.

---

## The GTM stack keeps its job. The account gains a memory.

GTM Action Web is connected to operational systems, but it does not flatten them into a row of interchangeable “integrations.” Each one contributes a specific kind of context or receives a specific kind of approved output.

<p align="center">
  <img src="./assets/gtm-stack.svg" alt="Recognizable GTM systems including HubSpot, RB2B, Google Analytics, n8n and LinkedIn Ads arranged around one canonical account" width="100%">
</p>

HubSpot remains the CRM. Google Analytics remains the aggregate traffic authority. RB2B contributes identifiable activity. Client Radar contributes research evidence. n8n orchestrates ingestion and refresh. **LinkedIn Ads belongs on the acquisition side of this story:** its campaign and UTM context can travel with identifiable activity, but this README does not claim a direct LinkedIn Ads API integration.

<details>
<summary><strong>Current integration roles</strong></summary>

| System | Current role in GTM Action Web |
| --- | --- |
| **HubSpot** | Read-only company and contact identity, firmographics, CRM state, ownership, opportunities and selected acquisition context. |
| **RB2B + n8n** | Identifiable website activity, person/company resolution and production ingestion orchestration. |
| **Client Radar** | On-demand company research with persisted requests, returned evidence and completed-result inspection. |
| **Google Analytics 4** | Aggregate website and campaign traffic, intentionally separate from named-account activity. |
| **LinkedIn Ads** | Campaign/source context carried through captured UTM or campaign evidence; direct Ads API connectivity is not claimed. |
| **Tavily** | Restricted ingestion of the company’s own public material for reviewed product knowledge. |
| **DeepSeek** | Bounded Account Brain and selected-period interpretation over controlled evidence. |
| **Clawd** | Separate consumer of immutable, explicitly approved execution handoffs. |

</details>

The operational repository still contains an older Sheets-sourced outbound-reporting path and manual Dripify-era export logic. Those are legacy surfaces, not the current GTM Action Web product thesis, so they are not presented as core integrations. Provider neutrality also does not mean pretending every planned provider is already connected: Dealfront, Cognism, PostHog and Salesforge are not presented here as current capabilities.

---

## AI makes the history readable. It does not decide the truth.

GTM Action Web currently gives AI two jobs where language is genuinely useful.

The **Account Brain** compresses a complicated account history into a readable explanation of why the account matters now. The **Period Brief** summarizes what changed across the selected reporting window. Both work over evidence the system already has and point the operator back toward that evidence.

<p align="center">
  <img src="./assets/ai-role.svg" alt="GTM Action Web AI turning controlled account evidence into an Account Brain explanation and a reporting-period brief while deterministic systems retain authority" width="100%">
</p>

The model does not resolve identity, promote observations into canonical truth, perform the official ICP evaluation, choose recommendation policy or authorize execution. In practical terms: **AI reduces the reading burden; it does not acquire decision rights.**

---

## The loop does not end at outreach

Decisions, actions and outcomes become part of the account’s operating history rather than disappearing into another tool after the click.

<p align="center">
  <img src="./assets/reporting-outputs.svg" alt="A synthetic campaign report with account decisions and outcomes plus PDF and operational CSV outputs" width="100%">
</p>

The current Reports surface keeps **GA4 aggregate traffic** and **canonical identified-touch history** visibly separate. It also retains a demoted legacy outbound-reporting packet with PDF and CSV exports. That older packet keeps its source and limitations; it is not silently promoted into canonical account truth.

The product direction is to generate leadership and operational reporting from the same canonical campaign → lead → account → decision → outcome history used by GTM Action Web. The useful point is not the file format. **Reporting should become an output of operating the system instead of a second account story rebuilt for the meeting.**

---

## Under the product surface

The implementation is a TypeScript monorepo with a React/Vite operator workspace, an Express API, PostgreSQL with Drizzle, explicit contracts and pure packages for identity, observations, reconciliation and evaluation.

<p align="center">
  <img src="./assets/truth-lifecycle.svg" alt="The evidence lifecycle from provider observation through identity, canonical truth, assessment, recommendation, human decision and confirmed result" width="100%">
</p>

The important technical decisions are the boundaries, not the framework names:

- provider-specific payloads stop at adapters;
- identity resolution and idempotency are deterministic;
- production evaluations retain the evidence snapshot and evaluator version they used;
- recommendations have a named policy version and a stable fingerprint;
- operator responses and execution handoffs are append-only;
- database constraints protect important lifecycle and immutability rules beneath the UI;
- browser, ingestion and execution-consumer routes have separate authorization boundaries.

Observation is not truth. Assessment is not recommendation. Recommendation is not authorization. Handoff is not a confirmed result. The product remains useful because those distinctions survive the full workflow.

---

## A working product with a clear frontier

GTM Action Web is already a working internal product, not a static concept prototype. The account model, evidence lifecycle, ICP evaluation, deterministic recommendations, operator decisions, grounded preparation, explicit handoffs, GA4 reporting and canonical touch history form the current operating spine.

<p align="center">
  <img src="./assets/product-frontier.svg" alt="The operating GTM Action Web product spine, the campaign and feedback loop being deepened, and the capabilities deliberately not claimed" width="100%">
</p>

The active frontier is continuity: following defensible campaign context into a known lead and account, then carrying the human decision through approved execution to a confirmed outcome. That is where the product becomes more than a better prioritization surface—it becomes a learning GTM operating loop.

---

## Why this is in my portfolio

<table>
<tr>
<td width="150" valign="top">
  <img src="https://github.com/MLupu88.png?size=240" alt="Mihail Lupu" width="126">
</td>
<td valign="top">

### Mihail Lupu

I work in product marketing and have spent more than a decade around automation, conversational AI and generative AI. I also teach design thinking for GenAI at the Bucharest University of Economic Studies.

I built GTM Action Web because I wanted to get past the easy version of the GTM story. “Connect the data, score the account, let AI recommend an action” sounds convincing until identity is uncertain, sources disagree, a recipient cannot be verified or nobody can prove what happened after the handoff.

This project let me own that problem from product thesis and information architecture through evidence modeling, workflow design, integrations, implementation and positioning. That is the part I value: getting close enough to the machinery that product judgment stops being abstract and the story becomes harder to fake.

[GitHub profile](https://github.com/MLupu88)

</td>
</tr>
</table>

### Related work

- **ChannelOS** — an AI-native operating system for a partner organization, built around relationship memory, attribution, targets and leadership reporting.
- **[AI Agent Sudo](https://github.com/MLupu88/ai-agent-sudo)** — a provider-neutral authorization layer that returns `allow`, `deny` or `require_approval` before an agent executes a tool.
- **[VoiceWire](https://github.com/MLupu88/voicewire)** — a local diagnostic engine combining packet/media evidence with agent traces to explain voice-AI latency and failure boundaries.

---

<p align="center">
  <strong>Built to understand the system well enough to tell its story properly.</strong>
</p>

<sub>This repository is a sanitized portfolio case study, not the operational source distribution or official company documentation. Visuals use synthetic companies, people, campaign names, activity and metrics. Product and company marks belong to their respective owners.</sub>
