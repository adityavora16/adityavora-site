# 2026 Aditya Vora Shorts Report: method note

File: `aditya-vora-shorts-report-2026.csv` (869 rows, one per YouTube Short).
Published with: https://www.adityavora.in/short-form-video-statistics#shorts-study
Captured: 10 November 2026. Author: Aditya Vora.

## Sample

- 869 YouTube Shorts from 45 Indian YouTube channels in 7 niches: auto (6 channels),
  comedy (5), education (8), finance (6), fitness (5), food (7), tech (8).
- Channels are large, established creator and publisher channels (about 0.4 million to 35 million
  subscribers at capture), picked by hand as well-known names in each niche. This is not a random
  sample of all Indian Shorts.
- For each channel: its most recent Shorts (up to 20) published between 13 July and 27 October
  2026, that is, 14 to 120 days before capture.
- Together the 869 Shorts had 270 million views at capture.

## What was collected

Public data only, read from YouTube with yt-dlp, with no login, no API key and no channel
analytics. Per Short: video id, channel, subscriber count, publish date, duration in seconds, views,
likes and comments at capture, and the title.

## What was excluded

- 100 channel handles were tried. 55 were dropped:
  - 21 had a wrong handle or no Shorts tab.
  - 12 had fewer than 12 Shorts listed.
  - 20 had fewer than 12 Shorts in the date window.
  - 2 were not collected after YouTube rate-limited the crawl.
- Shorts under 14 days old at capture, because they were still collecting views.
- All of Ankur Warikoo's channels and Do Epic AI, because the author works with them.
- One channel, Food Fusion, was removed because it is not Indian.

## How the numbers are calculated

- **Length buckets:** under 15 s, 15 to 29 s, 30 to 44 s, 45 to 59 s, 60 to 89 s, 90 s and over.
  The longest Short in the sample is 180 s.
- **Compared with the channel's usual Short:** each Short's views divided by the median views of
  that channel's Shorts in the sample (`views_vs_channel_median`). A bucket's figure is the median
  of those ratios minus one, so 0% means "what this channel normally gets". This removes channel
  size, which otherwise dominates any comparison of raw views.
- **Median views** (raw) are given too, but mostly reflect which channels sit in each bucket.
- **Niche medians** are raw median views per Short, so they mostly reflect the size of the channels
  sampled in that niche.
- **Hook type:** each Short's public title (or, when the title was only hashtags or a series label,
  the first line of its description) was classified into one of eight types: Stat/Number,
  Contrarian Claim, News-jack, Curiosity Gap / Question, Story/Case, Relatable POV,
  Listicle/Breakdown, Label only. The classification is human-style judgement made with an AI
  model reading each title, not a keyword rule. On-screen text was not read.

## Checks

- **Post age:** Shorts aged 14 to 45 days (643), 45 to 75 days (146) and 75 to 120 days (80)
  scored 0%, minus 3% and plus 2% against their channel's usual Short. No strong age effect.
- **Hits:** every bucket was re-run with the top 5% of Shorts removed. The 30 to 44 second bucket
  stays lowest (minus 23%). The Story/Case hook drops from plus 18% to plus 4%, so it wins on a few
  hits. The Relatable POV hook is mostly comedy channels (50 of 78) and is minus 4% without them.
- **Thin buckets:** Stat/Number titles (31 Shorts) and Shorts under 15 seconds (33 Shorts) are small
  and should be read as early signals.

## Limits

- View counts are a single snapshot on 10 November 2026. Since 31 March 2025 YouTube counts a
  Shorts view on every start or replay.
- These are comparisons, not causes. A length or hook type that scored above a channel's usual
  Short did so on these channels at capture.
- Titles in the CSV are reproduced exactly as published, in Hindi, Hinglish and English.

## Cite

Aditya Vora, "2026 Aditya Vora Shorts Report", adityavora.in, 10 November 2026.
https://www.adityavora.in/short-form-video-statistics#shorts-study
