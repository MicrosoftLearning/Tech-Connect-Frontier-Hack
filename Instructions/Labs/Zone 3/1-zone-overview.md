# 🟣 Zone 3: Architect an Agent System (Azure AI Foundry)

## What you’re doing in this zone

In this zone, you will **step back from building individual agents** and focus on **designing an agent system** that goes beyond what Copilot Studio alone can reasonably support.

This is an **advanced, open-ended zone** centered on:
- system design
- architectural tradeoffs
- platform decisions
- collaboration between roles

Rather than following a prescriptive lab, you’ll work **with your group** to design, justify, and (optionally) validate an agent-based solution using **Azure AI Foundry**.

This zone is intentionally less structured than Zones 1 and 2. Ambiguity is part of the exercise.

---

## What success looks like

By the end of Zone 3, your group will have:

- A **clear system-level design** for a multi-agent solution  
- A justified explanation of **why Azure AI Foundry is required**  
- A shared artifact that documents:
  - agent roles
  - data flow
  - orchestration decisions
  - human-in-the-loop boundaries
- (Optional) Evidence that parts of the design are **feasible in Foundry**

A working implementation is **not required**.

---

## How this zone fits with the others

- **Zone 1** focused on retrieval and insight  
- **Zone 2** focused on single-agent interaction and actions  
- **Zone 3** focuses on **orchestration, systems, and scale**

Think of this zone as answering:

> *“What happens when this solution grows beyond a single agent?”*

---

## The challenge

### Scenario

Your team has already built solutions similar to Zones 1 and 2 using Copilot Chat and Copilot Studio.

Those solutions work — but they are starting to hit limits.

Leadership now asks:

> **“What would the next generation of this system look like — and why does it require Azure AI Foundry?”**

Your task is to design that next-generation system.

---

## Your task (work as a group)

### Step 1: Define the system goal

Agree on a **single, clear goal** for the system.

Examples:
- portfolio-level decision support
- risk identification and escalation
- preparation for downstream actions or reviews
- coordination across multiple roles

Document:
- who the system serves
- what decisions it supports
- what *good output* looks like

---

### Step 2: Design the agent roles

Design a **multi-agent system**.

For each agent, define:
- agent name
- primary responsibility
- inputs (data, signals, context)
- outputs (insights, actions, handoffs)
- autonomy level:
  - advisory only
  - semi-automated
  - requires human approval

You must include:
- **at least 3 distinct agents**
- **at least one agent-to-agent interaction**
- **at least one human decision point**

Avoid “one agent does everything.”

---

### Step 3: Decide why this requires Azure AI Foundry

This step is required.

As a group, explicitly answer:
- Why is Copilot Studio no longer sufficient?
- What requirements push this into Foundry territory?

Consider:
- custom orchestration or workflows
- multiple cooperating agents
- non-M365 or custom data
- evaluation and observability needs
- governance or deployment flexibility
- developer ownership and extensibility

Be specific. “More control” alone is not enough.

---

### Step 4: Map the architecture (no code)

Create a **high-level architecture view**.

This can be:
- a diagram
- a table
- structured bullet points

Your architecture should show:
- how agents interact
- where data enters the system
- where decisions are made
- where humans stay in the loop

Do **not** worry about SDKs, syntax, or infrastructure details.

---

### Step 5 (Optional): Validate parts of your design in Foundry

If time permits, explore Azure AI Foundry to sanity-check your ideas.

You may:
- create a Foundry project
- explore available models and benchmarks
- experiment with:
  - chat playground
  - prompt flow
  - data + indexes
  - evaluation or guardrails

Your goal is **validation**, not completion.

---

## Required group deliverable

Each group must produce **one shared artifact**:

- an architecture diagram  
- or a structured agent/system design document  
- or a short design brief (1–2 pages)

Every group member should be able to explain the design.

---

## Constraints (intentional)

- ❌ No single-agent solutions  
- ❌ No “the model just knows” assumptions  
- ❌ No full automation of all decisions  
- ✅ At least one escalation to a human  
- ✅ At least one agent collaboration  

Differences between groups are expected — and valuable.

---

## Guidance: Using Azure AI Foundry (optional reference)

You are **not required** to implement anything end to end.

Use Foundry as a **design validation tool**, not a checklist.

Depending on your comfort level, you may choose:

### Option A: Foundry portal (UI-first)
- Create a project
- Explore models and benchmarks
- Use playgrounds to test prompts or grounding
- Review prompt flow and evaluation capabilities

### Option B: VS Code + AI Toolkit
- Explore Foundry project structure
- Review how agents, workflows, and tools are defined
- Inspect (not necessarily write) code artifacts

Choose what helps you reason about feasibility.

---

## Discussion prompts (if you finish early)

- What part of your system would be hardest to build?
- What would you prototype first?
- What risks would you flag to leadership?
- How would this system evolve over time?
- What would you keep in Copilot Studio vs move to Foundry?

---

## Outcomes

If you complete this zone successfully, you should walk away with:

- A clearer mental model for **agent systems**
- Confidence recognizing **when Foundry is required**
- The ability to articulate agent architectures to developers
- A stronger **agent-first, systems-oriented mindset**

This zone is about **thinking ahead**, not shipping today.

➡️ You may complete this zone independently or after Zones 1 and 2.
