# Visit Karma — new homepage

A drop-in homepage for visitkarma.com, inspired by the
[Visit Karma YouTube channel](https://www.youtube.com/@visitkarma)
(one-line family-travel tagline, playlist-style collections, minimal chrome).

## Install

Copy `layouts/index.html` into your Hugo site so it lands at:

```
<your-site>/layouts/index.html
```

Hugo prefers site-level `layouts/` over the theme's, so this overrides the
theme homepage with no theme edits. Rebuild / redeploy as usual.

## What it renders

- **Header** — brand, anchor nav, About link, red YouTube button (@visitkarma)
- **Hero** — "Family luxury travel, honestly reviewed.", your channel tagline,
  live stats (trip guides, destinations & topics, 300+ videos)
- **Latest trip** — your most recent post as a large feature card
- **Collections** — playlist-style lanes driven by categories/tags you already use:
  Hotel & Resort Reviews, Itineraries, Travel Tips & Money Savers, Skiing & Winter,
  Flight Reviews. A collection only appears once it has matching posts, so new
  lanes (e.g. Flight Reviews) appear automatically as you publish.
- **Destinations** — region cards (Caribbean, Europe, Asia, North America,
  South America) with country chips linking to that country's tag page.
  Regions with no posts are hidden automatically.
- **Latest posts** — the newest 8 after the featured one
- **YouTube banner** — subscribe CTA, since every guide starts as a video

## Keeping it fed as you add posts

- **Country tags**: keep tagging posts with the country
  (`Antigua`, `Japan`, …). To file a country under a region, add its tag slug
  to the matching list in `$regions` at the top of `index.html`
  (e.g. add `"iceland"` under Europe).
- **Collections**: posts land in a collection via their `categories`/`tags`
  (matched after `urlize`, so `Hotel Review` matches `hotel-review`).
  To add a new collection, copy one `dict(...)` line in `$collections`
  and point `more` at the matching taxonomy page.
- **Video count** in the hero stats is hardcoded (`300+`) — bump it when
  the channel grows.

## Tested

Rendered with Hugo v0.152.2 against 8 sample posts replicating your real
front matter (sections `p/` and `post/`, page-bundle images). All sections,
counts, links and cover images verified in the output HTML.
