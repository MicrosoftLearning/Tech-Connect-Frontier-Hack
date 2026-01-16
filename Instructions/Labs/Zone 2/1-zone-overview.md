# 🟡 Zone 2: Build a Reasoning & Routing Agent (Copilot Studio)

## Overview

In Zone 2, you will build a **reasoning-driven agent** in Copilot Studio that can analyze user intent and dynamically route conversations to the appropriate topic flow.

You will continue using the **same CRM_Synthetic_Data.xlsx dataset from Zone 1**; no new data sources are introduced in this zone.

Unlike Zone 1, which focused on retrieval and grounding, this zone introduces:

- Intent classification  
- Topic-based routing  
- Multi-turn conversation design  
- Data-grounded generative responses  

The step-by-step guidance in this zone intentionally focuses on **customer opportunities** as a representative example.  
The patterns you build here can be extended to other entities in the dataset—or applied to real-world data—without changing the core architecture.

## What Success Looks Like

By the end of this zone, you will have:

- An agent built in Copilot Studio  
- A central topic that analyzes user intent  
- Routing logic that directs users to different response paths  
- Topics that generate structured, data-grounded responses  
- A working agent you can extend beyond the scripted scenario  

This zone is about **reasoning and orchestration**, not automation or action-taking.

## How to Approach This Zone

You can complete Zone 2 in **one of two ways**. Both lead to the same functional outcome.

### 🧭 Option A: Guided Build

> [+Note] Follow a step-by-step path to build a baseline agent.
>
> This option is recommended if you are new to Copilot Studio topic design or want explicit guidance through configuration.
>
> You will:
>
> - Create a base agent
> - Add an intent analysis topic
> - Configure routing logic
> - Attach structured, data-grounded generative responses
>
> ➡️ Start with **Create a New Agent in Copilot Studio**, then proceed through each task in order.

### 🧠 Option B: Build It on Your Own

> [+Note] Design and build the agent independently or with your group.
>
> This option is intended for participants already comfortable working in Copilot Studio.
>
> The guided steps demonstrate **one representative implementation** using opportunity data in the provided dataset, but you are not limited to those guardrails.
>
> **Your objective** is to design an agent that:
>
> - Analyzes user intent  
> - Routes conversations dynamically  
> - Produces data-grounded responses using the CRM dataset  
>
> You may reference the guided steps at any time.
>
>**Design checkpoints (use these to self-validate)**
>
> As you build, pause and confirm:
>
> - Do you have a **single, central routing topic**?
> - Can the agent correctly handle **at least two distinct user intents**?
> - Does each conversation path end cleanly?
> - Can the agent clearly explain **what it does *not* know**?
>
> If you can’t confidently answer “yes” to these, refine your design before moving on.
>
> **Stretch (optional)**
>
> If time allows, consider:
>
> - Adding a third intent (for example, clarification or comparison)
> - Improving response structure for readability
> - Preparing your agent to support a future action (even if you don’t implement it yet)
>
> These extensions will make the Zone 2 Challenge easier.
>
> Once you feel confident in your design, proceed to **Challenge: Go Beyond the Script**.

## What You Should End Up With

At a minimum, your agent should include:

- A central topic that analyzes user intent  
- Routing logic that directs users to different response paths (child topics)  
- At least two response styles (for example, summary vs. details)  
- Generative answers grounded strictly in the dataset  
- A clean conversational endpoint  

The guided path uses opportunities as the example entity, but the same patterns apply to other records in the dataset.

## Conceptual Flow

The diagram below shows the intended shape of the solution, not the exact implementation.

```mathematica
User Message
     |
     v
Intent Analysis Topic
     |
     |-- approach = "summary"
     |         |
     |         v
     |   Summarize Opportunity Topic
     |         |
     |   Generative Answer (CRM-grounded)
     |
     |-- approach = "details"
     |         |
     |         v
     |   Review Opportunity Details Topic
     |         |
     |   Structured Field Output
     |
     |-- approach = "unclear"
               |
               v
        Clarification Message
```

This pattern is intentionally simple — and intentionally extensible.

## Group Work Expectations

Regardless of which path you choose:

- Work **with your group** as you test  
- Compare routing decisions and assumptions  
- Differences often reveal gaps in prompts or logic  

These insights will be useful during the Zone 2 Challenge.

## Where to Start

➡️ **Guided path:** Begin with **Create a New Agent in Copilot Studio**  
➡️ **On-your-own path:** Use the guidance above to build your agent, then move directly to **Challenge: Go Beyond the Script**
