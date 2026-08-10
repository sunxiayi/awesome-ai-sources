# Awesome AI Sources

Your all-in-one AI signal radar.

[Visit Agentic Brew](https://www.agenticbrew.ai) | [Browse the full source directory](SOURCES.md)

## 1. What This Is

This repository publishes the sources behind [Agentic Brew](https://www.agenticbrew.ai): high-signal places to follow if you care about AI, frontier labs, agents, infrastructure, research, startups, and builder workflows. See [SOURCES.md](SOURCES.md) for the full source directory.

The list is free to browse and use. [Agentic Brew](https://www.agenticbrew.ai) is the product built on top of it, with context, visuals, community signals, and historical background added to the important AI stories.

Current inventory:
- 821 public sources
- 106 company & lab sources
- 90 individual blogs
- 124 AI news & analysis sites
- 2 research feeds & paper trackers
- 499 social accounts and communities

This repository is updated weekly.

## 2. Source Directory

The directory is split by source type so it is easy to scan:

- Company & lab sources: official publications from AI companies, labs, platforms, and research groups
- Individual blogs: independent writers, technical newsletters, and practitioner publications
- AI news & analysis sites: media outlets, newsletters, and aggregators covering AI
- Research feeds & paper trackers: research aggregators and paper-discovery feeds
- Social accounts to follow: selected X accounts, YouTube channels, and Reddit communities

See the full live-generated list here: [SOURCES.md](SOURCES.md).

## 3. Why Agentic Brew

![Agentic Brew homepage](assets/agenticbrew-homepage.png)

Following good sources is necessary, but it is not enough. AI moves across Product Hunt, GitHub, Reddit, X, YouTube, newsletters, tech blogs, AlphaXiv, Hugging Face, Luma, company blogs, research feeds, event pages etc... Agentic Brew helps you keep up without jumping between all of them.

What the product adds:

- From 200+ sources, Agentic Brew identifies high-attention AI topics and explains why they matter, not just what happened.
- AI news, blogs, research, launches, community reactions, videos, and events are brought together in one website.
- The source directory keeps improving. New candidates are discovered as the site runs, then reviewed by a human each week before they are added here.

The goal is to avoid missing high-quality sources while keeping the reading experience focused.

## 4. How It Works

The workflow is simple:

```mermaid
flowchart LR
    A[Scrape] --> B[Filter]
    B --> C[Cluster]
    C --> D[Deep research]
    D --> E[Curate new sources]
```

If you want the raw source list, start with [SOURCES.md](SOURCES.md). If you want the product built from it, use [Agentic Brew](https://www.agenticbrew.ai).

## 5. Keep This Directory Fresh

This directory is refreshed weekly as the source map evolves.

If you use it as a starting point, check back occasionally for newly added sources and better organization.

## 6. Use From Any AI Agent

Agentic Brew exposes the curated source content as public RSS feeds, so any AI coding agent (Claude Code, OpenClaw, Hermes, custom agents, etc.) can pull from it without scraping or auth.

### The feeds

Eleven public endpoints under `https://www.agenticbrew.ai/feed/<feed>.xml`:

| Feed           | Contents | Item link points to |
|----------------|----------|---------------------|
| `news`         | Synthesized news clusters with overviews | Agentic Brew news-analysis card |
| `twitter`      | Trending X topics with the hottest tweets and engagement stats | Top tweet on x.com |
| `github`       | Trending GitHub AI repos with stars / language / daily delta | Original GitHub repo |
| `reddit`       | Trending Reddit AI threads with subreddit, upvotes, comments, excerpt | Original Reddit thread |
| `youtube`      | Curated AI videos with summaries | Original YouTube video |
| `product_hunt` | Trending AI launches with topics and taglines | Original Product Hunt launch |
| `skill`        | Top skills from skills.sh and clawhub | Original skill page |
| `blog`         | Curated AI blog articles with AI-generated summaries | Original blog article |
| `paper`        | Research papers with AI summary, institutions, source, votes | Original paper (arxiv / HF / x.com) |
| `event`        | Upcoming AI events with start time and summaries | Original event page (e.g., lu.ma) |
| `all`          | Union of all of the above | Per-item — same as the feed above |

### For your AI agent (one-line Claude Code plugin)

Install the `ai-news-radar` plugin in any Claude Code session:

```bash
claude plugin install github:sunxiayi/awesome-ai-sources/plugins/ai-news-radar
```

Then trigger the slash command:

```
/ai-news-radar [feed] [--limit N] [--query KEYWORD] [--json]
```

Examples:

```
/ai-news-radar news
/ai-news-radar paper --limit 5
/ai-news-radar twitter --query "openai"
/ai-news-radar all --json
```

When the user invokes the skill vaguely (e.g., "give me today's AI digest"), the agent asks three questions first — which categories, how often, how much detail per item — and shapes the output accordingly.

### In any RSS reader or scraper (raw feeds)

Every feed is a standard RSS 2.0 XML endpoint. No auth, no rate limit on the caller side. Works with any RSS reader, scraper, or AI ingest pipeline. For example:

```bash
curl -s https://www.agenticbrew.ai/feed/news.xml
```

Auto-discovery `<link rel="alternate" type="application/rss+xml">` tags for all eleven feeds are exposed in every page's `<head>` on [agenticbrew.ai](https://www.agenticbrew.ai). LLM-friendly summary at [agenticbrew.ai/llms.txt](https://www.agenticbrew.ai/llms.txt).

### Other agent frameworks (reuse the skill definition)

The plugin's skill definition (a single markdown file with frontmatter and a small bash + Python parsing snippet) lives at [`plugins/ai-news-radar/skills/ai-news-radar/SKILL.md`](plugins/ai-news-radar/skills/ai-news-radar/SKILL.md). If your agent framework supports skill / instruction files (OpenClaw, Hermes, custom harnesses, etc.), point it at that file or copy the snippet into your own tool format. The skill is self-contained — no external dependencies beyond Python's stdlib.

## 7. Use The Product

Visit [agenticbrew.ai](https://www.agenticbrew.ai) to use Agentic Brew.

Browse [SOURCES.md](SOURCES.md) when you want the source directory itself.
