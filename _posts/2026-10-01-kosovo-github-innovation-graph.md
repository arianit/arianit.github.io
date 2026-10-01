---
layout: post
title: Kosovo's software industry, seen through GitHub data
---

## In short

Kosovo has the third highest number of active software developers per person in the Western Balkans, behind Slovenia and Croatia and ahead of Serbia, North Macedonia and Albania. Since 2023, coding activity has grown faster in Kosovo than anywhere else in the region. The total amount of activity is still low, though: 145 code pushes per 1,000 residents in 2025, ahead of only Albania and Bosnia. Serbia has 248, Slovenia 304. So many people in Kosovo are coding, but each pushes less code than developers anywhere else in the region. But only 343 of Kosovo's roughly 2,500 active developers, or 13.5%, worked in repositories under an open-source licence, the lowest share in the region, so most of the code they publish can't legally be reused. GitHub's data for Kosovo starts in the last quarter of 2021.

## What this data is

GitHub is where most of the world's developers write, store and share code. Every quarter, through its [Innovation Graph](https://innovationgraph.github.com/), it publishes how many developers are active in each country, which programming languages they use and how much they work with people abroad. It is one of the few public sources that allows comparing software workforces across countries, and governments and investors use it where official statistics are missing or late. Because location comes from IP addresses, the figures cover developers working in Kosovo, not the Kosovar diaspora, who are counted in the countries where they live.

GitHub started counting Kosovo separately in the last quarter of 2021, using the code XK, which [exists for cases like this](https://www.iso.org/glossary-for-iso-3166.html) where a country has no permanent international code. Before that, Kosovo is missing from the data even though developers here were working. During the first year, the figures climb mostly because location detection improved, not because of real growth, so this analysis starts in 2023.

## Before reading the numbers

Some networks in Kosovo are [registered under Albania or Serbia](https://www.ripe.net/about-us/news/ripe-ncc-response-to-arkep/), so some developers in Kosovo may be counted as Albanian or Serbian. GitHub does assign XK to many Kosovo addresses, otherwise Kosovo would not appear in the data at all, but we can't tell how many are missed. If some are, three things follow. Kosovo's figures are an undercount, so this post treats them as a minimum. Albania's and Serbia's figures are slightly inflated, so in the per-person comparisons Kosovo's real position is, if anything, better than shown. And some of what shows up as collaboration between Kosovo and Albania or Serbia may in fact be developers in Kosovo working with each other.

## How many people develop software

The number of registered accounts says little, since it includes abandoned ones. A better measure is how many people pushed code in the latest quarter (early 2026):

![Software developers writing and sharing code, per 1,000 people](/images/kosovo-github-active-developers.svg)

In that quarter, about 2,500 developers in Kosovo pushed code, roughly 1.6 per 1,000 residents. [Data](https://github.com/github/innovationgraph/blob/main/data/languages.csv?plain=1#L180192)

## Growth

![Growth in coding activity, 2023 to 2025](/images/kosovo-github-growth.svg)

The yearly number of code pushes from Kosovo almost doubled between 2023 and 2025, the fastest growth in the region. [Data](https://github.com/github/innovationgraph/blob/main/data/git_pushes.csv)

## What kind of work

Developers in Kosovo work mainly on the web (HTML, CSS, JavaScript) and in PHP, which is widely used for business systems and content sites. Albania has a wider range: languages tied to mobile apps, data analysis and systems programming (Kotlin, Swift, C, Jupyter Notebook) pass the reporting threshold there but not in Kosovo.

![Kosovo: developers working in each programming language](/images/kosovo-github-languages.svg)

Since 2023, the number of developers in Kosovo has grown in every one of these languages. TypeScript and Python grew most, each more than tripling. [Data](https://github.com/github/innovationgraph/blob/main/data/languages.csv?plain=1#L180192-L180206)

## Working with other countries

The table shows how many contributions developers in Kosovo made to code owned by people in other countries, and the reverse, during 2025:

| Kosovo contributes to | | Contributes to Kosovo | |
|---|---|---|---|
| Albania | 2,475 | Albania | 2,452 |
| United States | 2,348 | Netherlands | 540 |
| France | 2,311 | Germany | 341 |
| Germany | 1,738 | United States | 246 |
| Norway | 791 | North Macedonia | 127 |
| Austria | 396 | | |

Albania is Kosovo's biggest partner in both directions, and the exchange is close to even. Contributions coming from Albania are more than four times those from the next country, the Netherlands. Going the other way, Albania is only slightly ahead of the United States and France.

*Disclaimer: networks in Kosovo are usually registered under Albania at the IP registry level. If GitHub places some of those users in Albania, part of the Kosovo-Albania figures above is really developers in Kosovo working with each other, and Albania's lead over Kosovo's other partners is smaller than shown. The data gives no way to measure this, so the Albania figures are reported as published.*

*Serbia is left out of the table. In the raw data it was the second largest source of contributions to Kosovo (607), ahead of Germany and the United States, and received 534 from Kosovo. I treat this as most likely developers in Kosovo on networks registered under Serbia, as described above, so it is counted as activity within Kosovo rather than with Serbia. The data can't confirm this.*

[Data](https://github.com/github/innovationgraph/blob/main/data/economy_collaborators.csv)

## Open-source licences

Public code is not the same as open code. If the author doesn't add a licence, all rights stay reserved: others can read the code but have no right to build on it.

Counting all open-source licences that pass the reporting threshold, the share of active developers working in licensed repositories in early 2026 was: Kosovo 13.5%, North Macedonia 22.1%, Albania 23.0%, Bosnia 32.5%, Montenegro 33.1%, Croatia 47.0%, Serbia 50.3%, Slovenia 60.6%. In every quarter since Kosovo entered the data, MIT is the only licence it has passed the threshold with. Serbia passes it with six (MIT, Apache, GPL-3.0, AGPL-3.0, GPL-2.0 and BSD). A developer who works under two licences is counted twice, so the shares for countries with several licences are somewhat overstated. Kosovo's, with a single licence, is not. [Data](https://github.com/github/innovationgraph/blob/main/data/licenses.csv?plain=1#L21554)

Code without a licence can't legally go into commercial products or other open-source projects. Adding a licence takes a few minutes, so the problem looks like a lack of awareness rather than of skill.

## Notes on the data

- Source: GitHub's Innovation Graph, [version 1.0.11](https://github.com/github/innovationgraph), published under CC0.
- For Kosovo, data from 2023 onward is used, for the reasons above.
- Active developers and the licensed share refer to one quarter (early 2026). The data doesn't allow counting unique people across several quarters, so these figures shift a little from one quarter to the next.
- Growth and collaboration are summed over full years, since they count actions, not people.
- When a figure falls below 100 people, GitHub doesn't publish it, to protect privacy. A missing figure looks the same as zero.
- Population comes from each country's latest census. Bosnia's census is from 2013, so its figures are less reliable.
