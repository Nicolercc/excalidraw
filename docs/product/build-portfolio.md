# **BUILD PORTFOLIO**

| Feature name | Templates \+ Diagram-Type Routing |
| :---- | :---- |
| **Team** | Natalie Walker, Nicole Rodríguez, Sean Pisano, Erasmo Concepcion — AI Affair |
| **Client** | Jacqueline Reverand, Head of Product — Excalidraw |
| **Date** | September 22, 2026 |

# **1\. What We Built**

A starting-point layer for the Excalidraw canvas. A new user who opens the app now sees a small set of ready-made diagram structures — flowchart, mind map, and a step-by-step process — instead of an empty page. Picking one places that structure on the canvas, ready to edit. The same choice also tells the AI generator which kind of diagram to produce, so a request for a flowchart returns a flowchart.

Before this, a first-time visitor faced a blank canvas with a toolbar and no indication of where to begin. Now they can be looking at a labelled structure within a few seconds, with no account required and nothing standing between them and the drawing.

# **2\. Why We Built It**

At kickoff the client named first-run as the highest-loss stage and asked us to focus on free-tier onboarding through to a first useful drawing. She also confirmed two things that shaped everything after: scope is the free tier at excalidraw.com, and users should experience value before any signup pressure.

Two findings pointed at the same feature.

* **Users had no first move.** The canvas opens empty. Someone who knows what they want to make still doesn't know how to begin here, and the substitutes — draw.io, tldraw — are also free and also require no account, so there is no switching cost holding anyone.

* **The AI returned the wrong diagram type.** We tested it directly: a prompt containing the word “flowchart” returned a UML class diagram, in hand-drawn style, poorly laid out. The renderer was faithful — the wrong grammar was chosen upstream. draw.io has already shipped the fix for this, letting users select a diagram type from a dropdown before generating.

Templates address both at once, and they do it without costing the user any time before they draw — which matters, because the free tier's advantage is not that it costs nothing but that it costs no time. Miro, FigJam and Whimsical are all free at entry too; they just charge ninety seconds and an account first.

**Early signal:** three template types render correctly on the branch with the right structure for each — a flowchart with a decision diamond and Yes/No branches, a mind map with a central node, and a four-step process. Notably, the type selection is made client-side and stays correct even when the AI generator is unreachable, which tells us the routing logic itself is sound.

# **3\. How It Works**

## **Step 1 — Open the canvas**

The user lands directly on a live canvas, as before. No account, no gate, no loading sequence. The template picker sits alongside the existing toolbar rather than in front of it.

## **Step 2 — Pick a starting structure**

Three to five options: flowchart, mind map, process. Selecting one places its structure on the canvas, fully editable. Ignoring every template and drawing freehand still works exactly as it did — nothing is required.

## **Step 3 — Or describe what you want**

The user can type a description and choose the diagram type before generating. If the prompt already names a type — “flowchart,” “mind map” — that term wins over inference. The chosen type is shown to the user, and they can override it and regenerate without rewriting the prompt.

## **Step 4 — When the generator is unavailable**

The system falls back to a static starting structure of the correct type, with a message saying so. This is a working state rather than a failure state: the user still gets a usable diagram, just without generated content.

**Screenshots:** flowchart, mind map and process templates rendering on feat/templates-prototype, September 21\.

# **4\. What's Left**

An honest account of where this stands.

* **AI generation is unverified.** The branch environment has no ANTHROPIC\_API\_KEY set, so no live generation has run. The routing logic works, but we have not yet confirmed end-to-end behaviour against a real generator. This is configuration, not a build defect.

* **No accuracy measurement yet.** We planned a 50-prompt test set scored against a pre-build baseline, targeting 90% correct type selection. That measurement is blocked by the same missing key. It is the single most important number for this feature and we do not have it.

* **Template set is provisional.** Flowchart, process, org chart and mind map is our working assumption. The final set has not been confirmed with the client.

* **Deferred by choice:** template preview before selection, type-appropriate styling for generated output, download as an editable file or image, and template suggestions by recency. All P1 or P2, all cut in a pre-agreed order rather than under pressure.

* **Deferred by client direction:** activation instrumentation. We were asked to assume analytics exist and focus on user-facing work. The consequence is that we cannot measure whether this feature moved activation — nobody could currently identify where the existing activation metrics come from.

* **Also deferred:** AI prompt history and persistence legibility, both acknowledged as valuable at discovery and ranked below templates. Voice-to-text prompt input was raised and remains unscoped.

## **What the next iteration should tackle first**

Set the API key, capture the 50-prompt baseline, and measure correct-type accuracy. Everything else is secondary until that number exists — it is the difference between a mechanism that works and a mechanism that works well enough.

In hindsight we should have captured that baseline on day one, before any build work. It needs no feature, only prompts run against the current system. Placing it at the end tied our only measurement to a dependency that could slip, and it did.

# **5\. Relevant Links**

* Team repo: \[link\] — branch feat/templates-prototype

* Demo recording: \[link\]

* Source of Truth v3.1 — research, competitive analysis, discovery record

* PRD v2.0 — requirements and acceptance criteria map

* Feature Roadmap — milestones, risks, cut order
