# Lesson 4: Install Agent Skills

**Goal:** Understand what Agent Skills are and install the two Apify skills into your coding tool.

**Time:** ~10 minutes

---

## 1. What are Agent Skills?

Agent Skills are structured instructions that teach your AI coding agent domain-specific knowledge about a platform or workflow. They tell the agent which tools to use, which patterns to follow, and which best practices to apply.

When you install an Apify Agent Skill, your coding agent learns how to use the Apify CLI, which Actors to call for different scraping tasks, and how to build and deploy new Actors from scratch.

Apify ships two skills:

| Skill                                       | What it teaches your agent                                                                                                         |
| ------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Ultimate Scraper** (a.k.a. Apify Central) | How to scrape any major platform using existing Apify Actors — Google, Instagram, Hacker News, Amazon, and dozens more             |
| **Actor Development**                       | How to build, test, and deploy new Apify Actors from a single prompt — project scaffolding, scraper logic, schemas, and deployment |

## 2. Install both skills

Run these commands in your terminal:

```bash
npx skills add apify/agent-skills/apify-ultimate-scraper
```

```bash
npx skills add apify/agent-skills/apify-actor-development
```

Confirm both are installed — ask your agent:

> What Apify Agent Skills are available to me?

## 3. How the skills work

When you ask your agent to scrape something, the Ultimate Scraper skill tells it:

- Which Apify Actor handles that platform
- How to structure the input
- Which CLI command to run

When you ask your agent to build an Actor, the Actor Development skill tells it:

- How to scaffold the project
- Which files to create (input schema, output schema, scraper logic, metadata)
- How to test locally
- How to deploy with `apify push`

Your agent already knows how to write code. These skills give it the Apify-specific knowledge to turn code into deployed, running Actors.

## 4. MCP vs. Agent Skills: Which one to use?

You now have two ways to connect your agent to Apify. Here is the distinction:

- **MCP:** Best for "chat and research." Use it when you want the agent to quickly grab some data from the web and bring it into your current conversation.
- **Agent Skills:** Best for "coding and building." Use these when you want the agent to use the Apify CLI, automate complex data pipelines, or build and deploy new Actors (which you'll do in the next lesson).

## 5. Practical Exercise: Research and Compare

Let's test the **Ultimate Scraper** skill. Ask your agent to research something complex that requires multiple sources:

> "I want to research the topic of 'The future of AI agents'. Find 3 relevant videos on YouTube and 2 recent articles found via Google Search. Summarize the different perspectives."

The agent should use its new knowledge to decide which tools are best, structure the inputs correctly, and call them via the CLI or MCP (the skills help it decide which is most efficient).

## 6. Checkpoint

- [ ] Both skills installed and confirmed by the agent
- [ ] Successfully performed a multi-source research task using the new skills

When ready, open [lesson-5-build-your-own.md](./lesson-5-build-your-own.md).
