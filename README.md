# 2027 Astrology Events

The free calendar that goes out with the 2027 Tarot Planner. Every season start,
moon phase, Mercury retrograde and eclipse for 2027. **67 events.**

## What is here

| Path | What it is |
|---|---|
| `index.html` | The events page. Pick a time zone and the dates and times move with you |
| `calendar/2027-astrology-events-all-day.ics` | All-day markers, dated Eastern. The one most people want |
| `calendar/2027-astrology-events-times.ics` | Exact times, stored in UT, so each calendar renders it in its own zone |

## Which calendar file to offer

**All-day** sits along the top of the day where people actually look. It carries
the Eastern time in the title. Because all-day events do not convert, subscribers
far from Eastern will see a handful of dates a day out.

**Exact times** is correct in every time zone automatically. It sits inside the
day grid, so a 3am moon is easy to miss.

Offer all-day as the main button and exact times as the alternative.

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
