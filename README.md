# Artificially Integrated

I am building an open-source ranking of AI tools and models from what real users say they did with them. I believe this is the first AI user benchmark.

A vote is a person saying they quit a tool, switched to it, kept using it, or that it has a problem. AURA (AI User Ranking Algorithm), developed in-house, turns each vote into a number, and the score is the average of those numbers. AURA reads posts and replies on X.

An ad, a giveaway, or a post from the official account of the company behind the tool doesn't count, even if it also claims use. That includes their announcement and their launch thread. A chart or a technical benchmark doesn't count when the poster never says they used the tool. If that same post also says what they personally did with it, that part can still count. Posts from within this project by me are written down but left out so as to not influence the ranking. Likes and views don't count either.

One account gets one vote per tool. I use 14 UTC days before the count day, and the count day is left out of that. When I publish a score, I publish the score, how many votes it came from, and the post ids that went into it. If there are fewer than 10 votes, it's determined to be too early to rank. I will still publish those, but they will not receive a ranking.

I'm building this in public under the name Artifex, including the parts that don't work yet. [@ArtifexInteg](https://x.com/ArtifexInteg)

## In this repo

Right now the repo holds the rules and the logs.

- [AURA v0](docs/AURA.md) is how a score gets counted.
- [Build log](docs/build-log.md) is what I tried, what broke, and what I kept.
- Results get added when I actually run a count.
- The site will get added when there's code that runs AURA and puts the scores on a page.

## Money

If a dollar comes in because of this project, it gets written down in public as its own dedicated money log. That includes getting paid for content, affiliate links, and anything else. Me getting any money from any part of this project will never influence the ranking of a system, model, or tool, and all source code and AURA rankings will be public at all times.

## License

This project is [AGPL](LICENSE). Copyright 2026 Artifex. If you give someone a version, or people use your changed version over a network, you have to give them the source.
