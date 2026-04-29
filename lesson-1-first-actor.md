# Lesson 1: Run Your First Actor

**Goal:** Create an Apify account, apply your promo code, and run an existing Actor to see what the platform can do. No terminal required.

**Time:** ~10 minutes

---

## 1. Create an Apify account

Go to [console.apify.com/sign-up](https://console.apify.com/sign-up) and create a free account. Sign in.

## 2. Apply the promo code

The instructor will give you a promo code in the room. This gives you free platform credits for today's workshop.

1. In Apify Console, click your avatar (top-right) → **Settings** → **Usage & Billing**
2. Enter the promo code and click **Apply**

You now have credits to run Actors.

## 3. Run the YouTube Scraper

**What is an Actor?**
An "Actor" is a serverless cloud program. It's the building block of the Apify platform. Each Actor is a mini-app designed for a specific task—like scraping a website, automating a browser, or processing data. They run in the cloud, so you don't have to worry about servers, proxies, or staying online.

Let's pull real data right now — no code, no terminal.

1. Go to [console.apify.com/store](https://console.apify.com/store) and search for **YouTube Scraper**
2. Click **Try for free**
3. In the input form, enter a search query you're curious about (e.g. `AI agents 2025`)
4. Set **Max results** to `10` to keep it fast
5. Click **Start**

The Actor runs in the cloud. You'll see it progress through the scrape.

## 4. See your results

When the run finishes:

1. Open the **Dataset** tab — you'll see structured data: video titles, view counts, upload dates, descriptions, and channel names
2. Click **Export** to download as JSON or CSV

That's it. You just scraped live data from YouTube without writing a line of code. Every Actor in the Apify Store works the same way — provide input, get structured data back.

## 5. Checkpoint

- [ ] Apify account created and promo code applied
- [ ] YouTube Scraper ran and returned live data

When ready, open [lesson-2-mcp.md](./lesson-2-mcp.md).
