# A Comparison of U.S. Flight Delays Over 3 Decades
## by Matt Brendel


## Dataset

The dataset consists of flights in the United States, including carriers, arrival and departure delays, and reasons for delays in 1988, 1998, and 2008.
Source: http://stat-computing.org/dataexpo/2009/the-data.html

## Resources used

Aside from Udacity class notes and various Google searches (yielding mostly Github and Stack Overflow articles), we didn't use any other resources.


## Summary of Findings

We first condense the dataset to look at the top 5 airlines by flight count. We are able to see that ArrDelay (arrival delay) and DepDelay (departure delay) columns are highly correlated, leading us to focus on DepDelay as one of our main features of interest for the analysis.

Through a logarithmically scaled histogram, we see that DepDelay is unimodal, with the majority of data points falling between -1 and 0 mins (most flights on time).

CRSElapsedTime (Elapsed flight time) is also unimodal, with slight peaks at ~85 and 250 mins, which makes sense with typical regional flights just over 1.5 hours and cross-country flights over 4 hours.

Focusing on the top 15 Dest (destinations) by flight count, we see that the dataset has the most flights for ORD (Chicago), followed by Houston and Atlanta. This makes sense, as we know those airports are all major flight hubs.

WN (Southwest) has the most flights in this dataset, followed by Delta. 1998 has the most data across the three years.

When looking at bivariate plots, we see that SFO leads in delay times, on average, and LGA leads in cancellation rate. On the carrier side, UA leads in both average delays and cancellations.

When encoding for Year as a third variable, we see that delay times increase over the three decades. Cancellations increase to 1998, but then slightly improve, on average, for 2008. We wonder whether advancements in airport infrastructure and/or technology helped fuel this turn-around.


## Key Insights for Presentation

We focus our analysis on the DepDelay variable for our explanatory presentation. As such, we include most of the relevant visualizations we developed during our exploratory analysis for this feature, leaving out our parallel exploration of the Cancelled variable.

We walk our audience through answering: which destination airports/cities are home to more delays & which carriers have the best on-time performance over the three decades?

We use the full flts_c (cleaned dataset) df, versus the sample we were using during the exploratory phase to yield faster calculation times. Otherwise, we do not change our design from the exploratory phase, but clean up the visualizations to ensure they have titles and correct labels for our audience.