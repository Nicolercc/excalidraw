# **FEATURE ROADMAP**

| Feature name | Templates \+ Diagram-Type Routing |
| :---- | :---- |
| **Team** | AI Affair — Natalie Walker, Nicole Rodríguez, Sean Pisano, Erasmo Concepcion |
| **Client** | Jacqueline Reverand, Head of Product — Excalidraw |
| **Date** | September 22, 2026 |

# **1\. Milestones**

| Day | Date | What has to be true by the end of this day | Status |
| :---- | :---- | :---- | :---- |
| Day 15 | 9/16/2026 | A hardcoded template picker renders on the first-run canvas with 3–5 template options visible. No selection behaviour and no real data yet. |  |
| Day 16 | 9/19/2026 | Selecting a template places its starting structure on the canvas. Visually rough is fine. Sean's Mermaid spike is answered: routing is modifiable, or it is not. |  |
| Day 17 | 9/20/2026 | Diagram-type selection appears in the AI generation flow and the chosen type is visible to the user before or alongside the output. |  |
| Day 18 | 9/21/2026 | Templates and type routing work end-to-end for the primary use case, including the P0 edge cases: ignore and draw freely, dismiss the picker, low-confidence defaults to flowchart, override and regenerate. |  |
| Day 19 | 9/22/2026 | Correct-type rate is measured across the 50-prompt set against the pre-build baseline. Erasmo's eval card and regression pass are complete and P0 defects are filed. |  |
| Day 20 | 9/23/2026 | P0 defects are fixed, regression re-runs clean, and the prototype is demo-ready for the client. |  |

**Note:** Days 15–18 have passed. Mark actual status before circulating.

# **2\. Risks & Dependencies**

* **Risk — Mermaid routing may not be ours to modify.** Sean's one-day spike decides it. If negative, Day 17's milestone narrows to static templates on the canvas with the AI untouched. Templates still ship; the routing half does not.

* **Risk — no baseline data exists.** Instrumentation is parked by client direction, so we cannot measure whether any of this moved activation. The 50-prompt correct-type rate is the only number we can actually produce.

* **Risk — public repository review.** Changes to the free app sit in a repo with an active contributor community. Maintainer review runs on their timeline, not ours.

* **Dependency — final template set.** Need client confirmation on which 3–5 templates before Day 17\. Flowchart, process flow, org chart and mind map is our working assumption.

* **Dependency — numbered acceptance criteria in the PRD.** Mercator parses AC IDs to build the coverage map. Without them Erasmo is testing against memory rather than requirements.

* **Dependency — fork versus sandbox.** Undecided, and it changes both the merge path and the scope of Erasmo's review.

* **Dependency — team capacity.** Sean owns the spike and the routing build; both Day 16 and Day 17 milestones rest on his availability.

# **3\. What We're Cutting First If We Run Out of Time**

Decided now, in order, so it is not a decision made under pressure on Day 19\.

* **1\. AC-1.1.7 \[P2\]** — template suggestions by recency or popularity.

* **2\. AC-1.2.7 \[P2\]** — regenerate for an alternative version of the same type.

* **3\. AC-1.1.6 \[P1\]** — template preview before selecting.

* **4\. AC-1.2.6 \[P1\]** — type-appropriate styling for generated output.

* **5\. AC-1.3.3 \[P1\]** — download as an editable .excalidraw file or image.

* **6\. AC-1.4.1 to AC-1.4.8** — the entire prompt-history sub-journey. Secondary by client direction, no dependency on anything else, lifts out cleanly.

* **7\. Routing scope** — narrow from four diagram types to two.

**Never cut:** the security and privacy work. Retention and deletion for any stored prompt content is decided before a schema is written. It is invisible in a demo, which is exactly why a compressed schedule reaches for it first — and cutting it is how a data problem ships permanently attached to a feature.
