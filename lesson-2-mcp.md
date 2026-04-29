# Lesson 2: Connect Your Agent with MCP

**Goal:** Understand what MCP is and configure your AI coding tool to use Apify's MCP server.

**Time:** ~15 minutes

---

## 1. What is MCP?

The Model Context Protocol (MCP) is a standard that lets AI agents discover and use external tools. Think of it like function calling, but standardized — any MCP-compatible client can connect to any MCP server.

Apify runs an MCP server that exposes scraping Actors as tools your agent can call. Your agent can search Google, scrape Instagram, pull Hacker News data, and more — all by calling tools through MCP.

## 2. Configure your MCP client

Follow the instructions at:

**[mcp.apify.com](https://mcp.apify.com)**

That page walks you through setup for your specific tool (Claude Code, Cursor, Codex, and others). It provides the exact configuration block you need.

### Enable essential tools

On the [mcp.apify.com](https://mcp.apify.com) page, make sure the following are enabled before copying your config:

1. **Preloaded Actors:** Click "Add Actors" and ensure **RAG Web Browser** and **Google Maps Scraper** are in your list.
2. **Custom tools:** Enable 'Actor discovery' tools which allows your agent to search the Apify Store for other tools.

> **Tip:** If you aren't logged in on the page, you can find your API token in the Apify Console under [Settings → Integrations](https://console.apify.com/settings/integrations).

## 3. Verify the connection

Restart your coding tool after configuring MCP, then ask your agent:

> What Apify tools are available to me?

It should list multiple scraping tools. If it doesn't, double-check the configuration from [mcp.apify.com](https://mcp.apify.com) and confirm your API token is correct.

## 4. Run your first MCP query

Ask your agent:

> Search Google for "best developer conferences netherlands 2026" and show me the top 5 results

Your agent should call the Apify Google Search tool through MCP and return live results.

## 5. Add any Actor to your agent

With **Actor discovery** and **Actor runs** enabled, your agent can now use any of the 2,000+ Actors in the Apify Store on demand.

Try asking your agent to use the preloaded Google Maps tool:

> Find 3 coffee shops in Prague using Google Maps. Show me their names and ratings.

### How it works behind the scenes

Because you added **Google Maps Scraper** as a preloaded Actor, the agent sees it as a direct tool. If you _hadn't_ preloaded it (but had **Actor discovery** enabled), the agent would take these extra steps:

1. **Search:** Call `apify.store.search` to find a matching Actor in the Apify Store.
2. **Select:** Inspect the Actor details and select the best one.
3. **Run:** Call `apify.actor.run` to execute that Actor on the platform.
4. **Deliver:** Return the structured data to you.

## 6. Experimental: On-the-fly Tool Creation

Some modern MCP clients support **dynamic tool discovery**. This means the agent can find a tool it doesn't have yet, "install" it, and use it immediately without you restarting anything.

1. Check **[modelcontextprotocol.io/clients](https://modelcontextprotocol.io/clients)** and filter for **"discovery"**.
2. If your client supports discovery (like Claude Desktop or Claude Code), try enabling the **Experimental features** → **Add Actor** on the [mcp.apify.com](https://mcp.apify.com) page.
3. Update your config and try this prompt:

> "I need to check the prices of some products on Amazon. Find an Amazon scraper Actor, add it as a tool, and get the price for 'PlayStation 5'."

If supported, you'll see the agent call `apify.store.search`, then `apify.actor.get`, and finally "register" a new tool specifically for Amazon before running it.

## 7. Checkpoint

- [ ] MCP server configured with Actor discovery and runs enabled
- [ ] Agent sees Apify tools when asked
- [ ] Google Search returned live data
- [ ] Google Maps scraper found and ran through a natural language request

When ready, open [lesson-3-apify-cli.md](./lesson-3-apify-cli.md).
