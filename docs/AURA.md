# AURA v0

AI User Ranking Algorithm. 2026-09-23.

This is the scoring algorithm for Artificially Integrated. Score one AI tool from what people say they did with it.

## 1. Take the window

Keep posts and replies from the 14 UTC days before the count day. The count day is out. A reply is a post. Likes and views are ignored. Posts from this project by the person publishing the score are written down and left out, so they don't influence the ranking.

## 2. Make one row per tool in that post

Drop the row when the post is an ad, a giveaway, or a post from the official account of the company behind the tool, even if it also claims use. That includes their announcement and their launch thread. Drop a chart or a technical benchmark when the poster never says they used the tool. If that same post also says what they personally did with the tool, score that part. “Giveaway entry. I switched to Claude and rebuilt the docs site with it.” is dropped.

Otherwise read the whole post and take the first match:

| Class | b | Vote |
|---|---:|---|
| Quit | −3 | yes |
| Switched | +3 | yes |
| It’s a problem | −1 | yes |
| Still using | +2 | yes |
| Name only | 0 | no |

“I switched to Claude. It is a problem.” is switched. “I switched to it. I’m still using it.” is switched.

s = 1 when the post names a concrete outcome for that tool. Otherwise s = 0. If unsure, s = 0.

If b is positive, p = b + s. If b is negative, p = b − s.

- Still using and s = 1 → +3
- Switched and s = 1 → +4
- Quit and s = 1 → −4
- It’s a problem and s = 1 → −2

“I built my business website with it, and it came out like this” is s = 1. “It deleted rows 40–90 of the March invoice table” is s = 1. “For code,” “for spreadsheets,” and “I switched” are s = 0.

## 3. Keep one vote per account, per tool

Sort by post time. If the times match, the higher post id is later. The later vote replaces the earlier one. A name-only post does not erase a vote.

One exception: “still using” does not replace “switched” while switched is still the vote. A later quit, or a later “it’s a problem,” does. After that, a later real vote replaces the current one, including a later “still using.”

Switched, then “it’s a problem,” then “I still use it” ends as still using.

## 4. Divide

n is how many votes are left. If n is 0, the result is “no votes.” Do not divide. Otherwise R = (the p values added up) / n.

## 5. Publish

Publish R, n, and the post ids that went into them. If n is under 10, it is too early to rank. Still publish R, n, and the post ids. Those do not receive a ranking.

Classifying the sentence stays with the reader. A wrong real post gets one example later.
