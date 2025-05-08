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
Recently, a [bright blue spiral appeared](https://www.bbc.com/news/articles/c241073v66jo) in the European skies, capturing the attention of countless onlookers. The unusual sight left many people staring upward in wonder. In this case, an explanation was provided relatively quickly: it was caused by fuel burning during a rocket launch. However, at the moment it occurred, no one could be sure of what they were seeing. Social media quickly lit up with speculation—ranging from scientific theories to claims of UFO activity.

This raises an interesting question: what is the current state of UFO sightings? How has the phenomenon evolved from early reports to the age of the internet?

Today, UFOs remain a hot topic, polarizing public opinion. On one side are passionate believers, convinced of extraterrestrial visitation; on the other are skeptics and debunkers, who often attribute sightings to optical illusions, atmospheric phenomena, or psychological factors. With this in mind, we aim to explore and analyze the UFO phenomenon using our own tools and perspective.

In this article, we do not aim to take sides in the ongoing debate. Instead, our goal is to present perspectives from both believers and skeptics, while conducting our own analysis of the data. To that end, we turn to the extensive database maintained by the National UFO Reporting Center (NUFORC), which contains hundreds of thousands of reports from around the world. By examining this rich source of information, we aim to highlight some of the most intriguing patterns and anomalies we uncovered. Curious about what we found? Let’s begin.
In this article we don't want to take one side of the argument, but rather we want to tell the story from both sides and doing our own analysis. For this goal we will analyze the  data, it's an incredible dataset that contains hundreds of thousands of sigthings, from all over the world, summing up the most curious thing that we found during our analysis. Are you curious about this? Let's start!
# Further reading

Due to the intended audience, in this article we're **omitting** some of the exquisitely technical topics and their details. 

If you're interested in knowing more about the **tools** and the **reasoning** behind some of the charts that will follow, we encourage you to read more in the [source notebook](https://github.com/BalducciFrancesco/02806-Social-Data-Analysis-and-Visualization/blob/master/assets/sources/final-project.ipynb).

# Step-by-step

## Part 1 - Knowing the database

We begin by examining the number of UFO sightings reported over the years. In the first chart, you can observe how sightings have evolved, with a clear upward trend. The red cross line marks the launch of the NUFORC website, a key moment in the visibility and accessibility of reporting. Reliable data begins in the 1950s, followed by a relatively stable period between 1965 and 1990, during which reports averaged around 300 per year.

With the advent of the internet, however, the number of sightings increased significantly, peaking in 2014 with nearly 10,000 reports in a single year. This sharp rise suggests that many sightings previously went unreported for lack of a convenient platform. Actually, even in the internet era, most reports are submitted an average of 20 days after the event, indicating that delays in reporting remain common.


## Part 2 – Emotional analysis

We all know *how* **passionate** is the public opinion about those who state to have seen a UFO. The question we want to answer is: yes, *how much*? 

In this section we're going to focus on a **specific aspect** of the UFO sighting: the numbers around **emotions** of those who claim to have experienced them. In other words, we decided to use the **tools** available to us through this course to extract and visualize *one of the biggest factors* that influence this phenomenon.

The reason? Emotions are often where **objectivity breaks down** — and that’s exactly why they’re interesting to study. They represent the human part of the experience, where logic gets blurred and interpretations take over. It's also the part where most discussions — and disagreements — begin, and where **pseudo-scientific narratives** often find their ground.

Since our dataset contains the **full text** written by the people, we attempted to use a mix of **machine learning** techniques to automatically analyze these texts and **extract the corresponding emotion**. Some of the most used yet simple techniques involve applying statistics to estimate the overall "positive" or "negative" tone of each word, or how strongly it *points* to a specific emotion. Considering the *several hundred thousand* records, we decided to opt for a **cherry-picking** approach — selecting some key terms that clearly reference an emotion (e.g. *thrilled*, *excited* → *joy*) — and flagging their presence for each record.

### The importance of words

The theory will certainly sound *interesting* (read: boring), but now it’s time to dive into the actual data. As we mentioned earlier, every analysis that will follow is based on the **words people used** and the **emotion tied to them**. So, it only makes sense to start by looking at the most common ones.

Below, you’ll find a so-called *word cloud* — a simple way to show the most frequent words, where the **size** of each word reflects how often it appears in the dataset. Let’s take a look!

![Most occurring words]({{ site.baseurl }}/assets/images/fp_most_occurring_words.png){: width="400" }{:.centered}

Unsurprisingly, the **top** words include **light**, **fast**, **moving**, and **bright** — which makes sense given that most reports focus on describing what was seen in vivid, physical detail.

Digging a bit deeper, we also found some **less frequent** but curious terms like **airplane**, likely used when trying to make sense of the object; **drive**, perhaps reflecting how often people spot UFOs while on the road; and **girlfriend**, oddly enough one of the most frequently mentioned witnesses of sightings.

### How many emotions

Nice, now we know which words they have used but *when do the numbers come*?!?! We will now show you how **frequent** each emotion is — nothing more, nothing less. 

We would be very *happy* if you could appreciate (and keep in mind) the **color coding**, since you will see it used consistently in the following charts and it will may be of help for you to follow each emotion more easily.

![Number of sightings by Emotion]({{ site.baseurl }}/assets/images/fp_sightings_by_emotion.png){: width="500" }{:.centered}

The chart clearly shows that *Confused* is the **most frequent** emotion, with almost 8000 reports. Right after, we find *Scared*, *Curious*, and *Surprised*, each appearing less often but with a **gradual drop**, like steps in a staircase. *Joy* follows closely behind *Surprised*, both reaching around 3300 entries. At the bottom of the ranking, *Sad* stands out for its **low occurrence**, with only 833 matches across the dataset.

### Rollercoaster of emotions

Cool, but now we would like to know whether the emotions **throughout the years** are going up or down! Is any emotion showing a similar trend to another? Or maybe diverging completely? Could there be a correlation hidden in the way these emotions evolve over time? Let’s check it out!

![Number of sightings by Years]({{ site.baseurl }}/assets/images/fp_sightings_by_emotion_years.png){: width="750" }{:.centered}

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

![Scared emotion projection over Years]({{ site.baseurl }}/assets/images/fp_scared_years_projection.png){: width="800" }{:.centered}

Yes, it's a long timespan. But as you can see by fitted curve, it suggests that the frightening effect of sightings might fade away by **2040**!. That’s a spark of hope — we’ll keep you posted when we get there.

### Carpe diem

Emotion sometimes may be fooling us. They may **alter** our perception of **time**, making it never ending or quick as a glimpse. Therefore, we want to see whether the emotion associated to the UFO sightings may have influenced the reported time of it.

Be careful! The plot you're about to see is called a *boxplot* but don't get scared: the **box** shows where most of the durations fall, the **line** in the middle is the typical (*median*) duration, the **whiskers** give an idea of the spread, and the **dots** represent unusually short or long sightings (*outliers*).

![Duration of the sighting by Emotion]({{ site.baseurl }}/assets/images/fp_sightings_by_emotion_duration.png){: width="750" }{:.centered}

Woah, hope you're still with us after that! 

For most reports, durations sit somewhere between **a few seconds and 15 minutes**. The **longest** average durations come from *Scared*: just look at how its **box** sits visibly further right than the others. On the flip side, *Confused* and *Joy* cluster tightly near the start of the axis, hinting that these emotions are more **shorter-lived**.

Now for the so-called **whiskers**: *Curious* (and a few others) has long ones, showing **big variation** in how long these sightings last. *Confused* and *Joy* again stick to **shorter whiskers** — pretty consistent and quick.

Lastly, the **outliers**: *Confused* shows quite a few dots past the right whisker — **rare** but long events that stand very out from the usual. Most sightings are short, but occasionally something lasts way longer and clearly leaves people puzzled.

### The Imperial March

If there's one thing that may influence people's opinions, it's **movies**. You know where we're going with this. Yes, we looked into how many times the word "movie" was **mentioned** in our dataset — and it showed up **1630** times! And that’s only counting the *direct* references.

We went further: read through those comments, checked which titles were most mentioned, and also looked online to identify blockbuster movies about UFOs. That gave us a list of **16 key titles**. Here are the most frequent ones:

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

![Star wars occurance in sightings by Years]({{ site.baseurl }}/assets/images/fp_sightings_by_star_wars_years.png){: width="750" }{:.centered}

Aside from the first two films (they were great), the number of sightings clearly **spikes** around the **release** of new Star Wars movies. Just look at the stretch from 2014 to 2020 — **three major releases and three sharp increases in reports**. Coincidence? We'll never know. But given how often the saga is mentioned in the comments, it’s fascinating to see how often people have **linked** their sightings to the most recent Star Wars release — almost like the movie gives them a cue to describe what they saw.

One thing to keep in mind: we’re looking at the *date of the sighting*, not when the report was posted. That’s why you’ll see Star Wars references even before the original 1977 release — some people report older experiences years later. Or maybe they were UFOs and have had the technology to predict the saga releases.

### Wrapping up

So, what did we learn? **A lot**. And also... *not much*.  

We saw that **emotions** play a major role in how people report UFO sightings — from the *confused* and *scared*, to the *curious* and oddly *joyful*. We tracked how these feelings evolved **over time**, spiked in 2012, got tangled with **movies**, and maybe, just maybe, are becoming **less intense** as the years go by.  

However, before jumping to any **conclusions**, it's important to highlight that our findings **cannot be considered conclusive**. We selected key terms, applied parsimonious models, and worked with **user-submitted reports**, which means there are **different biases** in both the data collection and interpretation. Our analysis offers an *inherently* partial view, the methods we used have limitations, and emotions are — by nature — complex and subjective.

Still, this was ***fun***. 

We used what we learned to do **data mining**, build **visualizations**, tell a **story** and maybe understand a little more about why people see what they see — or at least why they **feel** the way they do when they see it. 

And maybe that’s the point: not to conclude *if* UFOs exist, but to explore **what they mean** to the people who experience them.

Thanks for following us on this emotional rollercoaster through the unknown. See you on the next sighting 👽  


# Part 3
While UFO sightings may feel intense and scary, my analysis takes a data driven approach to look into possible explanations of the sightings. By examining correlations with external factors, such as extreme weather conditions, I explore whether these sightings might be better explained by natural phenomena rather than extraterrestrial activity. 
To investigate whether natural phenomena could explain some of the reported UFO sightings, I chose to explore the influence of severe weather events. For this, I used storm event data from NOAA’s Storm Events Database (1950–2024), which includes categorized events such as thunderstorms, hail, and high wind, along with geographic and temporal information. Since the UFO dataset ends in 2013, I limited the weather data to the years 1960–2013 and cleaned it by removing rows with missing values in key fields like location and date, leaving us with 751,321 entries. I also excluded long duration events like drought and heat, as they were less likely to be relevant to sudden sightings and would have distorted the analysis.

To explore whether extreme weather events might influence the number of reported UFO sightings, we narrowed our focus to the top 10 most frequent weather types in the U.S. storm event dataset, excluding 'Heat' and 'Drought' due to their long duration and low relevance to sudden visual anomalies.

Let’s start by looking at the subplot below, which visualizes UFO sightings in the 16 U.S. states with the highest number of reports. The bars show the total number of sightings during extreme weather events, with red indicating sightings that occurred without any such events. As seen, there is considerable variation between states. The most common weather types associated with sightings are hail, thunderstorms, and high wind, conditions that could easily disturb or obscure visual overview. For instance, strong winds may lift debris or objects into the sky, while heavy snow, fog, or rain can reduce visibility, increasing the chance of misinterpretation.

Interestingly, some states show a relatively higher proportion of sightings during extreme weather; Colorado, Texas, Illinois, and Missouri, while others, like Oregon, Washington, Arizona, and New Jersey, have most sightings reported in calm weather.

This contrast could partly be explained by regional weather patterns. States like Colorado, Texas, and Missouri are known for dramatic and fast-changing weather, including thunderstorms, tornadoes, and strong winds. These weather patterns may increase the chance of misinterpreting natural events as UFOs. Illinois, also sees varied weather and has large urban areas with lots of air traffic, which could add to visual confusion.

On the other hand, Oregon and Washington (Pacific Northwest) are known for frequent cloud cover and rain, but not necessarily for dramatic weather events, but both states have a long history of UFO interest. Washington, for instance, was the site of one of the first major modern UFO sightings in 1947 (the "Kenneth Arnold sighting"). Arizona is famously home to the 1997 “Phoenix Lights” incident, one of the most widely reported UFO sightings in U.S. history. New Jersey, while more urban, is close to New York and has a high population density, which may lead to more overall reports simply due to the number of people.

Taken together, these patterns suggest that both environmental and cultural factors influence UFO sighting trends. States with more extreme weather may generate more UFO reports during storms due to natural misinterpretations, while states with strong UFO-related histories or high public interest might see more reports in general, regardless of the weather.

![Subplot UFO correlating with extreme weather]({{ site.baseurl }}/assets/images/subplots.png)

Across all states, we observe that 66.2% of UFO sightings occur during some form of weather event, with the most frequent being thunderstorms and hail, as shown in the figure. The high number of sightings during thunderstorms (46,981 reports) raises the possibility that lightning, unusual cloud formations, or electrical disturbances could be mistaken for UFOs. Similarly, during hailstorms, people may be on high alert due to the dramatic atmosphere and may be more likely to notice and report strange phenomena. It's also worth noting that thunder and lightning can distort perception, especially at night, causing aircraft lights, reflections, or weather balloons to appear strange. So, while not everyone may literally mistake thunder for a UFO, it's plausible that the sensory overload and visual confusion of storms create a perfect storm for UFO misidentifications.

![UFO correlating with extreme weather]({{ site.baseurl }}/assets/images/all_states.png)

# Contributions

This goes in the Jupyter only?
