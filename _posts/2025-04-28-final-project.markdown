---
layout: post
title: "Final project"
date:   2025-04-28 12:00:00 +0100
tags: final_project
---

# Table of Contents

* Table of Contents  
{:toc}

# Mystery in the Sky: Blue Spiral Sparks UFO Debate

<iframe height="450" src="https://www.youtube.com/embed/nI4G8Br79sQ?si=--CpABgxoLOkeRiB" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>{:.centered}

&nbsp;

This raises an interesting question: what is the current state of UFO sightings? How has the phenomenon evolved from early reports to the age of the internet?

Today, UFOs remain a hot topic, polarizing public opinion. On one side are passionate believers, convinced of extraterrestrial visitation; on the other are skeptics and debunkers, who often attribute sightings to optical illusions, atmospheric phenomena, or psychological factors. With this in mind, we aim to explore and analyze the UFO phenomenon using our own tools and perspective.

In this article, we do not aim to take sides in the ongoing debate. Instead, our goal is to present perspectives from both believers and skeptics, while conducting our own analysis of the data. To that end, we turn to the extensive database maintained by the National UFO Reporting Center (NUFORC), which contains hundreds of thousands of reports from around the world. By examining this rich source of information, we aim to highlight some of the most intriguing patterns and anomalies we uncovered. Curious about what we found? Let’s begin.
In this article we don't want to take one side of the argument, but rather we want to tell the story from both sides and doing our own analysis. For this goal we will analyze the  data, it's an incredible dataset that contains hundreds of thousands of sigthings, from all over the world, summing up the most curious thing that we found during our analysis. Are you curious about this? Let's start!

# Further reading

Due to the intended audience, in this article we're **omitting** some of the exquisitely technical topics and their details. 

If you're interested in knowing more about the **tools** and the **reasoning** behind some of the charts that will follow, we encourage you to read more in the [source notebook](https://github.com/BalducciFrancesco/02806-Social-Data-Analysis-and-Visualization/blob/master/assets/sources/final-project_technical.ipynb).

# Step-by-step

## Part 1 – Knowing the database

We begin by examining the number of UFO sightings reported over the years. In the first chart, you can observe how sightings have evolved, with a clear upward trend. The red cross line marks the launch of the NUFORC website, a key moment in the visibility and accessibility of reporting. Reliable data begins in the 1950s, followed by a relatively stable period between 1965 and 1990, during which reports averaged around 300 per year.

![Total sightings]({{ site.baseurl }}/assets/images/total_sightings.png){: width="700" }{:.centered}

With the advent of the internet, however, the number of sightings increased significantly, peaking in 2014 with nearly 10 000 reports in a single year. This sharp rise suggests that many sightings previously went unreported for lack of a convenient platform. Actually, even in the internet era, most reports are submitted an average of 20 days after the event, indicating that delays in reporting remain common.

To provide a clearer picture of where these sightings occur, we created an interactive world map highlighting major UFO hotspots. You can explore the map freely to examine sightings by location. While the dataset does not cover every region—possibly due to the use of other reporting platforms in certain countries—it still includes reports from every continent.

<iframe src="{{ site.baseurl }}/assets/templates/ufo_heatmap.html" frameborder="0" style="width: 100%; height: 500px"></iframe>{:.centered}

A closer look reveals that the distribution of sightings closely follows global population patterns, with a significant concentration in major U.S. cities. Interestingly, locations often associated with UFO lore—such as Area 51 in southern Nevada—do not show particularly dense clusters of reported activity, challenging some popular assumptions.

Next, we focused on the temporal patterns of sightings, analyzing whether they are evenly distributed across the year and throughout the day. 

![Month distribution]({{ site.baseurl }}/assets/images/month_distribution.png){:.centered}
![Hour distribution]({{ site.baseurl }}/assets/images/hour_distribution.png){:.centered}

The data shows a clear imbalance. As illustrated in the following two charts, there is a noticeable increase in sightings during the summer months and a decline during the winter. 
The distribution by hour of the day is even more concentrated: most sightings are reported between 8:00 p.m. and 11:00 p.m.

## Part 2 – Emotional analysis

We all know *how* **passionate** is the public opinion about those who state to have seen a UFO. The question we want to answer is: yes, *how much*? 

In this section we're going to focus on a **specific aspect** of the UFO sighting: the numbers around **emotions** of those who claim to have experienced them. In other words, we decided to use the **tools** available to us through this course to extract and visualize *one of the biggest factors* that influence this phenomenon.

The reason? Emotions are often where **objectivity breaks down** — and that’s exactly why they’re interesting to study. They represent the human part of the experience, where logic gets blurred and interpretations take over. It's also the part where most discussions — and disagreements — begin, and where **pseudo-scientific narratives** often find their ground.

Since our dataset contains the **full text** written by the people, we attempted to use a mix of **machine learning** techniques to automatically analyze these texts and **extract the corresponding emotion**. Some of the most used yet simple techniques involve applying statistics to estimate the overall "positive" or "negative" tone of each word, or how strongly it *points* to a specific emotion. Considering the *several hundred thousand* records, we decided to opt for a **cherry-picking** approach — selecting some key terms that clearly reference an emotion (e.g. *thrilled*, *excited* → *joy*) — and flagging their presence for each record.

### The importance of words

The theory will certainly sound *interesting* (read: boring), but now it’s time to dive into the actual data. As we mentioned earlier, every analysis that will follow is based on the **words people used** and the **emotion tied to them**. So, it only makes sense to start by looking at the most common ones.

Below, you’ll find a so-called *word cloud* — a simple way to show the most frequent words, where the **size** of each word reflects how often it appears in the dataset. Let’s take a look!

![Most occurring words]({{ site.baseurl }}/assets/images/fp_most_occurring_words.png){:.centered-small}

Unsurprisingly, the **top** words include **light**, **fast**, **moving**, and **bright** — which makes sense given that most reports focus on describing what was seen in vivid, physical detail.

Digging a bit deeper, we also found some **less frequent** but curious terms like **airplane**, likely used when trying to make sense of the object; **drive**, perhaps reflecting how often people spot UFOs while on the road; and **girlfriend**, oddly enough one of the most frequently mentioned witnesses of sightings.

### How many emotions

Nice, now we know which words they have used but *when do the numbers come*?!?! We will now show you how **frequent** each emotion is — nothing more, nothing less. 

We would be very *happy* if you could appreciate (and keep in mind) the **color coding**, since you will see it used consistently in the following charts and it will may be of help for you to follow each emotion more easily.

![Number of sightings by Emotion]({{ site.baseurl }}/assets/images/fp_sightings_by_emotion.png){:.centered-small}

The chart clearly shows that *Confused* is the **most frequent** emotion, with almost 8000 reports. Right after, we find *Scared*, *Curious*, and *Surprised*, each appearing less often but with a **gradual drop**, like steps in a staircase. *Joy* follows closely behind *Surprised*, both reaching around 3300 entries. At the bottom of the ranking, *Sad* stands out for its **low occurrence**, with only 833 matches across the dataset.

### Rollercoaster of emotions

Cool, but now we would like to know whether the emotions **throughout the years** are going up or down! Is any emotion showing a similar trend to another? Or maybe diverging completely? Could there be a correlation hidden in the way these emotions evolve over time? Let’s check it out!

![Number of sightings by Years]({{ site.baseurl }}/assets/images/fp_sightings_by_emotion_years.png){:.centered}

Most emotions show a noticeable **rise after 2000**, which we might consider linked to the popularity of **social media** and the growing accessibility of the platform we got the data from, [NUFORC](https://nuforc.org/about-us/), active on **Internet** since 1995. Interestingly, they all **peaked in 2012** before **dropping** off — a phenomenon that even made it into the [news](https://www.huffpost.com/entry/american-ufo-reports-down_b_2982532), though the reasons behind it are still unclear.

*Scared* dominates the period from 1940 to 2000, consistently being the top emotion. Oddly enough, in 1969 and 1980, there were **no reported sightings** tagged as *Sad*, making them rare outliers in an otherwise continuous (and low) trend.

### The same but funnier!

All good, but I can see your struggle comparing all the plots. Fear not – *unlike you would if you saw an UFO* — we got you covered with a nice plot where we **strongly encourage** you to click around. 

In the next panel, each line represents the **trend of an emotion**, giving you a clearer sense of the magnitude differences between them. You’re free to **toggle** any emotion on or off by simply **clicking** its name in the legend. You can also **zoom in, pan around**, or use the **range slider** at the bottom for quicker navigation. Have fun exploring — we’ll catch up with you right after!

<iframe src="{{ site.baseurl }}/assets/templates/fp_sightings_by_emotion_years.html" frameborder="0" style="height: 450px; width: 100%; min-width: 800px"></iframe>

As mentioned earlier, the chart immediately draws attention to a **sharp spike** in all emotions in 2012, followed by a noticeable **drop**. Starting from 1995, emotional reactions began to somewhat **diversify** and spread around.

No surprises ahead: *Confused* dominates the scene, peaking in 2008 and again in 2012 — it seems most people walk away from a sighting feeling more **baffled** than anything else. Meanwhile, *Sad* keeps a **low but steady** profile, never making waves but always present.

Some drama unfolds between *Surprised* and *Curious*: the first takes the lead in 2018, only to be overtaken again by the second in 2020 — maybe reflecting a subtle change in how people **frame their encounters**. 

That being said, *Curious* best friend is arguably *Scared* as they move most of the time in **lockstep**, almost mirroring each other over time. Though neither steals the show to the other, their similarity suggests these emotions might be as likely to happen as the other, never deviating too much.

### Will we ever get accustomed to *them*?

We know (or do we?) that seeing a UFO can be quite the **unsettling** experience. We've been proven to be increasingly brave by the previous plots, so we asked ourselves: will the *Scared* trend ever come to an end? To get an answer, we put our skills to work and *automagically* trained a model using the past data — pushing it forward in time to see where things might be headed.

![Scared emotion projection over Years]({{ site.baseurl }}/assets/images/fp_scared_years_projection.png){:.centered}

Yes, it's a long timespan. But as you can see by fitted curve, it suggests that the frightening effect of sightings might fade away by **2040**!. That’s a spark of hope — we’ll keep you posted when we get there.

### Carpe diem

Emotion sometimes may be fooling us. They may **alter** our perception of **time**, making it never ending or quick as a glimpse. Therefore, we want to see whether the emotion associated to the UFO sightings may have influenced the reported time of it.

Be careful! The plot you're about to see is called a *boxplot* but don't get scared: the **box** shows where most of the durations fall, the **line** in the middle is the typical (*median*) duration, the **whiskers** give an idea of the spread, and the **dots** represent unusually short or long sightings (*outliers*).

![Duration of the sighting by Emotion]({{ site.baseurl }}/assets/images/fp_sightings_by_emotion_duration.png){:.centered}

Woah, hope you're still with us after that! 

For most reports, durations sit somewhere between **a few seconds and 15 minutes**. The **longest** average durations come from *Scared*: just look at how its **box** sits visibly further right than the others. On the flip side, *Confused* and *Joy* cluster tightly near the start of the axis, hinting that these emotions are more **shorter-lived**.

Now for the so-called **whiskers**: *Curious* (and a few others) has long ones, showing **big variation** in how long these sightings last. *Confused* and *Joy* again stick to **shorter whiskers** — pretty consistent and quick.

Lastly, the **outliers**: *Confused* shows quite a few dots past the right whisker — **rare** but long events that stand very out from the usual. Most sightings are short, but occasionally something lasts way longer and clearly leaves people puzzled.

## Part 3 - What is really going on?
While UFO sightings may feel intense and scary, our analysis takes a data driven approach to look into possible explanations of the sightings. By examining correlations with external factors, such as extreme weather conditions, we explore whether these sightings might be better explained by natural phenomena rather than extraterrestrial activity. 

### Can bad weather be mistaken for UFOs?
To explore whether extreme weather events might contribute to the frequency of UFO sightings, we analyzed storm event data from NOAA (1960–2013) alongside UFO sighting reports in the U.S. We focused on severe weather events like thunderstorms, hail, and high winds, excluding less relevant long-duration events like heat and drought.

Our analysis reveals considerable regional variation in UFO sightings during extreme weather. States like Colorado, Texas, and Missouri, with fast-changing weather patterns, report more sightings during storms, possibly due to visual confusion from weather disturbances. In contrast, areas like Oregon and New Jersey, with strong UFO histories, have more sightings in calm conditions, indicating cultural factors might also play a role. Overall, both weather and cultural factors influence UFO sighting trends, suggesting that extreme weather could cause misinterpretations of natural phenomena as UFOs.

![Subplot UFO correlating with extreme weather]({{ site.baseurl }}/assets/images/subplots.png){:.centered}

Across all states, we observe that 66.2% of UFO sightings occur during some form of weather event, with the most frequent being thunderstorms and hail, as shown in the figure. The high number of sightings during thunderstorms (46,981 reports) raises the possibility that lightning or unusual cloud formations could be mistaken for UFOs. Similarly, during hailstorms, people may be on high alert due to the dramatic atmosphere and may be more likely to notice and report strange phenomena. It's also worth noting that thunder and lightning can distort perception, especially at night, causing aircraft lights, reflections, or weather balloons to appear strange. So, while not everyone may literally mistake thunder for a UFO, it's plausible that the sensory overload and visual confusion of storms create a perfect storm for UFO misidentifications.

![UFO correlating with extreme weather]({{ site.baseurl }}/assets/images/all_states.png){:.centered}

### Does popculture and news affect the amount of UFOs reported? 

Beyond weather and natural explanations, media coverage and pop culture appear to play a role in shaping public perception—and potentially even the number of UFO sightings reported. Since the first major sighting in 1947, UFOs have captured the public imagination through news headlines, blockbuster films, and TV shows. From The X-Files to Pentagon disclosures, these events don't just reflect interest in UFOs, they may also amplify it, prompting spikes in sightings. The timeline below highlights major media and cultural moments related to UFOs, which we can explore to see if they coincide with increases in reported activity.

When we look at the data, we notice a clear pattern, reported UFO sightings often spike around major media events. In many cases, the number of sightings increases shortly after the release of a new UFO-related film, TV show, or news story. Interestingly, we also observe that sightings sometimes rise just before these releases—perhaps due to pre-release hype. In 1997 Phoenix Lights incident, we see a dramatic increase in reports, especially visible in the 7-day averages. Of course, not all spikes align with media events; holidays like New Year’s Eve and Independence Day often show elevated sightings too—likely due to fireworks or extreme weather events as previouesly discussed. While many spikes fade after a short burst, something changed after the launch of the Pentagon’s UFO program in 2007, since then, we’ve seen a more sustained rise in reports, suggesting that long-term media and government attention might be keeping the topic alive in the public mind.

<iframe src="{{ site.baseurl }}/assets/templates/ufo_timeline.html" frameborder="0" style="width: 100%; height: 550px"></iframe>{:.centered}

#### The Imperial March

We went further: read through the *comments* people made, checked which titles were most mentioned, and also looked online to identify blockbuster movies about UFOs. That gave us a list of **16 key titles**. Here are the most frequent ones:

| **Movie**             | **Count**  |
| Star Trek (1979)	| 183 |
| Star Wars (1977)	| 163 |
| Predator (1987)	| 81 |
| Independence Day (1996)	| 67 |
| Close Encounters of the Third Kind (1977)	| 37 |
| X-Files (1998)	| 37 |
| War of the Worlds (2005)	| 24 |
| Interstellar (2014)	| 17 |
| E.T. (1982)	| 15 |
| Twister (1996)	| 6 |
| Deep impact (1998)	| 4 |
| Armageddon (1998)	| 3 |
| The Day the Earth Stood Still (1951)	| 2 |
| A scene out of a Spielberg movie (?)	| 1 |
| Old movie of the UFOs in Montana in the late forties (1950)	| 1 |
| UFO Unplugged (1997)	| 1 |

That's impressive, to say the least. Considering our passion for **Star Wars** (sorry Star Trek fans, we're a bit biased), we didn’t think twice before diving deeper into that one. So we used a diagram you’re probably very familiar with by now — the **barplot** — to see if there’s any **correlation** between the **number** of sightings reported in a given year and the **release of a Star Wars movie**:

![Star wars occurance in sightings by Years]({{ site.baseurl }}/assets/images/fp_sightings_by_star_wars_years.png){:.centered}

Aside from the first two films (they were great), the number of sightings clearly **spikes** around the **release** of new Star Wars movies. Just look at the stretch from 2014 to 2020 — **three major releases and three sharp increases in reports**. Coincidence? We'll never know. But given how often the saga is mentioned in the comments, it’s fascinating to see how often people have **linked** their sightings to the most recent Star Wars release — almost like the movie gives them a cue to describe what they saw.

One thing to keep in mind: we’re looking at the *date of the sighting*, not when the report was posted. That’s why you’ll see Star Wars references even before the original 1977 release — some people report older experiences years later. Or maybe they were UFOs and have had the technology to predict the saga releases. 

### Do more people mean more UFOs?

When we compare UFO sightings across U.S. states, we see a clear trend, sightings tend to follow population density. In the blue choropleth map showing total UFO reports by state, the states with the highest counts are California, Texas, Florida, and New York—exactly what we’d expect given their large populations. This becomes even more apparent when we look at the second map, which shows population by state. The correlation is clear: more people means more potential observers, and therefore more UFO reports. This reinforces the idea that UFO sightings aren’t randomly distributed, but largely reflect where people live.

<iframe src="{{ site.baseurl }}/assets/templates/combined_ufo_population_maps.html" frameborder="0" style="width: 100%; height: 500px"></iframe>{:.centered}

To dig deeper than population numbers, we built a linear regression model to predict the number of sightings each state should have based on its population. This gave us a baseline: how many UFO reports we would expect if sightings followed population perfectly. We then calculated the residuals, i.e. the difference between actual and expected sightings, and visualized them on a choropleth map.

The map highlights where states deviate from the population-based expectation. Positive values (in blue) show more sightings than predicted, while negative values (in red) show fewer.

We see that Washington, Oregon, California, and Arizona all report more sightings than expected, whereas states like Texas, Georgia, and New York report fewer. These deviations might reflect differences in culture, visibility, or reporting habits. For instance, Washington has deep roots in UFO history, the term “flying saucer” was coined after a 1947 sighting there. Likewise, Arizona and Oregon are known for their UFO-watching communities. On the other hand, more urbanized or conservative states like Texas and Georgia might either see fewer unexplained phenomena or report them less often.

<iframe src="{{ site.baseurl }}/assets/templates/ufo_sightings_residuals.html" frameborder="0" style="width: 100%; height: 500px"></iframe>{:.centered}

Our analysis shows that extreme weather events, such as thunderstorms and hail, are closely linked to UFO sightings, likely due to visual misinterpretations caused by weather disturbances. Additionally, cultural factors and media coverage significantly influence the frequency of sightings, with reports often spiking around major UFO-related events. Finally, population density plays a role, with more populated states seeing more sightings. Together, these factors suggest that natural, social, and cultural influences all contribute to the reported UFO phenomenon.

## So that's it? UFOs don't exist?

On the other hand, the dataset reveals several details that may seem surprising to those with a stereotypical view of UFO sightings. As highlighted earlier, the distribution of reports does not center around iconic or conspiracy-linked locations, but rather follows population density, with most sightings occurring in large urban areas. This makes sense: where more people are present, there are simply more eyes on the sky—and more chances for unusual events to be noticed and reported.

The resulting portrait of UFO witnesses contrasts with the popular image of dedicated skywatchers or “Ghostbusters of the skies,” armed with cameras and special equipment. Instead, most reports come from ordinary people living in cities, simply recounting what they experienced.


Pursuing this line of reasoning, we conducted a detailed analysis of the temporal sequence of sightings and arrived at a surprising result: there appears to be no temporal correlation between them. In other words, if a sighting is reported in a particular location, our analysis suggests it does not lead to an increase in subsequent reports from the same area.

This finding can be interpreted in two ways. On one hand, it reinforces the idea that there is no tightly connected community consistently reporting from suspected hotspots of alien activity. On the other hand, it raises questions. If an unidentified object were to appear in the skies above a city, it would be reasonable to expect that many people would see it—resulting in a cluster of reports from the same time and place. Yet, the data does not reflect this pattern.

In addition, the database maintainers appear to be well aware of the potential for errors or misinterpretations in UFO reports. We observed a high level of diligence in addressing this issue. The site explicitly lists common explanations for sightings—such as rocket launches, bright planets, and camera artifacts—and notes that it reviews reports for signs of hoaxes or jokes. This level of oversight helps ensure that simplistic or easily debunked explanations are filtered out, lending greater credibility to the dataset as a whole.

# Wrapping up

So, what did we learn? **A lot**. And also... *not much*.  

We saw that **emotions** play a major role in how people report UFO sightings — from the *confused* and *scared*, to the *curious* and oddly *joyful*. We tracked how these feelings evolved **over time**, spiked in 2012, got tangled with **movies**, and maybe, just maybe, are becoming **less intense** as the years go by.  

However, before jumping to any **conclusions**, it's important to highlight that our findings **cannot be considered conclusive**. We selected key terms, applied parsimonious models, and worked with **user-submitted reports**, which means there are **different biases** in both the data collection and interpretation. Our analysis offers an *inherently* partial view, the methods we used have limitations, and emotions are — by nature — complex and subjective.

Still, this was ***fun***. 

We used what we learned to do **data mining**, build **visualizations**, tell a **story** and maybe understand a little more about why people see what they see — or at least why they **feel** the way they do when they see it. 

And maybe that’s the point: not to conclude *if* UFOs exist, but to explore **what they mean** to the people who experience them.

Thanks for following us on this emotional rollercoaster through the unknown. See you on the next sighting 👽 
