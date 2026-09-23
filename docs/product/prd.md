**AI AFFAIR · INTERNAL**

# **PRD — EXCALIDRAW FIRST-RUN ACTIVATION**

| TEAM AI AFFAIR |  |  |  |
| :---- | :---- | :---- | :---- |
| **Team Member** | **Role** | **Team Member** | **Role** |
| Natalie Walker | Product Manager | Sean Pisano | Back-end Developer |
| Nicole Rodríguez | Front-end Developer · UI / UX | Erasmo Concepcion | Security & Debugging Lead |
| **Build / Scope** | Excalidraw First-Run Activation · Free tier at excalidraw.com | **Version / Status** | v2.0 · Sep 16, 2026 · Post-discovery team review |
| **References** | Source of Truth v3.1 · Build Plan v2.0 | **Owner** | Natalie Walker · Team AI Affair |

# **1\. PROBLEM**

New Excalidraw visitors can draw immediately with no account, but first run does not consistently move them to the useful diagram they intended to make. The brief counts “new signups who complete and save a first drawing,” although the free app requires no signup and “save” can mean browser persistence, file or image export, a share link, or cloud save. Successful anonymous use can therefore be misread as churn. Research also found an AI-routing failure: a garment-production “flowchart” prompt returned a UML class diagram. The renderer followed the selected grammar; the wrong type was chosen upstream. Durability has improved behind the scenes, but first-time users may still not know where work lives or how to keep it.

### **Supporting Context**

* 09/16 discovery confirmed the free tier and that users should experience value before signup pressure.

* Browser-local work can be lost when storage is cleared or a user changes device or browser; explicit durable actions remain separate.

* draw.io already offers explicit diagram-type selection before AI generation; tldraw and draw.io also match Excalidraw's account-free start.

## **1A. OPPORTUNITY**

Create a faster path to a recognizable first diagram without sacrificing Excalidraw's defining advantage: almost no time before drawing. The governing test is time, not price — reduce friction without putting a gate in front of the canvas.

### **Market Opportunity**

* Excalidraw has 90,000+ GitHub stars and competes against larger signup-gated tools; account-free speed is its differentiated position.

* Source of Truth v3.1 holds the research, competitive analysis, discovery record, evidence limitations, and the unresolved analytics-source question.

## **1B. USERS & NEEDS**

| User | Need |
| :---- | :---- |
| Primary — first-time free-tier visitor | Start quickly, see a useful structure, and get the diagram type requested — with no account. |
| Shared-link / embed arrival | Create a new diagram from someone else's link without signup or losing the viewed scene. |
| Returning / casual creator | Know where work lives and how to keep or export a durable copy. |

# **2\. PROPOSED SOLUTION**

The proposed MVP adds Templates \+ Diagram-Type Routing to the free-tier canvas. Users can choose 3–5 starting structures (flowchart, process flow, org chart, mind map), ignore or dismiss the picker, or describe a diagram and select its type before AI generation. Template choice biases the matching Mermaid grammar; if routing is not modifiable, static templates still ship. The canvas stays immediately usable and no signup prompt is introduced.

## **2A. VALUE PROPOSITION**

First-time users get a starting structure plus explicit diagram-type selection so they can reach a usable diagram quickly. Unlike gated onboarding, the solution preserves account-free creation and delivers value first.

## **2B. TOP 3 MVP VALUE PROPS**

| Type | Value |
| :---- | :---- |
| Vitamin | Visible starting structures so the first move is obvious. |
| Painkiller | Explicit type selection so “flowchart” produces a flowchart, not a class diagram. |
| Steroid | Pick a template, type one sentence, and get a correctly structured diagram in under ten seconds with no account. |

## **2C. GOALS & NON-GOALS**

| Goals | Non-Goals |
| :---- | :---- |
| Recognizable first diagram in the opening session without an account. | No editor redesign or deep UML / BPMN / cloud-icon library. |
| Requested AI diagram type, with user override. | No canvas gate or signup prompt inside this feature. |
| Preserve speed: nothing sits in front of drawing. | No AI-model rebuild or diagram-layout fix. |
| Clarify durable work after value; retain prompt-history and persistence findings. | No activation-instrumentation build in this exercise; assume analytics exist or are provided. |

## **2D. SUCCESS METRICS**

| Goal | Signal | Metric | Target |
| :---- | :---- | :---- | :---- |
| Correct diagram type | Output matches the type asked for | Correct-type rate on fixed 50-prompt baseline | ≥90% |
| First useful diagram | Users place elements rather than leaving empty | Template-start sessions reaching meaningful scene | ≥60% |
| Template discoverability | Users open the picker unprompted | First-run sessions opening picker | ≥40% |
| Speed preserved | Canvas remains immediately usable | Added template-layer load time | 0 ms measurable delay |
| Generation stays fast | Users do not wait on classification | Added type-classification latency | ≤1 second |

**Meaningful scene** \= 2+ non-deleted elements, or 1 text \+ 1 non-text element, plus 10 seconds of activity. Tab close ends a session; refresh does not. Validate against at least 30 sessions. Targets for first-useful-diagram and discoverability are provisional — no baseline exists while instrumentation is parked.

# **3\. REQUIREMENTS**

## **User Journey 1 — First-time visitor making a first diagram**

**Context:**  Highest-loss stage and client priority. The user has a specific diagram in mind, no account, and should be able to draw immediately.

### **Sub-journey: Starting point**

* **\[P0\]**  User can open the template picker from the first-run canvas.

* **\[P0\]**  User can see 3–5 templates: flowchart, process flow, org chart, mind map.

* **\[P0\]**  User can select a template and see its structure placed on the canvas.

* **\[P0\]**  User can ignore every template and draw freely.

* **\[P0\]**  User can dismiss the picker without selecting anything.

* **\[P1\]**  User can preview a template before selecting it.

* **\[P2\]**  User can see templates suggested by recency or popularity.

### **Sub-journey: AI generation**

* **\[P0\]**  User can describe a diagram in natural language and select its type before generating.

* **\[P0\]**  User can state a type in the prompt and have that term override inference.

* **\[P0\]**  User can see which diagram type was chosen.

* **\[P0\]**  User can override the chosen type and regenerate without rewriting the prompt.

* **\[P0\]**  User receives a flowchart by default when classification confidence is low.

* **\[P1\]**  User receives output styled appropriately to the diagram type.

* **\[P2\]**  User can regenerate for an alternative version of the same type.

### **Sub-journey: Keeping work**

* **\[P0\]**  User can complete the entire flow without an account.

* **\[P0\]**  User encounters no signup prompt anywhere in the flow.

* **\[P1\]**  User can download an editable .excalidraw file or an image.

### **Sub-journey: Prompt history — secondary, build only if capacity allows**

* **\[P0\]**  User can see prompt text and timestamp stored for their session.

* **\[P0\]**  User can see prompts listed in reverse chronological order.

* **\[P0\]**  User can re-run a stored prompt exactly.

* **\[P0\]**  User can see an empty state and an error state rather than a blank panel.

* **\[P0\]**  User can delete an individual prompt.

* **\[P0\]**  User can keep drawing — the panel never blocks the canvas.

* **\[P1\]**  User's history is capped at 50 entries.

* **\[P1\]**  User can copy a prompt without re-running it.

## **User Journey 2 — Shared-link arrival starting a new diagram**

**Context:**  Link and embed traffic is the product's primary discovery channel. These users did not choose the tool — they clicked someone else's diagram.

* **\[P0\]**  User can start a new diagram from a shared scene without losing the scene they arrived to view.

* **\[P0\]**  User can reach the template picker from that new canvas.

* **\[P1\]**  User can see template choices relevant to the diagram type just viewed.

## **Delivery, Security & QA Constraints**

* **Design and scope.** Templates over a deep shape library; templates merged with routing; static templates still ship if routing is unavailable; no signup prompt; free tier uses browser-local persistence.

* **Build sequence.** Natalie P0/P1 ACs → Erasmo pre-build security and privacy → Sean schema, endpoints, data contract → Nicole and Sean parallel build → integration → Erasmo evals, Mercator, regression, debug audit → fixes → regression re-run.

* **Technical and QA.** Sean runs a one-day Mermaid spike; public-repo review time and fork-vs-sandbox remain open. Test wrong type, unavailable routing, low confidence, prompt and privacy failures, PII or content leakage if analytics resumes, performance, and persistence timing or blocking.

* **Two-week scope.** Prompt history \= session plus re-run, no cross-device sync; routing \= four types, no full Mermaid layout work; instrumentation \= core funnel and entry source only if resumed; persistence \= one desktop trigger, message and action. Never cut security or privacy.

# **4\. APPENDIX**

### **Discovery Priority**

* **1\. Templates \+ Diagram-Type Routing** — client top priority; static templates still ship if Sean's routing spike is negative.

* **2\. Persistence \+ export** — secondary.

* **3\. AI prompt history** — secondary; privacy and retention first.

* **4\. Activation instrumentation** — parked; assume analytics exist or are provided.

* **Voice-to-text** — raised at discovery; unscoped and unowned.

### **Acceptance Criteria Map**

Every requirement in section 3 carries a stable ID for coverage mapping. Mercator parses this table and the P0/P1/P2 tags to build the AC-to-test map; IDs follow journey.sub-journey.requirement. Do not renumber without telling Erasmo Concepcion — the coverage history in ac-mapping-history.md is keyed to these IDs. The previous numbering (AC-1.1 to AC-4.9) covered four candidates and is superseded.

| AC ID | Priority | Requirement |
| :---- | :---- | :---- |
| AC-1.1.1 | **P0** | Open the template picker from the first-run canvas. |
| AC-1.1.2 | **P0** | See 3–5 templates: flowchart, process flow, org chart, mind map. |
| AC-1.1.3 | **P0** | Select a template and see its structure placed on the canvas. |
| AC-1.1.4 | **P0** | Ignore every template and draw freely. |
| AC-1.1.5 | **P0** | Dismiss the picker without selecting anything. |
| AC-1.1.6 | **P1** | Preview a template before selecting it. |
| AC-1.1.7 | **P2** | See templates suggested by recency or popularity. |
| AC-1.2.1 | **P0** | Describe a diagram in natural language and select its type before generating. |
| AC-1.2.2 | **P0** | State a type in the prompt and have that term override inference. |
| AC-1.2.3 | **P0** | See which diagram type was chosen. |
| AC-1.2.4 | **P0** | Override the chosen type and regenerate without rewriting the prompt. |
| AC-1.2.5 | **P0** | Receive a flowchart by default when classification confidence is low. |
| AC-1.2.6 | **P1** | Receive output styled appropriately to the diagram type. |
| AC-1.2.7 | **P2** | Regenerate for an alternative version of the same type. |
| AC-1.3.1 | **P0** | Complete the entire flow without an account. |
| AC-1.3.2 | **P0** | Encounter no signup prompt anywhere in the flow. |
| AC-1.3.3 | **P1** | Download an editable .excalidraw file or an image. |
| AC-1.4.1 | **P0** | See prompt text and timestamp stored for the session. |
| AC-1.4.2 | **P0** | See prompts in reverse chronological order. |
| AC-1.4.3 | **P0** | Re-run a stored prompt exactly. |
| AC-1.4.4 | **P0** | See an empty state and an error state rather than a blank panel. |
| AC-1.4.5 | **P0** | Delete an individual prompt. |
| AC-1.4.6 | **P0** | Keep drawing — the panel never blocks the canvas. |
| AC-1.4.7 | **P1** | History capped at 50 entries. |
| AC-1.4.8 | **P1** | Copy a prompt without re-running it. |
| AC-2.1.1 | **P0** | Start a new diagram from a shared scene without losing the viewed scene. |
| AC-2.1.2 | **P0** | Reach the template picker from that new canvas. |
| AC-2.1.3 | **P1** | See template choices relevant to the diagram type just viewed. |

### **Open Questions**

* Final 3–5 templates; activation-metric source; is Mermaid routing modifiable; voice-to-text scope and owner; 50-prompt baseline; fork vs sandbox; Mercator adaptation.

### **References & History**

* Source of Truth v3.1 · Build Plan v2.0 · UX mocks and meeting notes.

* v0.1 09/14 · v0.2 09/15 · v1.0–1.1 09/16 · v2.0 Pursuit-template reformat.

*Team AI Affair · Pursuit L3 · September 2026*
