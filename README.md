# Teach your agents to scrape real-time data

A 90-minute hands-on workshop. Connect your AI coding agent to live web data using the Model Context Protocol (MCP) and Apify Agent Skills.

**Author:** Kevin Lewis ([@phazonoverload](https://github.com/phazonoverload)), Apify

## Why this workshop exists

AI coding agents can write code, but they can't access the live web. This workshop teaches you how to bridge that gap using MCP (Model Context Protocol) and Apify's platform. By the end, your agent will be able to scrape websites, pull real-time data, and build custom scrapers on command.

## What you'll learn

After completing this workshop, you will be able to:

- Run pre-built web scrapers (Actors) from the Apify Store
- Configure MCP to give your AI agent access to live web data
- Install Agent Skills that teach your coding tool Apify-specific workflows
- Build and deploy your own custom web scraper using natural language prompts

## Target audience

This workshop is designed for **developers** who:

- Already use AI coding tools (Claude Code, Cursor, Codex, etc.)
- Want to give their agents access to live web data
- Have basic command-line familiarity

No prior experience with web scraping, MCP, or Apify is required.

## What you'll build today

- Run your first web scraping Actor and get live data in seconds
- Connect your AI agent to Apify's MCP server so it can pull data from the web on demand
- Install Agent Skills that teach your coding agent how to use Apify tools
- Build and deploy your own web scraping Actor — from a single prompt

## Prerequisites

**Bring your laptop with:**

- An AI coding tool installed: Claude Code, Cursor, Codex, or similar
- Node.js (v18+) — download at [nodejs.org](https://nodejs.org)

No prior experience with MCP or Apify needed.

> **Note for self-hosted workshops:** If you're running this workshop at your own event, you may want to provide promo codes for free Apify credits to attendees. Contact Apify for event-specific codes. Instructors should be available to help participants who get stuck.

## Session structure

1. **Opening talk** (~15 min) — introduces Apify, MCP, and Agent Skills
2. **Self-paced lessons** (~70 min) — work through the lesson files at your own speed
3. **Wrap-up** (~5 min) — recap and next steps

If you're running this workshop yourself, have helpers available to assist participants who get stuck.

## Lessons

| #   | Lesson                                                           | Approx. time |
| --- | ---------------------------------------------------------------- | ------------ |
| 1   | [Run Your First Actor](./lesson-1-first-actor.md)                | 10 min       |
| 2   | [Connect Your Agent with MCP](./lesson-2-mcp.md)                 | 15 min       |
| 3   | [Install and Use the Apify CLI](./lesson-3-apify-cli.md)         | 10 min       |
| 4   | [Install Agent Skills](./lesson-4-agent-skills.md)               | 10 min       |
| 5   | [Build and Publish Your Own Actor](./lesson-5-build-your-own.md) | 20 min       |

## Stuck?

If you're running this workshop at an event, raise your hand or flag down an instructor.

If you're working through this on your own, open an issue on this repo and we'll help.

## After the workshop

The [Apify Store](https://apify.com/store) has thousands of ready-made Actors you can call through MCP or the CLI. A few highlights:

| Platform    | What you can get                         |
| ----------- | ---------------------------------------- |
| Google Maps | Business listings, reviews, contact info |
| Booking.com | Hotel prices, availability, ratings      |
| YouTube     | Video metadata, comments, channel info   |
| LinkedIn    | Company and job data                     |
| Amazon      | Product details, reviews, prices         |

## Further reading

- [Model Context Protocol Documentation](https://modelcontextprotocol.io)
- [Apify MCP Server](https://mcp.apify.com)
- [Apify Documentation](https://docs.apify.com)
- [Agent Skills Repository](https://github.com/apify/agent-skills)

## License

MIT — see [LICENSE](./LICENSE) for details.
