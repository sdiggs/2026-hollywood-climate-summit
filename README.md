# Hollywood Climate Summit 2026 · Scripps Delegation Day-of Page

A single-page, day-of logistics site for the Scripps Institution of Oceanography delegation at the [Hollywood Climate Summit](https://www.hollywoodclimatesummit.com/), June 3 and 4, 2026, in Los Angeles. It's the page people pull up on their phones to know where to be, what to bring, who to call, and how to get reimbursed.

**Live:** https://sdiggs.github.io/2026-hollywood-climate-summit/

## What's here

```
.
├── index.html      The entire page and app. Everything lives in this one file.
└── README.md       You're reading it.
```

That's the whole repo. The HTML, the CSS, and the two embedded venue maps are all inside `index.html`. The only external calls are Google Fonts (Fraunces and Manrope) and the Google Maps embeds, both loaded over HTTPS with no API key required.

## The page covers

- Two venue cards: Samuel Goldwyn Theatre (June 3) and The Ebell of Los Angeles (June 4), with addresses and one-tap directions
- Why we're there, kept short and plain for a non-science audience
- What to bring and what to wear
- Arrival steps and a two-day timeline, including set-up and breakdown windows
- Conversation starters for the table
- Travel and reimbursement details (Concur, mileage, train, hotel cap)
- The delegation roster
- Day-of contacts

## Source of truth

The content comes from the Scripps Communications planning doc for the summit ([Original Google Docs Page](https://docs.google.com/document/d/162IJhYUFdiR67XY2Pu3sLRILqIjk7MGzglb8c4yVHew/edit)). When that doc changes, update `index.html` to match. A few fields were marked TBD at build time (some attendees' confirmed days, table-staffing windows), so those are the first things to revisit as the date gets closer. Session-level timing defers to the [official HCS schedule](https://www.hollywoodclimatesummit.com/tickets/2026schedule).

## Editing

It's a static page, so editing is just editing one file.

1. Open `index.html`.
2. Change the text or times in place. The structure is commented in plain language (`<!-- DAY CARDS -->`, `<!-- ROSTER -->`, and so on), so you can jump to the section you need.
3. Commit and push. GitHub Pages redeploys on its own, usually within a minute.

To preview locally, open `index.html` straight in a browser, or run a quick local server from the repo folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

When you update content, bump the "Last updated" line in the footer so people know they're looking at current info.

## Deploying

Hosted on GitHub Pages off the default branch.

1. Push `index.html` to the repo.
2. In **Settings → Pages**, set the source to the default branch, root folder.
3. The page goes live at `https://sdiggs.github.io/2026-hollywood-climate-summit/`.

## A note on public visibility

This page is public, so anything in it is public. The current build includes the full roster with cell numbers, the reimbursement index codes, and a link to a shared Drive folder. That's fine for an internal-feeling logistics page, but it's a deliberate call, not an accident. If you'd rather not have those on an open URL, trim the roster to a single carpool-coordination contact, pull the financial codes, and drop the Drive link. The rest of the page stands on its own without them.

## Quick facts

| | |
| --- | --- |
| **Event** | Hollywood Climate Summit 2026 |
| **Dates** | June 3 (Samuel Goldwyn Theatre) and June 4 (The Ebell of Los Angeles) |
| **Role** | Scripps is a sponsor: table both days, plus a mainstage speaker |
| **Day-of leads** | Lauren Fimbres Wood and Robert Monroe (Communications) |
| **Repo maintainer** | Steve Diggs |

## License

Internal logistics page for the Scripps delegation. Reuse the structure freely for future event pages.
