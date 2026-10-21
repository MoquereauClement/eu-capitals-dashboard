## The decision this dashboard supports

> **Reflection — before you build anything:** if you personally had to choose a
> destination, how would you weigh good weather against low CO₂? Would you ignore
> one of them entirely? Write 1-2 sentences now — you'll compare this to what the
> dashboard actually computes later in this TD.

I wouldn't ignore one of them entirely. I would weigh good weather and low CO₂ 
emissions equally, choosing a destination with pleasant weather while trying to 
minimize the environmental impact.

## Stage 1 — Acquisition: a static reference table and a live weather API

> **Reflection — acquisition reliability:** before reading the docstring above a
> second time: why would making 26 separate API connections from the same script,
> in a loop, be *more* likely to fail than making 1 connection for all 26 capitals
> at once — not just slower, but more likely to actually fail? Write your guess,
> then check it against the comment in `fetch_weather_batch`.

I think making 26 separate API connections in a single second can fail because it
could be registered as "too many requests in a minute".

> **Reflection — provenance (CM3):** the CO₂ figure (0.15 kg CO₂e/km) is a rounded
> value from a real, cited range (0.12-0.15, DEFRA-style short-haul factors) that
> the script's own comment says to "verify/update." If this dashboard were going to
> be used by real travelers next year instead of graded once, what would you
> actually do about this number before publishing it?

I would check the latest official emission and verify that the value is appropriate. 
I would update the number if necessary, cite the source, and review it regularly to
keep the CO₂ estimates reliable.

> **Reflection — relative vs. absolute:** `normalize()` finds the best and worst
> value *within this list of 26 capitals* and stretches everything between them to
> 0-1. If a 27th, unusually cold and rainy capital were added to the list, would a
> mediocre capital's real temperature change? Would its *score* change? What does
> that tell you about the difference between a measurement and a KPI built on top of
> it (CM2)?

If a 27th capital were added, the temperature of the others capital won't change.
However, the normalized score could change because the highest and lowest value would change.
The KPI is based on the normalized value so its influenced by the measurement. 

> **Reflection — predict, then check:** based on the personal weighting you wrote
> down at the very start of this TD, which capital do you *predict* will come out
> on top once you run this script for real? Write the city name and one sentence of
> reasoning now, before you run anything.

I predict that Lisbon will be ranked among the top destinations because it often has
sunny weather and warm temperatures.

> **Reflection — was your prediction right?** Compare the real top-ranked capital
> to what you predicted in Stage 3. If they match, what does that tell you about how
> well you understood the 50/50 formula? If they don't match, what surprised you —
> was it the weather data, the distance, or the formula itself?

I predicted Lisbon and the top-ranked is Rome, although Lisbon is second and really 
close to the score of Rome. I underestimated the impact of the CO² emissions, as 
Lisbon does not score very well.

