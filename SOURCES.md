# RAVI News watchlist (Muse's digest sources)

Checked daily by the `ravi-facebook-digest` cron. Edit this file to change coverage.
This file lives at `ravi-news/SOURCES.md`. Daily digest files are
`<YYYY-MM-DD>.json` at the repo root.

Every entry carries a tier label. Tiers are never mixed in output:
- OFFICIAL — Riot / Riftbound official channels. The News section's main feed.
- COMMUNITY — player-community sources. Shown separately from official news.
- LOCAL — Vancouver Island stores and events. Shown separately from official news.

## OFFICIAL — primary (website first, social second)

The official website is the primary source: Facebook/Instagram/X posts are
downstream of it. Check the website news index first each run, then socials
for items the site does not carry (reels, short announcements, event posts).

- https://riftbound.leagueoflegends.com/en-us/news/ — official news index
  (also https://playriftbound.com/en-us/news/). Articles are dated and
  categorised (Announcements / Organized Play / Rules and Releases).
  Check every article from TODAY, TODAY-1, TODAY-2 (Pacific).
- https://playriftbound.com/en-us/rules-hub/ — Rules Hub. Track directly:
  poll the last-updated dates on the banned/legality list, Core Rules PDF,
  Tournament Rules PDF, per-set Core Rules Patch Notes and per-set Errata.
  Any date change is a digest item (kind: rules).
- https://www.facebook.com/profile.php?id=61573928660847 — official
  Riftbound page (facebook.com/playriftbound). Full detail recorded.
- https://www.instagram.com/playriftbound/ — @playriftbound, via the
  connected Instagram CLI (`posts --username playriftbound`). MUST filter
  results to username == "playriftbound" — the CLI mixes in other accounts.
  Reels and carousels (card reveals, BTS video) are the unique value here.
- https://www.youtube.com/@riftbound — official YouTube. Stream/VOD
  links and evergreen guides. Event-day bursts only; dedupe by video title
  against Facebook. Also https://www.twitch.tv/riftbound (same streams).
  (Handle confirmed 2026-11-08: Riot's own video descriptions link
  @riftbound; @playriftbound 404s.)

## OFFICIAL — secondary (optional)

- https://twitter.com/playriftbound — @playriftbound on X. Heavy duplication
  with Instagram/Facebook. Only add if a readable route is confirmed
  (Instalker mirror works; direct x.com readability unverified — needs a
  live-browser check). Also track retweets of @riftboundop (organized play)
  as their own items.

## COMMUNITY

- https://www.reddit.com/r/riftboundtcg/ — r/riftboundtcg (NOT r/Riftbound).
  FILTERED ONLY: top posts by score and/or news/decklist flairs and
  keyword filter. Never the raw feed (~48 posts/day, noisy). Skip memes,
  rules-lawyer threads, complaints, buy/sell (banned there anyway), and
  pulls photos (megathread-only). Fetch via the subreddit RSS feed
  (https://www.reddit.com/r/riftboundtcg/.rss) or the JSON endpoint
  (https://www.reddit.com/r/riftboundtcg/.json) — direct reddit.com page
  fetches are blocked.

## LOCAL — Vancouver Island stores and events

Backbone: the official Riftbound Gaming Network locator —
https://locator.riftbound.uvsgames.com/ — event pages are publicly readable
and give store, date, time, format, players, results. Check it every run.

- Skyhaven Games, Victoria — https://www.facebook.com/SkyhavenGamesVictoria
  (read via mirror https://www.findglocal.com/CA/Victoria/111540571855153/Skyhaven-Games ;
  direct Facebook feed is not readable). Nexus Nights: Sundays per recent
  group standings (Nov 1, Oct 25); Mondays 6:00–8:30 PM also listed
  historically — the group is the authority.
  Locator: https://locator.riftbound.uvsgames.com/events/477503
  Group (VERIFIED 2026-11-08, 166 members, private): Skyhaven Games Riftbound
  (League of Legends) Group — https://www.facebook.com/groups/1289633928950754/
  Read via `facebook-cli groups posts --group-id 1289633928950754`.
  Nexus Night standings, skirmish sign-ups and store notices live here — check
  it every run. The store's own page posts less often than the group.
- Colossal Cards & Collectables, Courtenay — https://www.facebook.com/100171202116663/
  (read via mirror https://www.globuya.com/CA/Courtenay/100171202116663/Colossal-Cards-and-Collectables).
  Weekly casual play + skirmish results; strongest up-island source.
- Colossal Cards & Collectables, Victoria — https://www.facebook.com/profile.php?id=61576236034631
  Monthly calendar; occasional Riftbound skirmishes.
- Rotty's Creations, Victoria — https://www.facebook.com/RottysCreations/posts/pfbid028uEbvzdqHKH6i5ApSLEVZkVGddidTVzARL1wJR64eYJkiNyGeYtbL8PzyagfhitKl
  Riftbound Tuesdays 5–8 PM. New shop (opened Oct 2026) — confirm still running.
- Gauntlet Games, Victoria — https://www.facebook.com/GauntletGamesVictoria
  Monthly events calendar; Riftbound League of Legends Tournament among the
  recurring events (Nov 3, 2026 calendar). Website news list is stale
  (nothing newer than Jul 10, 2026) — use the Facebook page.
- North Park Framing and Collectibles, Victoria — https://www.facebook.com/profile.php?id=61557444613977
  (website https://npframing.ca/). Runs Riftbound (Vendetta pre-release
  Jul 25, 2026) but Magic-focused; check the Facebook page.
- Everything Games, Langford — https://www.facebook.com/everythinggames.ca
  (721 Station Ave). Carries Riftbound; direct Facebook reads return
  profile-only, so this one may need the live browser.
- Elite4 Games, Langford — 2770 Leigh Rd. No Facebook page found; events
  announced via their Discord (unreadable from here) and
  https://www.elite4games.com/Local-Events (bot-walled). Saturday events
  rotate between Pokémon, Riftbound and Trade Day. Monitor only.
- AJ's Games, Campbell River — monitor only via the locator
  (https://locator.riftbound.uvsgames.com/events/296313). No recent activity.

## NOT sources

- Threads — no official Riftbound account exists. Do not add unless Riot
  launches one.
- Discord — no official Riot-run server found; discord.gg/riftbound is a
  community server and is login-gated (unreadable without joining).
- Board Game Paradise, Redlands, CA — runs Nexus Nights but is in
  California, not Vancouver Island. Excluded.

## Paused — groups and events (unchanged)

Local events are handled through the separate system above (locator + LOCAL
tier); the old Facebook group/event watch below stays paused. May be
re-enabled later as an extra precaution.
Groups (via `facebook-cli groups posts --group-id <id>`):
- 524513897119175 — Vancouver Island Riftbound
- 1481899039854322 — Riftbound BC
- 802203088987543 — Riftbound - Vancouver, B.C
- 1946261896221994 — Riftbound TCG - Rulings & FAQs
- 604213538783585 — Riftbound - League of Legends TCG
- 1269068458149392 — Riftbound TCG Community
- 940127361498628 — Riftbound Trading Card Game Community
- 1667468063763658 — Riftbound League of Legends TCG Canada
- 1670715730306339 — Riftbound TCG Global Exchange
Events (via `facebook-cli events search`):
- `--scope discover --keywords "Riftbound" --latitude 48.43 --longitude -123.36 --radius-in-miles 80`
- `--scope connected --keywords "Riftbound"`
