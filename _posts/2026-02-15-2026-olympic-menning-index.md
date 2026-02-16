---
layout: page-fullwidth
header:
    image: "logo.png"
    background-color: "#3a00ab"
title: Was the 2026 Olympics the hardest the men have ever menned?
categories:
- Men's Figure Skating
- Figure Skating
feature_image: "https://cdnph.upi.com/pv/upi/bb31a115a8639fc4943ae9210b5d1f39/MILAN-OLYMPICS-2026.jpg"
---
After a relatively clean team competition, the men really delivered on the chaos in the individual olympic event. This got me thinking, is the most chaotic/menningest men's competition in recent history? Short answer, yes. Long answer see below.

## What does it mean to men and how do we measure it?
Menning is the phenomenon when the rankings shift greatly between the Short Program and the Free Skate. So we are looking for a way to measure how rankings change between the short and free or between the short and overall ranking. I have come up with two different metrics for this. One is more easy to understand and one is more comprehensive.

### Podium Menning Index (PMI)
One way we can look at the level of chaos in a competition is to look at the rankings of the skaters on the podium. If all three podium skaters were in the top three in both the short and long, it indicates a lower chaos competition. If the podium skaters have lower rankings, then it is a higher chaos competition. The Podium Menning Index is calculated by adding the placements of the top three skaters and then subtracting 12. We subtract 12 so that if the top three were the top three for the short and the free, the Podium Menning Index would equal 0. For example in the 2026 Olympics we have $PMI = 5 + 1 + 2 + 6 + 9 + 3 - 12 = 14$ calculated from Mikhail, Yuma and Shun's rankings.  

### Spearman Menning Index (SMI)
In order to include all of the skater's results in a metric, I use the Spearman rank-order correlation. The Spearman rank-order correlation is a measure of the relationship between two rankings. If the two rankings are identical, the Spearman rank-order correlation would be 1. If the two rankings are in reverse order, the Spearman rank-order correlation would be -1. I decided to present my metric as a number from 0 to 100 for easier readability. $SMI = \left(1-\texttt{spearmanr}\left(\text{SP rankings},\text{FS rankings}\right)\right) \times 50$

## Results
Here are the results of the PMI and SMI at Worlds and the Olympics for the last three quads. For Olympic years I used just the Olympics and not Worlds. There was no worlds in 2020 due to covid. My code is [here](https://github.com/miajl/wtf_stats/tree/main/menning-calc).

<div class="row t60">
    <div class="medium-6 columns b30">
        <img src="/images/2026-02-15-menning-index/PMI.png" alt="PMI">
    </div><!-- /.medium-6.columns -->

    <div class="medium-6 columns b30">
        <img src="/images/2026-02-15-menning-index/SMI.png" alt="SMI">
    </div><!-- /.medium-6.columns -->
</div><!-- /.row -->

### SMI Sanity Check
To check that the metric is functioning how I wanted it to, I looked at the results from the next highest SMI (2015) and the lowest SMI (2023) to see if it matches my expectations. For the high SMI year 2015, over 50% of the skaters had a rank change of more than 3 between programs while in the low SMI year 2023 only 25% of the skaters had a rank change of more than 3. This matches with my expctations for high and low SMI years.

## Conclusions
Both the Podium Menning Index and the Spearman Menning Index indicate that the 2026 Olympics had higher than usual menning. We had the highest SMI of the three quads and the PMI was only beaten by 2024 where Adam Siao Him Fa jumped from 19th to 3rd place. Overall I think both menning indices are useful and I'm excited to apply them to the other disciplines. Are the pair's menning or are the men actually pairsing?