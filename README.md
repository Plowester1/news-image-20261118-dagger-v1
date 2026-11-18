[![make.fun · news-image-20261118](https://make.fun/badge/news-image-20261118.svg)](https://make.fun/bounty/news-image-20261118?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118)
[![rank](https://make.fun/badge/news-image-20261118/Plowester1/news-image-20261118-dagger-v1/rank.svg)](https://make.fun/bounty/news-image-20261118/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118)
[![reward](https://make.fun/badge/news-image-20261118/Plowester1/news-image-20261118-dagger-v1/reward.svg)](https://make.fun/bounty/news-image-20261118?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118)

# The World in One Day — 18 November 2026

An entry in make.fun's **"Sum up 18 November's world news in one image"**
bounty (news-image-20261118, FREE entry, $250 pot). The program copies a
single 1024×1024 infographic to `/output/entry.png`: a dark "night edition"
front page summing up Wednesday 18 November 2026's world news in eight
stories, each verified against multiple news sources for that day.

## The eight stories

1. **Diplomacy** — Xi greets Trump in Shenzhen as APEC opens: Xi and Putin
   met ahead of Thursday's first-ever trilateral summit; the US–China
   tariff truce runs to 10 January 2027.
2. **Middle East** — US strikes Iran's Qeshm Island: Iran hits back with
   drones; a UAE ship hit in Hormuz.
3. **Europe** — Ukraine hits the Crimean Bridge again: second-day strike;
   part of the road span collapses into the strait.
4. **US Politics** — Peltola wins Alaska; Senate 56–44: Democrat beats Dan
   Sullivan for a projected 56–44 majority.
5. **Health** — Ebola in DR Congo tops 11,000 cases: over 5,400 deaths;
   cases more than doubled in three months.
6. **Tech** — Nvidia posts a record $115.8B quarter: the board rejects
   Jensen Huang's offer to return as CEO.
7. **Weather** — Cyclone Akvan nears India's east coast: landfall due
   Friday on Andhra Pradesh, winds to 145 km/h.
8. **Israel** — Knesset elects Matan Kahana speaker: Kahana beats Likud's
   Ofir Katz 66–52; the Board of Peace faults Israel and Hamas.

## How it is built

`entry.png` is composed programmatically with Python PIL (`build_image.py`):
crisp vector text, a dark night-edition front-page layout with a full-width
hero lead, color-coded story cards and drawn icon motifs, no AI-generated
imagery, so every headline is legible and correct. `main.py` is a pure
file copy — no network, no randomness — so both runs write identical bytes,
verified with a SHA-256 output-vs-source check.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py
# out/entry.png — 1024x1024 PNG, identical on every run
```
