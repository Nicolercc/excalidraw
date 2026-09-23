# Excalidraw First-Run Activation — Source of Truth

**Team:** AI Affair **Date:** September 13, 2026 **Status:** Post-discovery — v3.1 **Scope:** The first-run activation brief. Discovery held September 16, 2026 — scope confirmed as the free tier **Purpose:** Single reference for the project. Consolidates stakeholder direction, the brief, KPI analysis, verified product and market state, user evidence, and the analysis that follows from them.

### Team — AI Affair

| Name | Role |
| :---- | :---- |
| Natalie Walker | Product Manager — owner of this document |
| Nicole Rodríguez | Front End Developer |
| Sean Pisano | Back End Developer |
| Erasmo Concepcion | Security / debugging |

**Exercise notice:** This is a simulated product engagement. Discovery was held on September 16, 2026; stakeholder direction is recorded in §1. Excalidraw is a real product and all external research in this document is drawn from genuine public sources, cited in Appendix A. The stakeholder brief in §3 and the roles above are part of the exercise. Nothing here represents Excalidraw's internal data, roadmap decisions, or personnel, and it should not be circulated as though it does.

### Version history

| Version | Date | What changed |
| :---- | :---- | :---- |
| 1.0 | September 13, 2026 | **Document created.** Product brief, KPI analysis, first-run map, drop-off hypotheses, community research, and verified product state from the Excalidraw+ changelog and roadmap |
| 1.1 | September 13, 2026 | Table of contents added. Reddit source pass restored as its own attributed section (now §7.2) |
| 1.2 | September 13, 2026 | X/Twitter section added (now §7.4). Free-tier-to-paid data-loss finding added to what is now §7.3 |
| 1.3 | September 13, 2026 | AI Affair team roster and exercise notice added |
| 1.4 | September 15, 2026 | Competitive landscape added (now §6.1–5.6) |
| 1.5 | September 15, 2026 | Competitor business models and user-retention drivers added (now §6.7–5.8) |
| 1.6 | September 15, 2026 | Market position ranking, licensing analysis, and positioning map added (now §6.9–5.11) |
| 1.7 | September 15, 2026 | Charts added: KPI blind-spot diagram (§2), first-run funnel (now §9), positioning map (now §6.11) |
| 1.8 | September 15, 2026 | Summary-at-a-glance chart added to the front of the document |
| 2.0 | September 15, 2026 | **Restructured into five parts** — facts, then evidence, then analysis, then action. Sections reordered and renumbered; no content removed. Framing of stakeholder status neutralised |
| 3.0 | September 16, 2026 | **Discovery held.** Stakeholder direction added as §1 and now governs where it conflicts with research. Free tier confirmed. Templates made top priority; §6.4 rewritten to support them. Instrumentation scoped out by client. tldraw and draw.io ownership facts corrected |
| 3.1 | September 16, 2026 | Team names corrected. Summary chart rebuilt around the post-discovery priority. **Time-not-price section added (§6.9, credit Erasmo Concepcion)** and made the document's headline. Open questions rewritten to show what discovery answered. Duplicate version history in Appendix C removed |

**Current version: 3.1 — September 16, 2026**

**How to read this document:** Everything below is marked as one of three things — **Confirmed** (verified against a primary source, linked in Appendix A), **Hypothesis** (research-derived, not yet validated against product data), or **Open question** (requires an answer from Jacqueline or the data team before roadmap commitment). Do not treat hypotheses as findings in the kickoff.

---

## Summary at a glance

Summary of findings

THE HEADLINE People do not choose Excalidraw because it is free. They choose it because it costs no time. THREE FINDINGS Time, not price Miro and FigJam are free too. They cost 90 seconds and an account. That is the difference. The KPI misreads success No account needed, and it autosaves. Satisfied users score as churn. AI picks the wrong type Asked for a flowchart, returned a class diagram. draw.io already shipped the fix. WHAT WE BUILD — PRIORITY SET BY THE CLIENT 1 · Templates \+ diagram-type routing Client priority · prototype for next session 2 · Persistence legibility \+ export Acknowledged · secondary 3 · AI prompt history Acknowledged · secondary — · Activation instrumentation Parked by client direction SCOPE CONFIRMED: the free tier at excalidraw.com. Open: where the current activation metrics come from. The stakeholder could not identify the source.

---

## Contents

**Part I — What we found**

1. [Stakeholder direction — discovery session, September 16, 2026](#1-stakeholder-direction-discovery-session-september-16-2026)  
   - 1.1 [Questions answered](#11-questions-answered)  
   - 1.2 [Decisions taken](#12-decisions-taken)  
   - 1.3 [Where the stakeholder and the research differ](#13-where-the-stakeholder-and-the-research-differ)  
   - 1.4 [Committed next steps](#14-committed-next-steps)  
2. [Headline finding](#2-headline-finding)  
3. [The brief as submitted](#3-the-brief-as-submitted)

**Part II — The product and market, verified**

4. [Verified product model](#4-verified-product-model)  
   - 4.1 [There are two products, and the brief does not say which one it means](#41-there-are-two-products-and-the-brief-does-not-say-which-one-it-means)  
   - 4.2 [Persistence model](#42-persistence-model)  
   - 4.3 [First-run surface (free hosted app)](#43-first-run-surface-free-hosted-app)  
5. [What has already shipped — scope constraint for the kickoff](#5-what-has-already-shipped-scope-constraint-for-the-kickoff)  
   - 5.1 [Recent releases relevant to this project](#51-recent-releases-relevant-to-this-project)  
   - 5.2 [On the public roadmap](#52-on-the-public-roadmap)  
   - 5.3 [Why this matters for the kickoff](#53-why-this-matters-for-the-kickoff)  
6. [Competitive landscape](#6-competitive-landscape)  
   - 6.1 [The field](#61-the-field)  
   - 6.2 [The account-free position is the moat — and the KPI penalizes it](#62-the-account-free-position-is-the-moat-and-the-kpi-penalizes-it)  
   - 6.3 [draw.io has already shipped Candidate 2's fix](#63-drawio-has-already-shipped-candidate-2s-fix)  
   - 6.4 [Templates — the gap Excalidraw is losing on](#64-templates-the-gap-excalidraw-is-losing-on)  
   - 6.5 [What the competitive read changes](#65-what-the-competitive-read-changes)  
   - 6.6 [Limitations](#66-limitations)  
   - 6.7 [Business models — and why they matter here](#67-business-models-and-why-they-matter-here)  
   - 6.8 [Why users keep choosing it](#68-why-users-keep-choosing-it)  
   - 6.9 [Time, not price — the argument that carries the rest](#69-time-not-price--the-argument-that-carries-the-rest)  
   - 6.10 [Market position — who is actually most desired](#69-market-position-who-is-actually-most-desired)  
   - 6.11 [Licensing — and why it is a distribution channel](#610-licensing-and-why-it-is-a-distribution-channel)  
   - 6.12 [Positioning map](#611-positioning-map)

**Part III — What users say**

7. [Voice of user](#7-voice-of-user)  
   - 7.1 [What users like](#71-what-users-like)  
   - 7.2 [Reddit research](#72-reddit-research)  
   - 7.3 [GitHub, issue-tracker and review-site evidence](#73-github-issue-tracker-and-review-site-evidence)  
   - 7.4 [X / Twitter](#74-x-twitter)  
   - 7.5 [Where concerns are voiced](#75-where-concerns-are-voiced)  
   - 7.6 [The one-sentence synthesis](#76-the-one-sentence-synthesis)

**Part IV — What it means**

8. [KPI assessment](#8-kpi-assessment)  
   - 8.1 [Unresolved measurement decisions](#81-unresolved-measurement-decisions)  
   - 8.2 [Recommended metric architecture](#82-recommended-metric-architecture)  
9. [First-run map and event taxonomy](#9-first-run-map-and-event-taxonomy)  
10. [Drop-off hypotheses](#10-drop-off-hypotheses)  
11. [Brief assumptions vs. research](#11-brief-assumptions-vs-research)

**Part V — What we do next**

12. [Product constraints to carry into discovery](#12-product-constraints-to-carry-into-discovery)  
13. [Open questions — status after discovery](#13-open-questions--status-after-discovery)  
14. [Recommended next steps](#14-recommended-next-steps)  
- [Appendix A — Sources](#appendix-a--sources)  
- [Appendix B — Research limitations](#appendix-b--research-limitations)  
- [Appendix C — Document control](#appendix-c--document-control)

---

# Part I — What we found

## 1\. Stakeholder direction — discovery session, September 16, 2026

**This section supersedes earlier analysis where they conflict. The client owns the roadmap; where her direction differs from our research position, her direction governs and the change is noted.**

Thirty-minute discovery session. Attending: Jacqueline Reverand (Head of Product), Natalie Walker, Nicole Rodríguez, Erasmo Concepcion.

### 1.1 Questions answered

| Question | Answer | Effect |
| :---- | :---- | :---- |
| **Free app or Excalidraw+?** | **Free tier.** Focus on free-tier onboarding through to first saved drawing | Assumption A1 resolved. Every criterion previously marked \[BLOCKED: Q2\] now takes its free-app form |
| **Where do the activation metrics come from?** | **Not established.** The stakeholder had not studied the underlying data and was not able to identify the source. She asked the team to assume instrumentation exists or will be provided | Our concern was correct, but instrumentation is now out of scope by client direction |
| **Should signup come earlier in the flow?** | **No.** Users should experience product value before being asked to register | Directly endorses the position in §8 and §6.2 |

### 1.2 Decisions taken

**Templates are the top priority.** The stakeholder named templates the strongest and most immediately impactful feature, and asked for a prototype of a template-driven text-to-diagram flow for the next session.

**Templates and diagram-type routing merge into one feature.** Selecting a template biases the AI output toward that diagram type. This is the same fix our Candidate 2 proposed, arriving through the client's own priority rather than ours.

**Instrumentation is out of scope for this exercise.** The team was asked to assume analytics exist and to concentrate on user-facing work. This removes Candidate 3 from the build, not from the record — the underlying gap is unresolved and is logged in §13.

**AI prompt history and persistence/export were acknowledged as valuable but secondary.**

**A new idea was raised:** voice-to-text input for AI prompts, to reduce friction for mobile users. Unscoped.

### 1.3 Where the stakeholder and the research differ

**On the shopping-cart analogy.** The stakeholder compared first-run to an abandoned shopping cart. The team pushed back: a shopper intends to complete a purchase, so abandonment is always failure. A person sketching may be finished the moment the sketch exists. That difference is precisely why the brief's KPI misclassifies successful users — the funnel shape is similar, the intent is not.

**On templates.** Our §6.4 originally argued against expanding templates. The stakeholder disagreed. On review her position is better supported than ours was, and §6.4 has been rewritten. The original reasoning is preserved there so the change is traceable.

### 1.4 Committed next steps

- Send the source-of-truth document and PRD to the stakeholder via Slack for review  
- Prepare a prototype or design proposal for the template-driven text-to-diagram flow, 3–5 templates, for the next session  
- Confirm availability for a follow-up session including Sean Pisano, technical lead; proposed 18:30 on an upcoming weekday  
- Coordinate through Slack — confirmed as the reliable channel with this stakeholder

---

## 2\. Headline finding

Jacqueline's brief identifies a real, high-leverage problem. The first-run experience is the right place to look.

But the KPI as written does not match the product it is measuring. Two issues, in order of severity:

1. **The brief measures "new signups," but the product most first-time users touch does not require a signup.** The free hosted app at excalidraw.com drops a visitor straight onto a live canvas. Restricting the denominator to registered users excludes the majority of first-run traffic — including the link-shared and embedded traffic the brief itself names as the main discovery channel.  
     
2. **The brief treats "save" as one behavior, but the product has several distinct persistence paths** — automatic browser-storage persistence, explicit `.excalidraw` file download, image export, share-link creation, and (on Plus) cloud workspace persistence. These are not interchangeable, and a user who leaves satisfied with a locally persisted drawing would currently be scored as a failed activation.

Populations the brief's KPI cannot see

Everyone who reaches a blank canvas Anonymous visitors Shared-link and embed arrivals Self-hosted deployments New signups Invisible to the brief's KPI The only group measured What counts as preserving work Browser autosave Share link File download Image export Cloud save Green counts as activation today. Coral does not — though a user who autosaves and returns has succeeded. **The risk this creates:** the team could ship a "save more" intervention against a metric that is mislabeling successful users as churned. Before committing engineering time, confirm whether the problem is failure to start, failure to form a meaningful scene, failure to understand persistence, or simply an incorrectly defined KPI.

---

---

## 3\. The brief as submitted

**Owner:** Jacqueline, Head of Product **Stated remit:** Owns the product roadmap end to end — what gets built, in what order, and how success is measured. Weighs fast narrow wins against slower complete ones and allocates engineering time by quarter. **Current focus:** First-run experience — named as the stage with the highest loss and the most direct control over a fix.

**Stated KPI — Activation rate:**

> Percentage of new signups who complete and save their first drawing within their first session.

**Stated definition:**

| Element | As written in the brief |
| :---- | :---- |
| Start of measurement | User lands on a blank canvas |
| End of measurement | User has created and saved something, "no matter how rough" |
| Window | Same first session |
| Session reset | A "meaningful gap" starts a fresh activation attempt (illustrated as roughly one hour) |

**Stated rationale:** Every user who opens the app, gets confused, and closes the tab is a user the company never gets back. Word-of-mouth and embed links bring constant traffic, but unconverted traffic means paying an acquisition cost — in reputation, and in every person who made the recommendation — and throwing away the return. The brief argues that unlike most product metrics, first-session drop-off is one where a single well-placed change can move the number in weeks rather than quarters.

**What the brief gets right, and should be preserved:**

- First-run is a bounded, observable surface, not a guess at latent user desire.  
- The channel argument is sound: link- and embed-driven acquisition amplifies the cost of first-run failure.  
- The "weeks not quarters" claim is plausible — the welcome cue and first-action UI are testable without an editor redesign.

---

---

# Part II — The product and market, verified

## 4\. Verified product model

**This section is the factual backbone. Get agreement on it at the kickoff before discussing solutions.**

### 4.1 There are two products, and the brief does not say which one it means

|  | excalidraw.com (free / open source) | Excalidraw+ (app.excalidraw.com) |
| :---- | :---- | :---- |
| Account required | No | Yes |
| Landing behavior | Straight to a live blank canvas | Sign-in / sign-up flow |
| Persistence | Local browser storage; PWA with offline use | Cloud workspace, collections, archive/trash |
| File format | `.excalidraw` (JSON); PNG/SVG export | Adds PDF and PPTX export, versioning (in progress) |
| Collaboration | Real-time, end-to-end encrypted, via relay | Adds guest commenting, presentations, workspace roles |
| Trial | n/a | 14-day free trial |

**Confirmed:** Excalidraw is an open-source, web-based whiteboard usable without account registration. It runs as a PWA with local install and offline use, saving natively to browser storage, using a JSON-based `.excalidraw` format with PNG and SVG export, and running collaboration sessions through a relay with client-side end-to-end encryption.

**Open question \#1 — the most important one in this document:** Is this project aimed at the free hosted app, at Excalidraw+, or at a specific authenticated deployment? The answer determines whether "new signup" is a meaningful population at all.

### 4.2 Persistence model

**Confirmed:** The hosted free product stores drawings in browser storage and explicitly warns users that browser storage can be cleared unexpectedly, recommending regular saving to a file.

This single fact drives most of the analysis below. It means:

- Background local persistence and deliberate durable saving are **different states** and must be separate events in the analytics model.  
- A user can create real value, leave satisfied, and never perform the explicit action the brief's KPI requires.  
- The product's own warning copy is the seed of a trust problem, not just a disclaimer.

### 4.3 First-run surface (free hosted app)

On landing, a user sees: the blank canvas itself, the drawing toolbar, a short "Pick a tool & Start drawing\!" prompt, canvas movement guidance, and high-level actions including Open, Help, Live collaboration, Sign up, and export/preferences/language controls.

---

---

## 5\. What has already shipped — scope constraint for the kickoff

**Several of the user complaints above have already been addressed, but mostly on Excalidraw+, not the free app.** This changes what is actually available to work on and must be confirmed before proposing interventions.

### 5.1 Recent releases relevant to this project

| Shipped | Item | Relevance |
| :---- | :---- | :---- |
| Aug 2026 | New rendering engine for faster, higher-resolution PNG, PDF and PPTX exports | Touches H3 (export path) |
| Aug 2026 | Spotlight Me (view syncing), bucket fill, real-time AI streaming to canvas | Collaboration and creation speed |
| Aug 2026 | Localized "Sign up" / "Sign in" labels; improved mobile navigation layout | Directly touches the first-run surface |
| Jul 2026 | **Autoshape** — converts freehand sketches into clean geometric shapes and arrows (Shift+X) | Directly addresses the flow-friction complaint (7.3) |
| Jul 2026 | Scroll-back-to-content button enabled on mobile | Touches H4 (mobile friction) |
| Jun 2026 | **Autosave reliability fix** — changes were not being saved when the window was visible but unfocused | Directly addresses the data-loss reports (7.3) |
| Jun 2026 | Constant-width pen mode; tablet toolbar UX improvements | Touches H4 |
| May 2026 | **Guest commenting** — external collaborators can leave feedback without an account | Directly addresses the async-comment gap (7.3) |
| May 2026 | Redesigned passwordless and social login flows | Touches H5 (signup path) |
| Mar 2026 | **Precise text editing** — click on selected text places the cursor exactly where you point | Directly addresses the caret complaint (7.3) |
| Mar 2026 | Dedicated trash system with restore and bulk actions | Touches durability confidence |

### 5.2 On the public roadmap

**In progress:** Versioning ("track your drawings in time and revert if needed"), Export private scenes ("better no-vendor-lock-in"), Fulltext search, Generate anything (AI chat "to help you get started"), PDF import, MCP diagram layouting, Custom fonts, Jira & Confluence integrations, new library marketplace, database migration.

**Backlog:** PWA install for Plus, nesting with folders, shared library, SSO, better scene filtering, app-wide command palette, GitHub integration, self-hosting, enterprise tier.

### 5.3 Why this matters for the kickoff

Three things follow:

1. **Versioning and "Generate anything (AI)" are in flight and both bear directly on first-run activation.** An AI chat explicitly framed as helping users get started is an onboarding intervention already in progress. Coordinate rather than duplicate — **Open question:** who owns it, and is it in scope for this project?  
     
2. **Some fixes exist on Plus but not on the free app.** Guest commenting, autosave reliability, workspace persistence. If the project targets the free app, those wins are not available; if it targets Plus, several community complaints are already stale evidence.  
     
3. **Evidence has a shelf life.** Community complaints gathered without a date should be checked against the shipping record before being used as justification. Several of the strongest-sounding complaints predate the fix.

---

---

## 6\. Competitive landscape

*Researched September 15, 2026\. Framed around first-run specifically — what a new user encounters before they can draw — because that is the question this project is answering.*

### 6.1 The field

| Tool | Position | Account to start? | Free tier |
| :---- | :---- | :---- | :---- |
| **tldraw** | Closest direct competitor — polished open canvas, developer SDK | **No** | Whiteboard entirely free, no paid tier, no published board limits |
| **draw.io / diagrams.net** | Precise technical diagramming — UML, BPMN, ERD, cloud icons | **No** | Fully free, no paid tier; files live in the user's own storage |
| **Miro** | Enterprise workshops, facilitation, timers, voting | Yes | 3 editable boards; Starter \~$8/user/mo |
| **FigJam** | Figma's whiteboard; brainstorming next to design files | Yes | 3 files; paid seats from \~$3–5/user/mo |
| **Whimsical** | Structured product work — flows, wireframes, mind maps | Yes | 4 boards; AI on paid plans |
| **Mural** | Facilitated workshops, retrospectives, design sprints | Yes | Seat-priced |
| **Lucidchart / Lucidspark** | Formal diagrams, engineering documentation, enterprise | Yes | Hard caps on documents and shapes |
| **AFFiNE** | Local-first workspace merging docs, whiteboard, databases | No (local-first) | Free for individuals |
| **Apple Freeform / Obsidian Canvas / Microsoft Whiteboard** | Bundled into an ecosystem the user already pays for | Varies | Included |

### 6.2 The account-free position is the moat — and the KPI penalizes it

**Only tldraw and draw.io match Excalidraw's no-account start.** Every other significant competitor requires registration before a first drawing, and the three closest commercial rivals also cap free usage at 3–4 boards.

Independent comparisons name this as the defining advantage. One notes a user can go from nothing to a live collaborative whiteboard shared with five engineers in under thirty seconds, and that Miro, FigJam and Mural all require accounts and have loading sequences — calling the speed advantage significant for ad-hoc technical discussion. Another describes the category positioning simply: use Excalidraw to sketch without an account.

**This is the strongest external argument against the brief's KPI.** The property the market identifies as Excalidraw's primary differentiator — start drawing, no account — is the exact behavior "new signups who save a first drawing" scores as a failed activation. Competitive analysis, community sentiment (§7.2), and advocacy on X (§7.4) all converge on the same point from three independent directions.

**Strategic implication:** any first-run intervention that moves Excalidraw toward the gated pattern moves it toward its competitors' weakness, not its own strength. The §12 constraint — nothing sits in front of the drawing — is a competitive position, not just a design preference.

### 6.3 draw.io has already shipped Candidate 2's fix

**This is the most actionable finding in this section.**

draw.io's Smart Templates feature lets a user describe the diagram they want in natural language — their own examples include an emergency management flowchart for a power failure, and a swimlane diagram for software engineer onboarding — and then **select the diagram type from a dropdown before generating.** The user can insert the result or regenerate for an alternative.

That dropdown is precisely the routing step Candidate 2 proposes. A competitor has concluded that AI diagram generation needs explicit type selection rather than pure inference, and shipped it.

Two things follow:

1. **It de-risks Candidate 2\.** We are not proposing an unproven interaction. There is a shipped precedent in the same category solving the same failure.  
2. **It raises the stakes.** Our firsthand test — a prompt containing the word *flowchart* returning a class diagram (§7.3) — is a failure a competitor has already designed around. This is a gap, not an enhancement.

### 6.4 Templates — the gap Excalidraw is losing on

**This section was rewritten on September 16, 2026 following stakeholder direction. The earlier version argued against expanding templates. That analysis was wrong, and the reasoning below replaces it.**

**What the earlier version argued:** that shape and template depth is draw.io's strongest ground, that deep libraries serve users who already know what they're making, and that minimalism protects the speed advantage in §6.2.

**Why that was wrong:** it conflated two different things. A *shape library* — hundreds of UML, BPMN and cloud icons — does serve experts and would compromise minimalism. A *template* is the opposite: a small set of ready-made starting structures that answer the blank canvas's only real question, *what am I supposed to make here?* Adding four templates is not adding complexity. It is removing a decision.

**The competitive position.** draw.io's Smart Templates lets a user describe a diagram in plain language and then **select the diagram type from a dropdown before generating** (§6.3). That is templates and AI generation working as one feature, shipped, in a product that is free and requires no account. Excalidraw's AI has no equivalent step — which is why a prompt containing the word *flowchart* returned a class diagram (§7.3).

So the comparison is not "draw.io has more shapes." It is **draw.io solved the blank-canvas problem and the AI-routing problem with one feature, and Excalidraw has solved neither.**

**Why templates fit Excalidraw's model rather than fighting it:**

- They sit *before* the first mark, but they do not gate it. A user can ignore every template and draw freely — nothing is blocked, nothing is required.  
- They cost nothing in account terms. No signup, no friction, no commitment.  
- They shorten time-to-value, which is the property §6.2 identifies as the moat. A template makes the ten-second promise more true, not less.  
- They are the direct answer to drop-off hypothesis H1, blank-canvas uncertainty, which is our highest-ranked hypothesis in §10.

**Scope discipline still applies.** Four to six templates covering the common cases — flowchart, process flow, org chart, mind map — not a library competing with draw.io's hundreds of technical shapes. The win is in the first three seconds, not in breadth.

### 6.5 What the competitive read changes

- **Reinforces the KPI argument (§2, §8).** Three independent evidence streams now converge on the same conclusion.  
- **De-risks Candidate 2\.** A shipped competitor precedent exists for type selection ahead of generation.  
- **Hardens the "nothing in front of the drawing" constraint.** It is a competitive moat, not an aesthetic preference.  
- **Bounds Candidate 4\.** Durability messaging must not drift toward account creation — that is the competitors' pattern and Excalidraw's differentiator is its absence.  
- **Does not support a template-library expansion.** Out of scope for first-run activation, and a fight against draw.io's strongest ground.

### 6.6 Limitations

This is desk research from comparison articles and vendor pages, several of them published by competitors or by tools positioning themselves in the category — read directional, not neutral. Free-tier limits and pricing change frequently and should be re-verified before being quoted to the client. No hands-on first-run testing of competitor products was conducted; the account-free claims for tldraw and draw.io are consistent across multiple independent sources but were not verified by direct use.

### 6.7 Business models — and why they matter here

The competitors do not share a monetization model. Excalidraw's is unique among them, and that shapes what a first-run intervention can safely do.

| Tool | What's free | Where the revenue is |
| :---- | :---- | :---- |
| **Excalidraw** | Entire MIT-licensed product, self-hostable, no account | **Open-core** — Excalidraw+ cloud tier of the same product |
| **draw.io** | Entire web app, no user limit, files in the user's own storage | **Adjacent** — Atlassian Marketplace apps for Confluence and Jira |
| **tldraw** | Entire whiteboard, no paid tier | **The engine** — an independent London startup (founded 2022, Lux Capital / Amplify backed, $10M Series A) licensing its SDK to ClickUp, Padlet, Craft and others |
| **Miro / FigJam** | 3 boards or files, account required | **Seats** — per-user subscription |

**draw.io** gives the web app away completely and monetizes somewhere else entirely. Its Confluence integration has been described as the most successful paid app on the Atlassian Marketplace, priced around $34/month for 20 cloud users and scaling to roughly $920/month at 2,000, with data-center licensing from about $6,250 to $13,000 per year. The free tool is a funnel into enterprise integration revenue, which is why it can afford to have no paid tier and no user cap.

**tldraw** likewise has no paid tier on the whiteboard. Its commercial product is the SDK. One review notes the consequence directly: because the app is the SDK's showcase, its feature direction follows SDK customers rather than whiteboard users. Its source is also under a custom license rather than an open-source one, so it cannot be freely self-hosted or embedded — a real differentiator in Excalidraw's favor for data-sovereignty buyers.

**Excalidraw alone monetizes the upgrade.** draw.io monetizes adjacent, tldraw monetizes the engine, Miro and FigJam monetize seats. Excalidraw sells a paid tier of the same product it gives away.

### 6.8 Why users keep choosing it

Four properties, and they compound:

1. **No account.** Link to live collaborative canvas in under thirty seconds while gated competitors are still loading a signup form.  
2. **The hand-drawn aesthetic is functional, not cosmetic.** It signals *this is not finished, argue with me.* Polished diagramming tools invite people to treat a rough idea as a settled decision. One comparison names this explicitly as removing the "this is a finished design" misinterpretation.  
3. **MIT license and mature self-hosting.** Organizations with data-sovereignty requirements can run it themselves. tldraw's custom license cannot.  
4. **Link-and-embed distribution.** Every shared board is an acquisition channel.

**The strategic consequence, stated plainly for the kickoff:**

Excalidraw's growth engine is the free, account-free product. The brief's KPI measures the paid gate. Those are not the same funnel, and optimizing the second at the expense of the first would damage the mechanism that generates the traffic in the first place.

### 6.9 Time, not price — the argument that carries the rest

**Credit: Erasmo Concepcion raised this framing, and it reorganises the competitive case.**

The intuitive story is that Excalidraw wins because it is free. That story is wrong, and it is easy to disprove in one line: **Miro and FigJam are also free at entry.** So is Whimsical. Free is table stakes in this category, not a differentiator.

What separates them is what free *costs you*.

| Tool | Price to start | Time to start |
| :---- | :---- | :---- |
| **Excalidraw** | $0 | Open the page and draw |
| Miro | $0 (3 boards) | Account, password, email verification, load |
| FigJam | $0 (3 files) | Account, password, email verification, load |
| Whimsical | $0 (4 boards) | Account, password, email verification, load |

**The currency the user is spending at first run is time, not money.** A person mid-conversation who says "let me draw that" has a thought with a short shelf life. Ninety seconds of registration outlasts the thought. That is the entire competitive position, and it is why the comparison writers keep reaching for the same measurement — thirty seconds from nothing to a live shared canvas.

**Three consequences:**

**It reframes retention.** Retention here does not mean time on canvas. Nobody wants to be kept on a whiteboard for an hour. It means the person comes back next Tuesday when they need another sketch. A metric optimising session length would be optimising against the product's actual promise.

**It explains why the signup wall is fatal rather than merely annoying.** A signup wall does not cost the user money. It costs them the thought they were trying to capture. And the substitutes — draw.io, tldraw — charge nothing in either currency, so there is no switching cost to overcome because the user has invested nothing yet.

**It bounds every feature we build.** The test for any first-run intervention is not "is this free?" It is **"does this cost the user time before they have drawn anything?"** Templates pass — picking a starting structure is faster than facing a blank canvas. A durability message after a first drawing passes. A signup prompt on landing fails.

**Phrase for the readout:** *people do not choose Excalidraw because it is free. They choose it because it costs no time. The KPI measures the price gate, and the product competes on the time gate.*

### 6.10 Market position — who is actually most desired

"Most desired" splits three ways depending on what is measured. No single source ranks these head to head, so the ordering below is a reasoned read, not a scoreboard.

| Measure | Leader | Evidence |
| :---- | :---- | :---- |
| **Organizational adoption** | **Miro** | The whiteboard most organizations have already procured and trained people on. Comparative writing notes that trust in this category is largely a function of who else in the room already has an account |
| **Design-team standing** | **FigJam** | Inherits Figma's position with every design team; free tier caps at 3 files |
| **Open-source and developer mindshare** | **Excalidraw** | The most popular open-source whiteboard by a wide margin — 90,000+ GitHub stars, used by individual developers and enterprise engineering teams alike |
| **Trust among free tools** | **draw.io** | Carries the most trust among open options for the plain reason that it has been free, working and account-free for over a decade |

**Approximate overall ordering:** Miro → FigJam → Excalidraw → draw.io → tldraw → Lucidchart / Whimsical / Mural in narrower niches. This mixes different measures — revenue, install base, community size — and should be presented as a read, not a ranking.

**Where Excalidraw rates:** not first overall, first in its own category. It does not compete on enterprise procurement and is not structured to. Miro's advantage is that it has already been bought — not a fight Excalidraw can win or should pick.

**The strategic point for the kickoff:** Excalidraw's advantage is that a person can draw in ten seconds with no account. The two tools ranked above it cannot copy that without dismantling their own per-seat business model. It is defensible precisely because it is expensive for the market leaders to match.

### 6.11 Licensing — and why it is a distribution channel

| Tool | License | Self-hostable? | Embeddable commercially? |
| :---- | :---- | :---- | :---- |
| **Excalidraw** | **MIT — fully open source** | Yes, with the most mature deployment story in the category | Yes, freely |
| **draw.io** | Open source | Yes | Yes |
| **AFFiNE** | Open source, local-first | Yes | Free for individuals |
| **tldraw** | **Custom license — source-available, not open source** | **No** | **No — requires a commercial agreement** |
| Miro, FigJam, Whimsical, Mural, Lucidchart | Proprietary | No | No |

**tldraw is commonly miscalled open source and is not.** Its source is public but under a custom license rather than an OSI-approved one, so unlike Excalidraw it cannot be freely self-hosted or embedded in another product. Against the closest competitor on the positioning map, this is Excalidraw's clearest structural advantage.

**Licensing here is a distribution channel, not a philosophical position.** MIT plus mature self-hosting is how Excalidraw reaches enterprise buyers who would never get a proprietary whiteboard through a security or data-sovereignty review.

**It also produces a third invisible population.** Self-hosted deployments are users who by definition never create an account on excalidraw.com — alongside anonymous visitors and shared-link arrivals, a group the brief's KPI cannot see.

### 6.12 Positioning map

Plotting the field on two axes — friction before a first drawing, against structural depth — produces three readings:

Whiteboard tool positioning map

More structure, more features Draw immediately, no account Signup required first Minimal, fast the signup line tldraw free; SDK is the product Excalidraw open core; paid cloud tier draw.io free; revenue via Atlassian FigJam 3 files free; per seat Whimsical 4 boards free; per seat Miro 3 boards free; per seat Lucidchart hard caps; enterprise *Excalidraw highlighted. Everything right of the dashed line requires an account before a first drawing.*

**Excalidraw and tldraw occupy nearly the same point.** Same quadrant, same promise, same free-and-instant pitch. tldraw is the closest real rival, and the material difference between them is licensing (§6.11), not features.

**draw.io sits alone in the high-structure, no-account corner.** The only tool combining deep structural capability with account-free access — and the same company that has already shipped Candidate 2's fix (§6.3). This is the competitor to watch.

**Everything else sits on the far side of the signup line.** Miro, FigJam, Whimsical, Mural and Lucidchart all require registration before a first drawing, and the closest three also cap free usage at 3–4 boards.

That dividing line is the argument in one image: every tool to the right of it gates the account. The brief's KPI measures Excalidraw as though it lived on that side.

---

---

# Part III — What users say

## 7\. Voice of user

### 7.1 What users like

Sentiment is broadly positive, and the positive sentiment is specific: speed, informality, and keeping attention on thinking rather than design polish. **Reviewers describe it as a simple, fast whiteboard for diagrams, wireframes, user flows, presentations and especially interviews, repeatedly praising the clean distraction-free interface, keyboard shortcuts, libraries, dark mode, and cross-device support — with some valuing the end-to-end encryption even though the app feels less polished than heavier design tools.**

The emotional benefit users describe:

- "I can get an idea out quickly."  
- "It feels less intimidating than a polished diagramming tool."  
- "It's lightweight enough to use spontaneously."  
- "It fits inside my note-taking workflow."

**Product implication:** users do not want this to become a heavy enterprise diagramming tool. They want the speed and looseness preserved. Any first-run intervention that adds weight to the opening moment works against the thing users came for.

### 7.2 Reddit research

*Source pass conducted by Natalie Walker across r/Excalidraw, r/ObsidianMD and adjacent subreddits. Four themes, each with its product implication.*

**Theme 1 — Saving and file management are a recurring pain point.** The clearest product signal comes from a Mac client creator who describes the web app's lack of file management as troublesome and unsettling, noting that users often have to manually save and organize multiple Excalidraw files. Their proposed solution centers on automatic saving, grouping, direct file operations, and multiple export formats. A separate self-hosting discussion similarly criticizes an Excalidraw-based experience for not saving into file storage, while pointing to the need for explicit export and editable `.excalidraw` workflows.

*Implication:* Jacqueline is right to care about preservation — but the problem may not be that users fail to click "Save." It may be that they don't understand what is already auto-saved, where their drawing lives, whether it survives browser changes, which export choice is appropriate, or how to find and reopen the work later. That is a **first-run durability-confidence problem**, not a conversion problem.

**Theme 2 — Users like the speed of first creation.** Reddit users repeatedly describe the tool as quick, useful and lightweight for informal visual thinking. One daily-use thread calls it amazingly quick for diagrams and math exercises. A first-time user says the tool is good while asking how to improve their output, describing a readability and scaling issue. Posts about professional-looking drawings and use in design communities show users progressing from rough sketching to higher-fidelity visual communication.

*Implication:* The core proposition — make a first mark, produce a rough visual — is likely strong. Early abandonment may be less about not understanding that this is a drawing tool, and more about uncertainty *after* the first few interactions: how do I make this readable, how do I resize or organize it, how do I keep it, how do I get it into the rest of my work? This is the argument for measuring past first element: `first_element_created` → `meaningful_scene_reached` → `durable_action_taken`.

**Theme 3 — The product is frequently used inside other workflows.** A substantial share of Reddit discussion happens in the Obsidian community rather than the dedicated Excalidraw subreddit. Users describe it as part of a note-taking, knowledge-management or documentation workflow: the Obsidian integration lets them save drawings directly into a vault, keep an Excalidraw note alongside Markdown, and embed drawings so changes update automatically. Users also discuss the limits of browser-based workflows that require manually opening, loading, exporting and reinserting files.

*Implication:* First-run success should not be defined only as "a user saved a sketch." For many people, success is **"I got this sketch into my workflow."** A user who exports a PNG, embeds a drawing in a note, saves an `.excalidraw` file to a local folder, or shares a link has activated — even with no account.

**Theme 4 — Storage anxiety is real.** A Reddit thread explicitly describes the tool using local storage for drawing data, with elements stored as objects containing positional and styling information. This matches the hosted product's own disclosure that drawings are retained in browser storage and may be cleared unexpectedly. The pattern is consistent: users enjoy browser-based convenience but want stronger confidence that work is recoverable, portable and organized.

*Implication:* Test a **just-in-time preservation moment** after a user has made a meaningful first scene — not on landing. For example: *"Your drawing is safely available in this browser. To keep a permanent copy or open it elsewhere, download an editable .excalidraw file."* This makes current behavior legible, explains the benefit of the explicit action, and avoids interrupting the first-drawing flow with a signup wall.

**Reddit-led conclusions carried into the kickoff:**

| Brief assumption | Reddit evidence | Interpretation |
| :---- | :---- | :---- |
| Saving is central to first-run activation | Manual saving, file organization, browser storage and lack of direct file management recur as pain points | Supported — but "save" must include confidence, recoverability and retrieval, not just a click on an export menu |
| The blank canvas is the main barrier | Users praise speed and ease, but ask for help with readability, scaling and workflow integration | Partially supported — investigate whether abandonment happens before or after first creation |
| Signup should be part of activation | Use cases center on local files, Obsidian vaults, self-hosting and native clients rather than accounts | Not supported as a universal requirement |
| One core funnel can represent new users | Distinct paths visible: standalone web sketching, note-taking embeds, file-based workflows, self-hosting, collaboration | Not supported — segment by entry context and intended outcome |
| A small, focused change could improve activation | Saving and file-management confusion is concrete and repeated, so potentially responsive to clearer guidance or a simpler durable-save path | Plausible and worth testing, once the team identifies where the funnel breaks |

### 7.3 GitHub, issue-tracker and review-site evidence

**Loss of work is the sharpest, most emotional complaint, and it is documented directly.** This is the strongest evidence in the entire research set.

- A GitHub discussion titled "Frustrated about no auto-save and backup" describes losing hours of work several times, notes there is no backup and no prompt asking whether to save on exit, and says work is sometimes present on return and sometimes not. A second commenter confirms the cached version is sometimes current and sometimes an older canvas without the previous session's changes.  
- A separate discussion documents a user opening a permalink without realizing they had unsaved work, which replaced the canvas. A maintainer replied that nothing could be recovered, and that the team was working on making this clearer and on allowing save/export before content is replaced — with a longer-term plan to stop shareable links overriding the canvas at all, similar to collaboration rooms. Another commenter in the same thread lost an ER diagram after clearing browser cache and local storage.  
- A filed issue documents an hour of collaborative documentation work disappearing after switching browser windows and returning to the canvas, replaced by an earlier backed-up version.

**The signup moment itself is a documented point of data loss.** A filed issue describes a user who had weeks of work on the free version, decided to pay because the product was so good, and lost all of it on converting — with a request for a way to attach the free whiteboard to the new account. Two more issues show the same local-storage fragility outside the conversion path: one where a browser reboot cleared history and the canvas went blank, and one from February 2026 where images returned blank after a few weeks away, with no backup or export made.

**This is the single most important finding for Jacqueline's brief**, because it inverts the premise. The brief treats signup as the endpoint of a successful activation. At least one documented path makes signup the moment work is destroyed. Before optimizing anything toward signup conversion, confirm whether a free-tier-to-account migration path exists today.

**Expectation mismatch with Figma/FigJam is explicit.** A Product Hunt reviewer describes a bad experience: they did not realize work created in live collaboration mode would not be saved and had to save it manually, and attributes the confusion to coming from Figma/FigJam where that is built in.

**Other recurring themes:**

- *Workflow interrupts creative flow.* A mind-map feature request describes manually creating text, circles and arrows for each thought as too slow — it "breaks flow" and sends the user back to paper. The underlying statement: the product is good for thinking until its interaction model gets in the way of thinking.  
- *Collaboration feels incomplete for real teams.* A request for asynchronous comments compares the gap to Miro and FigJam capabilities — comments, timers, voting, feedback workflows. Particularly relevant to shared-link acquisition: a guest arrives, sees the value, then hits a wall trying to respond.  
- *Text, precision, and readability.* Community posts flag caret placement, fixed-width text indicators, auto-resize, and positioning of new text. A first-time user reported needing heavy zoom for readability. The statement underneath: "the hand-drawn look is appealing, but I still need readable output — if I can't make it legible, I can't confidently share it."  
- *Missing elements.* Review aggregation flags gaps in built-in elements such as tables and standard system-design icons.  
- *Version-change anxiety.* Obsidian plugin users report drawings failing to open after updates, with recovery advice involving `.excalidraw` files, backups and saved versions.  
- *Mobile and touch friction.* Pen mode, accidental palm touch and double-tap settings surface as workarounds rather than defaults.

### 7.4 X / Twitter

*Searched September 13, 2026\. X is weakly indexed and the sample is not representative — treat as directional. But what surfaces is unusually useful, because the sentiment there runs opposite to the brief's premise.*

**The most-amplified X commentary praises the onboarding specifically — and praises exactly what the brief's KPI penalizes.**

A widely circulated thread from a large developer account describes Excalidraw as the tool they'd find hardest to leave behind, crediting it with unlocking sketching for someone with handwriting they'd avoided since school. The reply thread names the onboarding mechanics explicitly and approvingly:

1. Generous free tier  
2. Use it for free without an account  
3. Hand-drawn defaults mean faster experiments  
4. Sensible paid features

The thread closes by calling the UX and onboarding delightful, and follow-on commentary in the same conversation frames the product mindset as the real advantage — not competing with heavyweight design tools, but extending the whiteboard, with simplicity as the focus.

**Why this matters more than its volume suggests.** Point 2 on that list — *use it for free without an account* — is cited as a reason the onboarding is good. Jacqueline's KPI scores that exact behavior as a failed activation. This is the sharpest available external statement of the measurement problem in §2, and it comes from an advocate, not a critic.

**Secondary signals on X:**

- **Figma comparison surfaces again**, this time as a feature ask: a user publicly asks the account whether a curve pen tool similar to Figma's is planned, and whether plugins can be explored. Consistent with the Product Hunt and Miro/FigJam comparisons in §7.3 — users benchmark against tools they already know.  
- **The official account's own posting pattern** is release-driven: performance improvements to shape creation and the freedraw tool, text-to-diagram AI with no API token required, open-sourcing mermaid-to-excalidraw, slide animation work in progress, and an open call to the community asking what to name a UI panel. That last one is notable — the team crowdsources naming publicly, which means first-run copy changes have a natural community-consultation path.  
- **No organized first-run complaint exists on X.** Data-loss frustration, which is the dominant negative theme everywhere else, is filed on GitHub rather than posted publicly. Users appear to complain about this product *to the maintainers*, not *about* them.

**Channel conclusion for the kickoff:** X carries advocacy and feature requests, not first-run pain. It is a poor prioritization source but a strong source for understanding what advocates believe the product's value is — and the advocates believe it is frictionless, account-free immediacy. Any first-run intervention that compromises that will be visible and unpopular on this channel.

### 7.5 Where concerns are voiced

| Channel | What users express there | Best research use |
| :---- | :---- | :---- |
| GitHub issues | Specific gaps, reproducible bugs, workflow constraints, data-loss reports | Strongest source for concrete unmet needs; maintainer replies reveal roadmap intent |
| GitHub discussions | Broader feedback, suggestions, design opinions, integration ideas | Product direction and what engaged contributors want |
| r/Excalidraw | Feature updates, troubleshooting, interaction concerns | Useful but small and technically skewed |
| r/ObsidianMD | Workflow feedback from people using it inside a knowledge system | Best source on persistence, file behavior, embeds, repeat use |
| Product Hunt reviews | Summarized comparative sentiment vs Figma/FigJam and Miro | Good for expectation-mismatch signals |
| X / Twitter | Quick bug reports, shortcut complaints, support questions | Rapid anecdotal monitoring; weak for prioritization |

### 7.6 The one-sentence synthesis

User sentiment is not "Excalidraw is bad." It is closer to:

> "Excalidraw is wonderful when I want to think visually and quickly — but I get frustrated when I need it to be organized, precise, durable, or collaborative in the ways my real work requires."

**This reframes the first-run opportunity.** The job is not to teach a newcomer every capability. It is to deliver the core emotional payoff — *I can make an idea visible quickly* — and then reduce anxiety at the exact moments users ask: Can I make this look right? Will I lose it? Can I get this into my workflow? Can I share it and get feedback? Why should I create an account?

---

---

# Part IV — What it means

## 8\. KPI assessment

### 8.1 Unresolved measurement decisions

The definition is directionally useful but is **not instrumentable** until these are decided:

| Decision | Why it blocks instrumentation |
| :---- | :---- |
| **Who is eligible** | The free app presents "Sign up" as an option, not a gate. Limiting eligibility to registered users excludes most anonymous first-run traffic from links, embeds, and direct visits. |
| **What "complete" means** | One element? Two connected shapes? A text-labeled diagram? Without an intent signal, accidental marks inflate the numerator. |
| **What "save" means** | Autosave to browser storage, `.excalidraw` download, PNG/SVG export, share-link creation, and cloud workspace save are five different behaviors with five different difficulty levels. |
| **How sessions reset** | "Meaningful gap" must become a fixed analytics rule (e.g. 30 minutes of inactivity). Also define whether blur, tab close, background return, or refresh terminates a session. |
| **Whether collaboration arrivals count** | A person arriving via a live collaboration link is not in a blank-canvas solo flow. Their motivation and path differ materially. |

### 8.2 Recommended metric architecture

Use nested metrics rather than one overly strict metric. This preserves Jacqueline's business question while stopping the KPI from mislabeling successful users.

| Metric | Definition | What it answers |
| :---- | :---- | :---- |
| **Core creation activation** *(primary)* | % of eligible first-run visitors who create a meaningful scene during their first active session | Does the product get users to its core value — turning a blank canvas into an idea? |
| **Durable-work activation** *(downstream qualifier)* | % of core-activated users who explicitly export/download, create a shareable link, or save to an authenticated workspace | Does the created work become recoverable, portable, or shareable? |
| **Signup activation** *(segment, not universal KPI)* | % of new signups who create a meaningful scene **and** take a durable-work action in the same first active session | Retains Jacqueline's original business question, scoped correctly |

**Proposed formula for the primary metric:**

```
Core activation = eligible first-run users who reach a meaningful scene
                  ─────────────────────────────────────────────────────
                  eligible first-run users who view a new blank canvas
```

**Proposed starting rule for the core event** (conservative, to be validated before it is treated as authoritative):

> User creates at least two non-deleted elements, **or** one text element plus one non-text element, **and** remains active for at least 10 seconds after the first creation.

**Validation required:** check this rule against session replays or a manually reviewed sample before locking it in.

---

---

## 9\. First-run map and event taxonomy

| Stage | Observable behavior | User's likely question | Event to capture |
| :---- | :---- | :---- | :---- |
| Entry | User reaches a live canvas, not a marketing page or signup gate | "What am I supposed to make here?" | `first_canvas_viewed` (+ entry source) |
| Orientation | Welcome copy explains tool choice; toolbar exposes shapes, text, drawing | "Which tool should I use first?" | `welcome_seen`, `tool_selected` |
| First mark | User places an element or writes text | "Can I make this quickly and correctly?" | `first_element_created` |
| Scene formation | User adds, edits, moves elements into something meaningful | "Is this usable for my actual task?" | `meaningful_scene_reached` |
| Preservation | Local persistence happens in background; explicit export available | "Will I lose this? How do I keep or send it?" | `autosave_confirmed`, `export_opened`, `file_downloaded` |
| Sharing / collaboration | Live collaboration available | "How do I bring someone else in?" | `collab_started`, `share_link_created` |
| Account conversion | Sign-up available, not required | "Why should I create an account now?" | `signup_started`, `signup_completed` |

First-run funnel with hypothesised drop-off points

Canvas viewed First element created Meaningful scene reached Durable action taken Widths are illustrative — no baseline data exists yet (see §13, open question 4\) H1, H4 H2, H3 **Segmentation dimensions to carry on every event:** entry source (direct, embed, shared link, docs, referral), device and viewport, signed-in vs anonymous, solo vs collaboration guest.

---

---

## 10\. Drop-off hypotheses

**All six are research-backed hypotheses, not confirmed funnel losses.** They are ordered by estimated leverage, and each carries the measurement that would confirm or kill it.

**H1 — Blank-canvas uncertainty.** The user reaches an empty canvas with a compact prompt and a multi-tool interface. People arriving from a shared diagram or a recommendation may understand the aesthetic but lack a concrete first task. *Failure mode:* no tool selection, no first element. *Test:* rate of `first_canvas_viewed` → `tool_selected`, and time-to-first-tool by source.

**H2 — The "saved" mental-model gap.** Users reasonably assume work is safe because it stays on screen. The product's own warning says otherwise. A user can create a drawing, leave satisfied, and never perform the explicit action the KPI requires. *Test:* share of sessions reaching a meaningful scene with zero export/share/download events, cross-referenced against return rate.

**H3 — Explicit save and export discoverability.** The product distinguishes export, save to active file, save as image, and save file to disk. These are conceptually distinct preservation paths, not one obvious "Save my drawing" action. *Test:* export-menu open rate, and export-menu abandonment rate.

**H4 — Tool-choice and interaction friction.** Shapes, drawing tools, text, shortcuts, canvas movement, menus, and collaboration are all presented at once. Experienced diagrammers move fast; casual and mobile visitors may not infer the shortest path from intention to first mark. *Test:* time-to-first-element split by viewport, device, and acquisition source.

**H5 — Premature signup measurement boundary.** If signup is a prerequisite in the metric but not in the product's core use case, users who successfully create and retain a local drawing are scored as failures. Highest risk on shared-link and embed traffic — which the brief itself names as the main discovery channel. *Test:* recompute the brief's KPI with an anonymous-inclusive denominator and compare.

**H6 — Collaboration as a diversion before solo value.** Live collaboration is valuable, but a novice pushed to share before making a basic diagram faces permissions, links, and co-editing decisions before experiencing the drawing payoff. *Test:* instrument as a parallel path; compare activation of collaboration-link arrivals against solo arrivals.

---

---

## 11\. Brief assumptions vs. research

| Brief assumption | Research finding | Implication |
| :---- | :---- | :---- |
| New users begin by signing up, then land on a blank canvas | The free hosted app exposes the canvas immediately; Sign up is visible but not blocking | Segment signup users; make visitor-level first-run activation the primary population |
| A user must manually save to preserve a drawing | Drawings persist to browser storage automatically, with a warning that storage may be cleared | Separate automatic local persistence from explicit durable saving |
| "Save first drawing" is one behavior | Product distinguishes export, save to active file, save as image, save to disk, share link, cloud save | Define which actions qualify; report each separately |
| Saving is central to first-run activation | Supported — but data-loss reports show the issue is confidence and recoverability, not clicking an export menu | Reframe from "get them to save" to "make persistence legible and trustworthy" |
| The blank canvas is the main barrier | Partially supported — users praise speed, but ask for help with readability, scaling, and workflow integration | Determine whether abandonment happens *before* first creation or *after* users have begun |
| Signup should be part of activation | Not supported as a universal requirement — heavy use centers on local files, Obsidian vaults, self-hosting, native clients | Treat signup as a segment or downstream conversion event |
| One core funnel can represent new users | Not supported — distinct paths: solo web sketching, note-taking embeds, file-based workflows, self-hosting, collaboration guests | Segment the funnel by entry context and intended outcome |
| A single well-placed change could move activation quickly | Plausible — the welcome cue and first-action UI are bounded, testable surfaces | Validate through experiment, after locating the break |
| First-session drop-off is directly observable | The brief states the team can watch where people give up, but supplies no analytics taxonomy or baseline | Confirm instrumentation, data quality, sessionization, consent rules, and baselines first |

---

---

# Part V — What we do next

## 12\. Product constraints to carry into discovery

- **Local-first persistence.** Browser storage supports fast anonymous use but creates durability risk. This is a deliberate design property, not a bug to remove.  
- **Account-optional use.** Signup must deliver clear incremental benefit rather than block the initial creative act. Gating the canvas would break the product's core value proposition.  
- **Collaboration is an alternate journey.** A solo blank-canvas-to-saved-drawing funnel cannot be assumed to represent every new arrival.  
- **Editor complexity is purposeful.** Toolbar, shortcuts, drawing controls, import/export, language and preference controls cannot simply be removed. Reduce cognitive load without hiding expert capability.  
- **Persistence and export are differentiated.** Loading scenes, saving to active file, saving as image, and configurable disk export are separate states in the analytics model.  
- **Open-source governance.** Changes to the free app surface sit in a public repository with an engaged contributor community. Factor review and community response into timelines.  
- **Speed is the brand.** Every proposed intervention should be tested against: does this slow down the first thirty seconds?

---

---

## 13\. Open questions — status after discovery

**Resolved at the September 16 session:**

| Question | Answer |
| :---- | :---- |
| Which product? | **Free tier at excalidraw.com** |
| Should signup come earlier in the flow? | **No.** Users should experience value before being asked to register |
| What is in scope this quarter? | **User-facing features.** Templates first; instrumentation out of scope |

**Still open — and the first one matters:**

1. **Where do the current activation metrics come from?** The stakeholder was not able to identify the source. Instrumentation is out of scope by direction, but the gap is unresolved, and no baseline exists for any feature we ship.  
2. **Which 3–5 templates?** Flowchart, process flow, org chart and mind map are our working assumption, not confirmed.  
3. **What event currently represents "save" in the data** — autosave, download, export, share link?  
4. **What is the traffic mix** across anonymous, signed-in, shared-link and embed arrivals?  
5. **Does a free-tier-to-account migration path exist today?** At least one documented case shows a paying convert losing all prior free-tier work. If that is still true, signup conversion cannot be an activation goal until it is fixed.  
6. **Who owns the "Generate anything" AI chat already on the public roadmap?** It is framed as helping users get started, which overlaps our templates work directly.  
7. **Voice-to-text prompt input** — raised at discovery, unscoped, no owner.

---

## 14\. Recommended next steps

**Do not commit to a "save more" solution at kickoff.**

**Decision to put to the room:** Are we optimizing for first meaningful creation, explicit durable preservation, signup conversion, or a sequenced combination of all three?

**Recommended sequence:**

1. **Settle scope** — answer Open question \#1 before anything else.  
2. **Fix the KPI** — adopt the nested metric architecture in §8.2; get sign-off on the core-event rule.  
3. **Instrument and baseline** — ship the event taxonomy in §9 with full segmentation; establish baselines before proposing interventions.  
4. **Validate the event rule** — review session replays or a manual sample against the meaningful-scene definition.  
5. **Locate the break** — determine whether loss occurs before first element, between first element and meaningful scene, or after.  
6. **Then design the intervention** — and only then.

**One qualitative study worth running in parallel**, cheap and high-signal: a small set of moderated first-session tests where the single most important question is asked at the end —

> *"Where do you think this drawing is saved right now?"*

**Leading hypothesis going into the kickoff:** users may create value quickly but leave without durable-save confidence or a clear path to move the work into the tools they already use.

---

---

## Appendix A — Sources

Primary product sources, retrieved September 13, 2026:

- Excalidraw+ changelog — [https://plus.excalidraw.com/changelog](https://plus.excalidraw.com/changelog)  
- Excalidraw+ public roadmap — [https://plus.excalidraw.com/roadmap](https://plus.excalidraw.com/roadmap)  
- Free hosted app — [https://excalidraw.com](https://excalidraw.com)  
- Repository — [https://github.com/excalidraw/excalidraw](https://github.com/excalidraw/excalidraw)  
- Excalidraw overview (technical model, PWA, file formats, encryption) — [https://en.wikipedia.org/wiki/Excalidraw](https://en.wikipedia.org/wiki/Excalidraw)

User-report sources:

- "Frustrated about no auto-save and backup" — GitHub Discussion \#6463 — [https://github.com/excalidraw/excalidraw/discussions/6463](https://github.com/excalidraw/excalidraw/discussions/6463)  
- "I accidentally cleared the canvas, is there a way to restore the previous drawing?" — GitHub Discussion \#6648 (includes maintainer response on planned save/export prompt and shareable-link behavior) — [https://github.com/excalidraw/excalidraw/discussions/6648](https://github.com/excalidraw/excalidraw/discussions/6648)  
- "excalidraw lost my data" — GitHub Issue \#8817 — [https://github.com/excalidraw/excalidraw/issues/8817](https://github.com/excalidraw/excalidraw/issues/8817)  
- "How does export utilities work and how do I save my drawing?" — GitHub Discussion \#3778 — [https://github.com/excalidraw/excalidraw/discussions/3778](https://github.com/excalidraw/excalidraw/discussions/3778)  
- "Loss of all the work when going from free to subscribing" — GitHub Issue \#6671 — [https://github.com/excalidraw/excalidraw/issues/6671](https://github.com/excalidraw/excalidraw/issues/6671)  
- "I lost all my excalidraw (maybe due to Arc browser data)" — GitHub Issue \#7870 — [https://github.com/excalidraw/excalidraw/issues/7870](https://github.com/excalidraw/excalidraw/issues/7870)  
- "Lost all images" — GitHub Issue \#10765 (February 2026\) — [https://github.com/excalidraw/excalidraw/issues/10765](https://github.com/excalidraw/excalidraw/issues/10765)  
- "Lost my data" — GitHub Discussion \#6487 — [https://github.com/excalidraw/excalidraw/discussions/6487](https://github.com/excalidraw/excalidraw/discussions/6487)  
- Obsidian Excalidraw plugin — drawings inaccessible after update — [https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/2235](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/2235)  
- Product Hunt reviews (comparative sentiment, live-collaboration save complaint) — [https://www.producthunt.com/products/excalidraw/reviews](https://www.producthunt.com/products/excalidraw/reviews)  
- X / Twitter — advocacy thread on onboarding and account-free use — [https://x.com/theo/status/1571229812907462656](https://x.com/theo/status/1571229812907462656)  
- X / Twitter — official account, release posting pattern and community replies — [https://x.com/excalidraw](https://x.com/excalidraw)

Competitive research, retrieved September 15, 2026:

- draw.io Smart Templates (AI template generation with explicit diagram-type selection) — [https://drawio-app.com/blog/smart-templates-from-draw-io/](https://drawio-app.com/blog/smart-templates-from-draw-io/)  
- Excalidraw alternatives comparison — [https://ponder.ing/blog/excalidraw-alternatives](https://ponder.ing/blog/excalidraw-alternatives)  
- Excalidraw alternatives, 2026 — [https://sliplane.io/blog/5-awesome-excalidraw-alternatives](https://sliplane.io/blog/5-awesome-excalidraw-alternatives)  
- tldraw review (no-account start, pricing, licensing) — [https://freealternatives.to/tldraw/review](https://freealternatives.to/tldraw/review)  
- tldraw alternatives, hand-drawn whiteboards compared (shape library depth, free-tier caps) — [https://codepic.cc/blog/tldraw-alternatives](https://codepic.cc/blog/tldraw-alternatives)  
- Open source whiteboard tools, 2026 — [https://www.opensourcealternatives.to/blog/best-open-source-whiteboard-tools](https://www.opensourcealternatives.to/blog/best-open-source-whiteboard-tools)  
- Best Excalidraw alternatives, tested and ranked — [https://storyflow.so/blog/best-excalidraw-alternatives-2026](https://storyflow.so/blog/best-excalidraw-alternatives-2026)  
- draw.io pricing and Atlassian positioning — [https://drawio-app.com/pricing/](https://drawio-app.com/pricing/)  
- draw.io Confluence app, Atlassian Marketplace — [https://marketplace.atlassian.com/apps/1210933/draw-io-diagrams-uml-bpmn-aws-erd-flowcharts](https://marketplace.atlassian.com/apps/1210933/draw-io-diagrams-uml-bpmn-aws-erd-flowcharts)  
- draw.io as the leading paid Confluence app — [https://seibert.group/blog/en/draw-io-diagramming-in-confluence-is-currently-the-most-successful-app-in-the-atlassian-marketplace/](https://seibert.group/blog/en/draw-io-diagramming-in-confluence-is-currently-the-most-successful-app-in-the-atlassian-marketplace/)  
- draw.io integration pricing tiers — [https://techradar.com/reviews/drawio](https://techradar.com/reviews/drawio)  
- Reddit source pass (Natalie Walker): r/Excalidraw, r/ObsidianMD and adjacent subreddits — covering Mac client file-management critique, self-hosting storage discussion, daily-use and first-time-user threads, Obsidian vault and embed workflows, and local-storage data-structure discussion. See §7.2.

---

## Appendix B — Research limitations

**Community feedback is qualitative and self-selected.** Posts skew toward engaged users, power users, integration builders, and people who hit enough friction to seek help or build a workaround. It cannot establish the volume of a problem or prove that a given friction causes first-session abandonment. Treat it as a hypothesis source only.

**No product analytics were available for this research.** Every funnel claim in this document is a hypothesis. Nothing here has been checked against Excalidraw's own instrumentation.

**X/Twitter indexing is poor and the sample is not representative.** What surfaced is advocacy and feature requests rather than a representative cross-section. §7.4 should be read as directional, and its main value is as evidence of what advocates believe the product's value is — not as a measure of how common any view is.

**Dates matter.** Several strong-sounding complaints predate fixes shipped in 2026 (see §5). Check any complaint's date against the shipping record before citing it.

**Validate hypotheses against:** funnel conversion by entry source; time from canvas view to first element; time from first element to meaningful scene; export-menu open and abandonment rates; first-session rate of download, share-link creation, collaboration start, and account creation; return rate for users who create but take no durable action.

---

## Appendix C — Document control

The full version history is at the front of this document, under the team roster. It is not repeated here to avoid two records that can drift apart.

**Current version: 3.1 — September 16, 2026**

**Next review:** after the template prototype is shown to the client. Update §5 if new releases ship before then.
