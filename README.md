# Teach your agents to scrape real-time data

A hands-on workshop. Connect your AI agent to live web data using the Model Context Protocol (MCP) and Apify Agent Skills, then build your own scraper when nothing off-the-shelf fits.

**Author:** Kevin Lewis ([@phazonoverload](https://github.com/phazonoverload)), Apify

## Why this workshop exists

AI agents can write code and reason, but they can't access the live web on their own. This workshop teaches you how to bridge that gap using MCP and Apify's platform. By the end, your agent will be able to scrape websites, pull real-time data, and build custom scrapers on command.

## Who this is for

This workshop works for non-coders and developers alike.

- **Non-coders** can run Actors, export data, chain them together, and connect them to an AI assistant -- no terminal needed.
- **Developers** can do all of that plus install CLI tools and Agent Skills to build and publish custom Actors.

No prior experience with web scraping, MCP, or Apify is required.

## Prerequisites

**Everyone:**

- An Apify account (free, you'll create it in Lesson 1)

**For lessons 4-6 (developer track):**

- An AI coding tool installed: Claude Code, Cursor, Codex, or similar
- Node.js (v18+), download at [nodejs.org](https://nodejs.org)

> **Note for self-hosted workshops:** If you're running this at your own event, you may want to provide promo codes for free Apify credits. Contact Apify for event-specific codes, and have instructors available to help people who get stuck.

## Session structure

This works as a self-paced station or as an instructor-led session.

1. **Opening talk** (~15 min) -- introduces Apify, MCP, and Agent Skills
2. **Self-paced lessons** (~70 min) -- work through the lessons at your own speed
3. **Wrap-up** (~5 min) -- recap and next steps

Everyone starts at lesson 1. If you don't write code, lessons 1-3 are for you. If you build software, continue through lesson 6.

## Lessons

| # | Lesson | Time | 
| --- | --- | --- |
| 1 | [Run Your First Actor](./lesson-1-first-actor.md) | 10 min |
| 2 | [What to Do With Your Data](./lesson-2-what-to-do-with-your-data.md) | 15 min |
| 3 | [Connect Your Agent with MCP](./lesson-3-mcp.md) | 15 min |
| 4 | [Install and Use the Apify CLI](./lesson-4-apify-cli.md) | 10 min |
| 5 | [Install Agent Skills](./lesson-5-agent-skills.md) | 10 min |
| 6 | [Build and Publish Your Own Actor](./lesson-6-build-your-own.md) | 20 min |

### Not sure what to do?

- **Everyone:** start at lesson 1 and go in order.
- **Non-coder:** you can stop after lesson 3. Browse [recipes.md](./recipes.md) for ready-to-use prompts that work with your connected assistant.
- **Developer:** complete all six lessons. The [recipes](./recipes.md) are useful at any point for inspiration.

## Stuck?

If you're at an event, raise your hand or flag down an instructor.

If you're working through this on your own, open an issue on this repo and we'll help.

## After the workshop

The [Apify Store](https://apify.com/store) has thousands of ready-made Actors you can call through MCP or the CLI. A few highlights:

| Platform | What you can get |
| --- | --- |
| Google Maps | Business listings, reviews, contact info |
| Booking.com | Hotel prices, availability, ratings |
| YouTube | Video metadata, comments, channel info |
| LinkedIn | Company and job data |
| Amazon | Product details, reviews, prices |

## Further reading

- [Model Context Protocol Documentation](https://modelcontextprotocol.io)
- [Apify MCP Server](https://mcp.apify.com)
- [Apify Documentation](https://docs.apify.com)
- [Agent Skills Repository](https://github.com/apify/agent-skills)

## License

MIT, see [LICENSE](./LICENSE) for details.
