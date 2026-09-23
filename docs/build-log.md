# Build log

What I tried, what broke, and what I kept.

## 2026-09-23

I locked the scoring rules today as [AURA v0](AURA.md). AURA is the AI User Ranking Algorithm, and I developed it in-house. A vote is a person saying they quit a tool, switched to it, kept using it, or that it has a problem. AURA turns each of those votes into a number, and the score is the average of those numbers. The extra point is only for a concrete thing you could point at, like a site someone actually built, or rows a tool deleted. A vague label like "for code" does not get that point.

One account gets one vote per tool. I use the 14 UTC days before the count day, and the count day is left out of that. When I publish a score, I publish the score, how many votes it came from, and the post ids that went into it. If there are fewer than 10 votes, it's determined to be too early to rank. I will still publish those, but they will not receive a ranking.

An ad, a giveaway, or a post from the official account of the company behind the tool doesn't count, even if it also claims use. That includes their announcement and their launch thread. A chart or a technical benchmark doesn't count when the poster never says they used the tool, because what I care about is real use, not a lab table. If that same post also says what they personally did with it, that part can still count. Posts from within this project by me are written down but left out so as to not influence the ranking. Me getting any money from this project will never change how a score is counted.

I wrote the [README](../README.md) in my own words and made sure it lines up with [AURA v0](AURA.md). The license is [AGPL](../LICENSE), copyright 2026 Artifex. If someone gives out a version, or people use their changed version over a network, they have to give those people the source.

## 2026-09-22

The scoring rules were not locked yet. I had a draft sheet, and it had two real problems. If someone said they switched to a tool, that could get scored as a loss for the tool they left, even when they never said they quit it. And if there were only one or two votes, the average could come out looking perfect, which it isn't. I already knew I did not want an extra point for something as vague as "for code."

I am still reading posts by hand. I have not decided how I will search for them, how many votes a tool needs before a rank means anything, or whether any of this counting gets automated later.
