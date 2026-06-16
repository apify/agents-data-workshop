# Lesson 2: What to do with your data

**Goal:** Learn what happens to your data after an Actor runs, and how you can export it, fetch it via API, or chain Actors together so one scraper feeds into another.

**Time:** ~15 minutes

---

## 1. Recap: Where your data lives

In Lesson 1 you ran the YouTube Scraper and saw results in the **Dataset** tab. Every Actor run produces a dataset. You can view, export, and interact with it from the Apify Console.

## 2. Export it

You can download data in two formats:

1. Open [console.apify.com](https://console.apify.com) -> **Actors** -> **My Actors** (or **Last runs**)
2. Find your YouTube Scraper run from Lesson 1
3. Open the **Dataset** tab
4. Click **Export** and choose **JSON** or **CSV**

JSON preserves nested data and works in code. CSV opens in any spreadsheet app.

## 3. Access it via API

Every dataset has a unique API endpoint. You can fetch it from any script, app, or automation tool.

1. In the Dataset tab, click **API**
2. Copy the "Get dataset items" endpoint (it looks like `https://api.apify.com/v2/datasets/...`)
3. Click the "Test endpoint" button and a new tab will open.

Note: a live API token will be included in the URL. You can create and select one with limited permissions.

## 4. Chain Actors together

The real power of the platform is chaining: one Actor finishes and automatically triggers another.

Apify has a built-in **Actor-to-Actor integration** that handles this. Instead of writing a webhook by hand, you use a UI that connects the output of one Actor to the input of another.

**Example:** scrape YouTube video URLs with the YouTube Scraper, then send each URL to the Website Content Crawler to get the full page text.

1. Go to [console.apify.com](https://console.apify.com) -> **Actors** -> find the `streamers/youtube-scraper` Actor.
2. Click the **Integrations** tab.
3. Search for **Website Content Crawler** in the catalog and select it
4. Set **Start when** to **Run succeeded**
5. The input fields will appear. Integration-ready Actors (like the Website Content Crawler) handle data passing automatically -- they know to fetch the dataset from the triggering run. Just review and save.
6. Click **Add integration**

Now every time the YouTube Scraper finishes, the Website Content Crawler automatically runs against the video URLs it found. You get enriched data without writing any code between the two steps.

> **Tip:** You can chain any two Actors this way. The Integrations tab lists compatible targets for each Actor. This is how you build multi-step pipelines.

## 5. What just happened

You now know three ways to use data from an Actor: download it as a file, fetch it over HTTP as JSON, or chain it into another Actor. Chaining is the most powerful -- it lets you compose multiple scrapers without writing code between them.

## 6. Checkpoint

- [ ] Exported data as JSON or CSV from the console
- [ ] Accessed the dataset via its API URL
- [ ] Understand how webhook chaining works
- [ ] Know when to use export vs API vs chaining

When ready, open [lesson-3-mcp.md](./lesson-3-mcp.md).
