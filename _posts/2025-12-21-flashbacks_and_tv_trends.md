---
layout : post
title : Stuck in the Past: Why Are TV Shows Obsessed with Flashbacks?
---

# Introduction

I have a confession: I watch a lot of TV. In today’s age of “time optimizers,” where you’re chastised for not maximizing every nanosecond, this has become a slightly rebellious thing to admit. But this article isn’t an apology for my love of serial crime dramas, it's about something more important: why are we seeing so many flashback episodes on TV?

In the right hands, the flashback episode is a valuable storytelling device, providing a new canvas for writers to fill in the missing parts of the tapestry. Learning about Don Draper inhabiting the identity of another man provided a fresh lens for viewing Don’s journey. However, when misused, it feels like you’re watching a legal proceeding, being hit over the head with facts and events designed to create an airtight alibi for the main plotline. In the worst scenario, it’s just filler: empty calories of TV consumption. Recently, I’ve been noticing the flashback more. It seems I’m not alone in fuming about this (alone)[https://www.vulture.com/article/penultimate-flashback-tv-episodes.html].

Rather than just stew about it, I decided to dig into the data. Are flashbacks actually on the rise? And if so, what’s fueling their newfound popularity?

# The Data

I pulled the top 50 shows for each year from IMDb, covering 1995 to 2025, and focused on those airing on US networks or streaming platforms. For every show, I grabbed metadata and episode lists from Wikipedia. Since Wikipedia’s episode descriptions are crowd-sourced and surprisingly detailed, they made a perfect source to hunt for flashbacks.

To pinpoint flashback episodes, I used a two-step approach: first, I ran a keyword search to flag possible candidates. Then, I brought in an LLM (large language model) to separate the true flashbacks from shows simply set in the past. The prompt nudged the LLM to focus on episodes where the action jumps back from the main timeline.

# The Rise of Flashbacks

So, are flashbacks actually becoming more common? The data says yes, loud and clear. In 2010, about 2% of episodes featured a flashback. By 2025, that’s climbed to 8%. The chart below makes the trend hard to miss.

<iframe src="../posts_images/2025-10-21-movie-analysis/interactive/flashback_by_year.html" width="100%" height="600px" frameborder="0"> </iframe>

Why the sudden surge in flashbacks? I have two theories:

* Who makes it: Some studios may have preferences for certain ways of telling stories.
* What gets made: Certain genres lend themselves to flashbacks, while others do not.

Of course, these forces can feed off each other. Studios with a taste for certain genres might also favor particular storytelling tricks. Still, I wanted to tease them apart and see what each explains on its own.

## Who Makes TV, or the Big 4’s Fall

For decades, American TV was ruled by linear networks, the Big 4 (Fox, ABC, NBC, CBS) and the big-name cable channels (think HBO, AMC, Cartoon Network, Comedy Central, and more). From the mid-90s through 2008, about half of top shows aired on the Big 4, with nearly as many on cable. Fast forward to 2025: just 13% of our list comes from the Big 4, and cable’s down to 20%.

<iframe src="../posts_images/2025-10-21-movie-analysis/interactive/network_group_share.html" width="100%" height="600px" frameborder="0"> </iframe>

My dataset is not “viewership”; instead, it’s a selected list of top shows as voted on by IMDb users, so there is certainly some bias. But a recent Nielsen report from November 2025 puts broadcast TV at 23.2% and cable at 20.5% of viewership, which lines up pretty well with my findings. One reason my numbers are a bit lower: live events (especially sports), where broadcast still calls the shots.

<img src="/posts_images/2025-10-21-movie-analysis/static/nielsen_report_2025.png" alt="Nielsen Report 2025" width="100%">

Who makes a show matters a lot because flashback rates vary dramatically by network. Below, you’ll see flashback rates broken down by network. Streamers are far more likely to serve up a flashback than legacy networks. What’s wild is that some streamers (like Hulu) are owned by the legacy players themselves. We’ll get into whether it’s the studios themselves driving this trend.

<iframe src="../posts_images/2025-10-21-movie-analysis/interactive/flashback_by_network.html" width="100%" height="600px" frameborder="0"> </iframe>

So are the networks themselves changing, or is it just the mix of who’s making TV? Around 2015, cable channels started leaning into flashbacks, and streamers went all in. These days, streamers and cable are neck-and-neck in terms of flashback frequency. So, part of the rise is a classic mix shift: streamers and cable have always loved flashbacks, and there’s just more of them now.

<iframe src="../posts_images/2025-10-21-movie-analysis/interactive/flashback_rate_by_group.html" width="100%" height="600px" frameborder="0"> </iframe>

## What TV Gets Made

Who’s making the shows matters, but what’s getting made might matter even more. Some genres are flashback-friendly by nature. Take Mad Men, a character-driven drama where flashbacks are a storytelling staple, fleshing out characters in ways your average sitcom would never need.

The data shows another big shift: the slow death of the comedy. Back in 1995, comedies were nearly half the list, at 44%. By 2025, they’re just 6%. Meanwhile, genres like thrillers, drama, and dark comedy have come into the spotlight, accounting for about 35% of shows.

<iframe src="../posts_images/2025-10-21-movie-analysis/interactive/genre_distribution.html" width="100%" height="600px" frameborder="0"> </iframe>

Can genre changes explain some of the rise in flashbacks? More serious genres (drama, thriller) lend themselves to flashbacks, while less serious ones do not. We can see that very clearly: thrillers are more than twice as likely to have a flashback as a comedy.

<iframe src="../posts_images/2025-10-21-movie-analysis/interactive/flashback_by_genre.html" width="100%" height="600px" frameborder="0"> </iframe>

## Using Math to Get an Answer

So what’s really driving the trend? Is it just that the types of shows being made are changing, or is Hollywood itself shifting how it tells stories? To tease this apart, I used a Blinder-Oaxaca decomposition to break down how much genres and networks each matter.

We decompose the change in flashback rates into three components:

* **Composition effect**: Holding flashback rates constant, how much of the change is due to shifts in what people watch (genre-network mix)?
* **Rate effect**: Holding what people watch (genre-network mix) constant, how much is due to the change in flashback usage within genres or networks?
* **Interaction effect**: The joint effect when both the mix and the rates change together. For example, streamers gaining share and showing more flashbacks.

The chart below is a visual breakdown of these different effects. The clear dominating factor is the interaction effect: certain networks and genres are gaining share and becoming more likely to show flashbacks. What’s interesting is that the network terms alone have negative effects, meaning it’s not simply that people are watching more streamers and that’s the sole cause.

<iframe src="../posts_images/2025-10-21-movie-analysis/interactive/flashback_decomposition_waterfall.html" width="100%" height="600px" frameborder="0"> </iframe>

# Summing it all up

Flashbacks really are on the rise and not just because of changes in what or where we’re watching. There’s something in the creative water. While I won’t try to psychoanalyze the culture’s new obsession, I (and every other TV addict) am watching to see if flashback fever will break, or if this is just the new normal.