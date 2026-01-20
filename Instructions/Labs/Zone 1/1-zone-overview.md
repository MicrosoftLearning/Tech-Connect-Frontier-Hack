# 🟢 Zone 1: Build a Retrieval Agent (Copilot Chat)

**Suggested Time:** ~35 minutes

## What You’re Building

In this zone, you'll build a **retrieval-based agent** that helps people explore and understand a **portfolio of business records** (for example, accounts, leads, and opportunities) using a provided sample dataset.

Here, you are intentionally not building something impressive. You are building something trustworthy.

In the real world, teams constantly work with exports, reports, and spreadsheets to understand what’s happening across their business — whether that’s customers, projects, partners, or work in flight.

Your agent should turn that kind of data into something people can explore through natural language, making it easier to spot patterns, identify gaps, and get oriented without digging through rows and columns.

## What Success Looks Like

By the end of this zone, you'll have:

- A retrieval-based agent that is grounded in the provided sample dataset  
- An agent that can answer realistic portfolio-level questions  
- An agent that clearly calls out missing or unclear data instead of fabricating answers  

## How You Can Approach This Zone

There are two valid ways to complete Zone 1. Choose the one that best fits your experience level, and work with your group as you build and test.

### 🧭 Option A — Guided Build

If you're new to building agents, or want a structured path, continue with the step-by-step instructions that follow under **Create a New Agent in Microsoft 365 Copilott**.

### 🚀 Option B — Build It on Your Own

If you're already comfortable with Copilot agents, you may skip the step-by-step instructions and build your agent directly.

Your agent must still meet the same grounding, testing, and exit criteria before you move on. Be sure to complete the **Testing Your Agent** and **Outcomes & Next Steps** tasks once your agent is built.

No matter which path you take, you'll validate your work using the same testing steps and exit criteria before moving on.

## What You’re Working With

You're provided with a set of **synthetic business datasets** designed to simulate real-world exports.

The primary dataset for this zone is **CRM_Synthetic_Data.xlsx**, which includes multiple related record types (such as accounts, leads, and opportunities) and serves as the **baseline for the guided examples and testing scenarios** throughout the workshop.

Treat this data like a real export: useful, imperfect, and incomplete.

Before building your agent, take a few minutes to open the dataset and skim the contents.

You don’t need to analyze every row — just get a feel for:

- What types of records exist
- How fields relate (or don’t)
- Where data appears missing, inconsistent, or ambiguous

> [!NOTE]
> When opening Excel for the first time, you may be **prompted** to sign in. Use the following credentials:
> - **Username:** +++@lab.CloudPortalCredential(User1).Username+++
> - **Password:** +++@lab.CloudPortalCredential(User1).Password+++
> - **temporary password**, +++@lab.CloudPortalCredential(User1).AccessToken+++

If it’s helpful for your scenario, you may also choose to work with **alternative sample datasets** (for example, engineering activity logs or support case data) instead of—or in addition to—the CRM data.

All sample files can be found on your desktop in the **Lab Docs** folder.

![Screenshot showing same docs folder.](../Media/sampledocs.png)

> [!NOTE]
> For Zone 1, ignore all JSON files in the Sample Docs folder. They are provided for use in later zones.

➡️ Proceed to the next task in Zone 1: **Create a New Agent in Microsoft 365 Copilot**
