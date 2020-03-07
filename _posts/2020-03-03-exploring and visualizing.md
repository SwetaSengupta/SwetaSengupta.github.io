---
layout: post
url: https://medium.com/@ssengupta801/exploring-and-visualizing-23152107c5aa
title: Exploring and Visualizing
subtitle: Patterns in City of Chicago Taxi Trip Dataset
#gh-repo: daattali/beautiful-jekyll
#gh-badge: [star, fork, follow]
#tags: [test]
comments: true

![taxi](img/8254827.jpg)


The taxi service is an important transportation mode in urban areas. In this project, I will be analyzing City of Chicago taxi trip data. This dataset does not include the taxi trips data from ride-sharing companies such as Lyft, Uber, etc.
 
 I have taken a sample of data from a huge dataset to see what all information I can get from it. Like,<i> how centralized is Chicago? Do Chicago residents use taxis more during rush hours? Is the taxi fare usually higher during rush hour? Is taxi fare higher in the downtown area? What is the relationship between distance traveled, time taken and fare?<>

## Hypothesis Generation:
<ul>
<li>Chicago is centralized</li>
<li>Chicago residents use taxis more during rush hour</li>
<li>Taxi fare is higher during rush hour</li>
<li>Taxi fare is higher for downtown Chicago residents than other parts of Chicago</li>
<li>If the distance traveled is more, then the fare is higher.</li>
<li>There is a strong relationship between distance traveled, time taken and fare.</li>
</ul>

## Hypothesis: Chicago is centralized

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plot.ly/~SwetaSengupta/16.embed" height="525" width="100%"></iframe>


The above plot shows most trips start out from the center of the city, around the airport area, and the University of Chicago. To understand this pattern better I have created a pie chart with ride counts from 20 most popular taxi pick up areas in Chicago.

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plot.ly/~SwetaSengupta/11.embed" height="525" width="100%"></iframe>

As you can see, more than fifty percent of ridership is concentrated in the downtown area. Therefore, it can be said that the taxi trip analysis shows that like most other cities in the world, downtown Chicago is also centralized. There are always many more taxi pickups and drop offs in those community areas in the city center.

## Hypothesis: Chicago residents use taxis more during rush hour

(plot here)

As the plot depicts only two areas in Chicago showed a significant difference otherwise the ride count is the same . On further investigation, it was seen that these two areas usually face huge traffic jams due to which most taxis avoid these routes during rush hour. Furthermore, when I conducted a T-test for means of the two independent samples with the null hypothesis that two independent samples have identical average (expected) values i.e there is no difference in ridership between rush hours and other times as expected the T test gave a p value is 0.99728. <i>Therefore it can be said that ridership is equal during rush hour and other times.<>

(plot here)

## Hypothesis : Taxi fare is higher during rush hour

Now let us explore whether the fare is higher during rush hours. After exploring the data it can be seen there is a difference in fare during rush hour and other times. But as the difference is only 3,826.73 dollars is this significant enough? So let us explore this further with a T-test for means with the null hypothesis that there is no difference in fare between rush hours and other times. The p value of 0.008651 confirmed that yes <i>taxi fare is significantly higher during rush hours.<>

(plot here)

## Hypothesis: Taxi fare in downtown Chicago is higher than other parts of Chicago

For this analysis I created two data sets, one of downtown Chicago and the other of other parts of the city. And by exploring this two datasets I found that the total fare amount is much higher in downtown area as the ridership is higher in downtown and<i> the taxi fare i.e the cost of travel is also higher for downtown Chicago than other parts of Chicago.<>

(polt here)

## Hypothesis: If the distance traveled is more, then the fare should be higher

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plot.ly/~SwetaSengupta/13.embed" height="625" width="100%"></iframe>

The plot clearly shows that there are multiple linear correlations between trip distance and cost. But for the majority of trips,<i> their cost depends on the distances<>. Most of the trips are small trips. In this case small trips are those which has a trip time of less than 15 minutes, trip distance of less than 2 miles and cost of less than 10 dollars.

## Hypothesis : There is a strong relationship between distance traveled, time taken and fare.

To understand the relationship between distance traveled, time taken and cost let us visualize the data with the help of some pair plots.

(plot here)

Basically, the distribution of trip duration, distance and cost are all little skewed to the right, meaning that majority trips are small trips. But as you can see there is a drop in the distribution of both trip duration and distance when the corresponding values are very small, and there is a small bump in distance and cost when the corresponding values are relatively large.Trip duration does not seem to have a linear correlation with distance. We can see that short trips take a long time to complete, whereas some long distance trips take less time to finish.

To explore this further we will analyse the correlation matrix of these features.

(plot here)

Analyzing the correlation matrix we can say that the mileage and duration of a trip tend to correlate with each other.The longer the trip, then longer time it takes to complete. The trip mileage correlates with trip duration. Trip fares have stronger correlations with trip distance and duration than those of total cost of trips. As many other random factors add to the total payment.The traffic condition is rather complicated in the city and it is hard to predict cost of the trip based on these factors only.

## Summary
<ul>
<li>From the taxi rides analysis we can say that Chicago is a centralized</li>
<li>Chicago residents do not use taxis more during rush hour</li>
<li>Taxi fare is higher during rush hour</li>
<li>Taxi fare is higher for downtown than other parts of Chicago</li>
<li>If the distance to be traveled is more, then the fare should be higher.</li>
<li>There is a strong relationship between distance traveled, time taken and fare.</li>
</ul>