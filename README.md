# 2027 Astrology Events

The free calendar that goes out with the 2027 Tarot Planner. Every season start,
moon phase, Mercury retrograde and eclipse for 2027. **67 events.**

## What is here

| Path | What it is |
|---|---|
| `index.html` | ⭐ **The hub.** Where planner buyers land. Every link lives here |
| `events/index.html` | The events page. Pick a time zone and the dates and times move with you |
| `images/` | The two cover images. See `images/README.md` |
| `calendar/2027-astrology-events-all-day.ics` | All-day markers, dated Eastern. The one most people want |
| `calendar/2027-astrology-events-times.ics` | Exact times, stored in UT, so each calendar renders it in its own zone |
| `moon-calendar/index.html` | ⭐ Twelve month grids. Print it and you have the wall calendar |
| `rituals/index.html` | ⭐ The premium version. Every event with a ritual |
| `calendar/2027-astrology-events-rituals.ics` | ⭐ The premium calendar, rituals in the event descriptions |

## Which calendar file to offer

**All-day** sits along the top of the day where people actually look. It carries
the Eastern time in the title. Because all-day events do not convert, subscribers
far from Eastern will see a handful of dates a day out.

**Exact times** is correct in every time zone automatically. It sits inside the
day grid, so a 3am moon is easy to miss.

Offer all-day as the main button and exact times as the alternative.

## The hub

`index.html` is the page the planner sends people to. Digital download, calendar
subscription, the events list, the moon calendar, the ritual upgrade, the
paperback, the workshop, and the school.

**Four links need pasting in before it goes live.** They are marked `PASTE_` with
a comment block at the top of the file naming each one: the digital PDF, the
workshop registration, the ClickFunnels checkout, and the Amazon listing.

**The calendars are offered as subscriptions rather than downloads**, so a later
correction reaches everyone who already subscribed. Google gets its own add-by-URL
link, everything else gets `webcal://`.

## The moon calendar

`moon-calendar/` renders all twelve months as grids, with every event plotted on
the day it happens and listed underneath with its sign. It replaces three jobs
that used to be done by hand:

- the calendar section of the astrology guide
- the printable twelve month wall calendar
- the PDF, via print to PDF

**Hit print and it lays out two months to a sheet**, six sheets, page breaks in
the right places, backgrounds dropped.

**The moons are drawn in CSS rather than typed as characters**, so every phase is
the same size and none of it depends on a font being installed. New moon solid
black, full moon gold, quarters gold on the correct side for the northern
hemisphere, lunar eclipse a coppery blood moon with the shadow biting in, solar
eclipse a dark centre with a corona. **Seasons carry their real zodiac glyph**,
with `U+FE0E` appended so they stay monochrome instead of turning into colour
emoji.

## The premium version

`rituals/` is the paid upgrade the planner landing page has been offering. Every
one of the 67 events carries a ritual: under fifteen minutes, using only what is
already in the house, one action rather than a list.

**It is written by sign and phase, not by date.** Twelve rituals for each of the
four moon phases, twelve season openings with a question to sit with, two eclipse
treatments and two for Mercury. Sixty-four pieces covering sixty-seven events.
**New Moon in Taurus reads the same in 2031, so every future year is a script run
rather than a writing job.**

The source library lives in `biz-brain` at `content/rituals/`.

**Every new moon names the date its full moon completes it**, same sign, roughly
six months on, where that lands inside the same year.

## Building a new year

Source data comes from Astro-Seek, in UT: the moon `.ics`, the sun ingress `.ics`,
the quarter moon tables and the Mercury station table. Everything is converted to
Eastern with that year's daylight saving applied.

**⚠️ Never generate the astronomy from memory.** Dates and times for moons,
eclipses and retrogrades look plausible and come out wrong. They come from a real
ephemeris or they do not go in.

**⚠️ Keep `.ics` files plain ASCII with short lines.** A file that parses is not a
file that imports.

## Notes on 2027

- **Five eclipses.** Two solar (Feb 6, Aug 2), three lunar (Feb 20, Jul 18, Aug 17).
  **Aug 2 is a total solar**, one of the longest this century, and it lands in Leo
  season.
- **No blue moon.** Twelve full moons, one per calendar month.
- **Two full moons in Scorpio**, Apr 20 at 0 degrees and May 20 at 29.
