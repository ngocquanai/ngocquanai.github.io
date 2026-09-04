---
title: 'Does a Low OpenReview Submission ID Help?'
date: 2026-09-04
permalink: /posts/iclr-submission-id/
description: "The sooner you create your submission, the higher your acceptance rate is?"
tags:
  - ICLR
  - Data Analysis
  - OpenReview
---

Recently, I heard that some people open their OpenReview submissions early just to claim a low paper ID. Of course, maybe there is some logic behind this. It costs almost nothing, just a few minutes to create a submission on OpenReview. So if opening it early could somehow give even a tiny advantage, why not, right? 

In this blog post, I did some simple statistics with ICLR submissions to see whether there is actually anything interesting there. Notice that the “paper ID” (the numeric submission number) is assigned based on creation order. Earlier submission, lower number.



## Does a lower submission ID mean a higher acceptance rate?

I sorted the papers by submission number and split them into ten roughly equal-sized groups, or deciles, from the earliest 10% to the latest 10%:

![Acceptance rate by submission-ID decile for ICLR 2025 and 2026](/images/iclr-submission-id/fig2-deciles.png)

*Acceptance rate by submission-ID decile for ICLR 2025 and 2026. Dashed line is overall acceptance rate.*
{: .text-center}

At ICLR 2025, 36.7% of papers in the earliest 10% were accepted, compared with 27.7% in the latest 10%. In 2026, the corresponding rates were 33.0% and 20.3%. Submissions created in the final six hours before the deadline did even worse: 24.1% of 470 papers in 2025 and 18.3% of 1,083 papers in 2026 were accepted.

Of course, this is correlation, not evidence that grabbing a low paper ID will get your work accepted. But if you needed one more reason not to wait until the last few hours to create your OpenReview submission, there it is!

---

## But this pattern only appeared recently

There was one thing I did not expect, and it is even more surprising. Here is the same decile curve across all five years, with the two older years separated from the three more recent ones:

![Acceptance rate by submission-ID decile, ICLR 2022-2023 on the left and 2024-2026 on the right](/images/iclr-submission-id/fig3-years.png)

*Same axes on both sides, the two older years are on the left, and the three recent years are on the right.*
{: .text-center}

| Year | Papers | Decile 1 | Decile 10 | 
|---|---|---|---|
| 2022 | 3,422 | 36.4% | 33.2% |
| 2023 | 4,955 | 29.8% | 30.8% | 
| 2024 | 7,404 | 32.1% | 26.2% | 
| 2025 | 11,672 | 36.7% | 27.7% | 
| 2026 | 19,814 | 33.0% | 20.3% |

In 2022 and 2023, there is no clear or consistent early-submission advantage. The acceptance rate remains roughly uniform across the ten decile groups, which feels much closer to what we would naturally expect, right?

The pattern first appears in 2024, when the acceptance rate for the first decile was about 5.9 percentage points higher than that of the last decile. The gap then widened to 9.0 percentage points in 2025 and 12.7 percentage points in 2026.


I do not yet have a good explanation for this, and I have not run formal statistical tests, so I cannot make a formal claim about statistical significance. Still, the trend in the raw data looks quite clear. Together with the recent boom in submission numbers, this makes me wonder: *what, exactly, has changed in the last few years?* I will not put my guess here, but maybe you already have yours...



## Some more interesting figures about submission number


I selected the 50 institutions with the most accepted papers in each year. Among them, the top 20 are labeled directly in the figures.

The horizontal axis shows each institution's median submission percentile rather than the raw submission number, so the two years can be compared directly even though their ID ranges are very different.


![Median submission-ID percentile against acceptance rate for the 50 institutions with the most accepted ICLR 2025 papers.](/images/iclr-submission-id/fig4-institutions-2025.png)

*ICLR 2025. Bubble size represents the number of accepted papers. The dashed lines mark the overall acceptance rate.*
{: .text-center}

![The same chart for ICLR 2026, showing the same left-right split between Chinese and US institutions](/images/iclr-submission-id/fig4-institutions-2026.png)

*ICLR 2026. Same rules and axes as above.*
{: .text-center}

Among these top institutions, there is no obvious sign that submitting earlier comes with a higher acceptance rate. Many large institutions sit on the later side of the figure while still staying well above the overall acceptance rate.

So, one more reminder: the findings in this blog are fun and surprising patterns, not a submission strategy.

More than 80% of the institutions in these figures are from China or the US (41/50 in 2025 and 42/50 in 2026). But there is one interesting pattern here: Chinese institutions sit noticeably further to the left than US institutions, meaning that they tend to create their submissions earlier. Almost the same split appears in both years.

The clearest exception is NVIDIA. Its median submission percentile is much lower than those of the other US institutions, while its acceptance rate is close to 50% in both years.

| | Number of Institutions | Median percentile | Mean acceptance rate |
|---|---|---|---|
| Chinese institutions, 2025 | 17 | 41% | 35.2% |
| US institutions, 2025 | 24 | 58% | 42.3% |
| Chinese institutions, 2026 | 23 | 35% | 32.8% |
| US institutions, 2026 | 19 | 57% | 36.9% |


Still, it is hard to read much more into these figures from submission numbers alone. Since most submissions are created in the final few days, part of the difference between countries could simply come from time zones and normal working hours. So again, these are interesting descriptive facts, not serious conclusions about institutions or countries.

---


![Submissions per day before the deadline, ICLR 2025 and 2026](/images/iclr-submission-id/fig1-when.png)

*Submissions per day before the deadline, ICLR 2025 and 2026.*
{: .text-center}


Despite all this discussion about early and late submissions, most papers are not created very early at all. Around two-thirds of all submissions were created during the final 72 hours before the deadline in both years.

Finally, submissions come from all around the world, but their creation times still follow a surprisingly clear daily rhythm. I plotted the share of submissions opened during each UTC hour, excluding the final 48 hours. Since the deadline occurs at the same moment for everyone, those final two days are dominated by the countdown and would hide the usual pattern.


![Submissions by UTC hour of day, 2025 and 2026](/images/iclr-submission-id/fig7-clock.png)

*Submissions by UTC hour of day, 2025 and 2026.*
{: .text-center}

The busiest hour is 07:00–08:00 UTC in both years, while the quietest is 23:00–00:00 UTC. Apparently, even a global submission queue has a daily routine.
...


