# Lesson 5: Build and publish your own actor

**Goal:** Use the Actor Development skill to build a Hacker News hiring scraper and deploy it to the Apify platform — from a single prompt.

**Time:** ~20 minutes

---

## 1. The prompt

Copy this entire prompt and paste it into your AI agent:

```
Build an Apify Actor that scrapes the latest Hacker News Hiring thread.

The hiring threads are posted monthly at https://news.ycombinator.com/submitted?id=whoishiring
by the user "whoishiring." The latest post will have a title starting with "Ask HN: Who is hiring?"

Input schema:
- keywords (string array) — filter posts that contain any of these keywords (case-insensitive)
- remoteOnly (boolean) — when true, only include posts that mention "remote" in the body

Output schema: each dataset entry should have:
- company (string) — the name of the company hiring
- role (string) — the job title or role
- location (string) — where the job is based (e.g., "NYC", "Remote", "London")
- body (string) — the full post body
- link (string) — the permalink to the individual comment
- matchedKeywords (string array) — which keywords were found in the post
- isRemote (boolean) — whether the post mentions remote work

The Actor should:
1. Find the latest hiring thread URL on the submissions page
2. Scrape all top-level comments as individual posts
3. Filter by keywords and remote preference
4. Push matching posts to the dataset
```

## 2. Watch your agent work

Your agent (guided by the Actor Development skill) will:

- Scaffold an Apify Actor project
- Implement the scraper logic (uses Cheerio by default)
- Set up the input schema, output schema, and dataset schema
- Create Actor metadata
- Test the Actor locally

If the agent hits an issue, it'll iterate until it's fixed. Let it work — this is the Actor Development skill doing its job.

> **Running short on time?** Skip to step 3 and push the project as-is — you can always re-run and fix it from the Apify Console later. The important thing is getting a deployment up.

## 3. Deploy to Apify

Once the agent finishes, `cd` into the project directory and push:

```bash
apify push
```

Your Actor is now live on the Apify platform.

> **If `apify push` fails:** Make sure you ran `apify login` in Lesson 3 and that you're inside the project directory the agent created.

## 4. See your results

1. Open [console.apify.com](https://console.apify.com) → **Actors** → find your new Actor
2. Click **Run** and provide input:

   ```json
   {
   	"keywords": ["python", "typescript", "rust"],
   	"remoteOnly": false
   }
   ```

3. Wait for the run to complete, then open the **Dataset** tab

You should see structured job postings matching your filters.

## 5. Export your data

From the Dataset tab:

- **Download as JSON** — for programmatic use
- **Download as CSV** — for spreadsheets
- **API access** — copy the API endpoint to fetch this data from your own apps

The Actor Development skill also generated a Store-ready README and metadata. If you want to publish it on the Apify Store for others to use, add a price and hit Publish.

## 6. Checkpoint

- [ ] Agent built the Actor project from the prompt
- [ ] `apify push` deployed successfully
- [ ] Actor ran and returned filtered HN hiring posts
- [ ] Data exported as JSON or CSV
