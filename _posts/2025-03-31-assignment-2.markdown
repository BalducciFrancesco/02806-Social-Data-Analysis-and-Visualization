---
layout: post
title: "Assignment 2"
date:   2025-03-27 15:00:00 +0100
tags: assignment
---

> **TODO: add reference to [DAOST](https://www.oreilly.com/library/view/data-analysis-with/9781449389802) and to [Narrative Visualization: Telling Stories with Data](http://vis.stanford.edu/files/2010-Narrative-InfoVis.pdf)**

# Table of Contents

* Table of Contents  
{:toc}

# Context

This assignment is part of the [Social Data Analysis and Visualization course](https://kurser.dtu.dk/course/02806). The goal of the course is to teach us new techniques for exploring and visualizing raw datasets, as well as introducing some analytical tools. Full guidelines for the course can be found on [GitHub](https://github.com/suneman/socialdata2025).

# About the Dataset

The datasets used in this assignment can be easily accessed [here](https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-Historical-2003/tmnf-yvry/about_data) and [here](https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-2018-to-Present/wg3w-h783/about_data). They are .csv files where each row represents a crime reported by the San Francisco Police Department, with columns detailing information like the type of crime, its location, and more.

We merged the datasets using code since the first contains "historical" data (up to 2018) and the second includes "recent" data (from 2018 to the present). We also cleaned the data to standardize column names. The final dataset includes the following columns:

- Incident Category (e.g., homicide, fraud, etc.)
- Police District
- Resolution
- Latitude
- Longitude
- Incident Datetime

In total, there are **3,004,644** crimes recorded **from 2003 to 2024**, which we analyzed (and yes, it’s a depressing number).

# Goal of the Assignment

The purpose of this assignment is to bring together everything we've learned about data visualization. This includes using techniques for data exploration and effectively communicating findings, all while making the information accessible to a broad audience.

# Step-by-step

Here we go with the actual analysis. Brace yourselves!

One phenomenon that caught everyone’s attention is the **different behavior people seem to exhibit on weekends and at night**. Of course, we’re still talking about crimes, and alcohol and hanging out might play a significant role in this. Everything that follows aims to find evidence-backed explanations for this intuition.

To kick off our investigation, we used our *Python programming skills* to create a huge (and somewhat ugly) plot where, for *each crime category*, we displayed the number of crimes *per weekday* and *per hour range*. We're skipping this plot for the sake of brevity. As suggested in [Data Analysis with Open Source Tools (DAOST)](https://www.oreilly.com/library/view/data-analysis-with/9781449389802/), when presenting graphical analysis, we intentionally kept it quick to avoid any bias from spending too much time making it visually appealing.

> From now on, *"hour range"* will refer to the following daily time slots: 6-14, 14-22, and 22-6. We also decided to define "weekdays" as Monday through Thursday and "weekend" as Friday through Sunday.

At first glance, it was clear that most crimes occur more often at night than during the day, with not many showing a distinct peak over the weekend.

However, there were some surprises. For example, it might be surprising to learn that most drug offenses and prostitution were reported on Wednesdays, rather than on the weekend.

Returning to our goal, we observed that **assaults** and **malicious mischief** indeed occurred more frequently on weekends and at night. So, we created a specific plot to highlight these findings:

![Crime categories occurring more often in the weekend and at night](/assets/images/assignment2_plot1.png)

As seen in the plot, considering the entire data span, assaults rarely exceeded 30,000 during the weekdays, while on the weekend, they grew and almost reached 40,000 on Saturdays. The same pattern applies (with about 10,000 fewer daily occurrences overall) for malicious mischief, with the only difference being that Fridays had more occurrences than Sundays. A **clear preference for Saturdays and nighttime hours** seems to apply in both cases, suggesting that external factors like drinking or hanging out may play a role.

## Navigating San Francisco: Where to Go and What to Avoid  

It’s the weekend, and like most people, you’re ready to unwind and explore the city. Maybe you’re a family looking to relax in one of San Francisco’s beautiful parks, or a group of college friends excited for a night out at your favorite pub. The last thing on your mind? Crime.  

But what if you could know exactly where and when crime is most likely to happen? That’s exactly what we set out to uncover. By analyzing crime data of assaults and malicious mischief, which came out that have their peak during weekends, and visualizing it in a **Time Heat Map**, we reveal the city’s weekend crime, so you choose the safest places to enjoy your time. 

<iframe src="/assets/sources/sf_heatmap.html" width="800" height="300" frameBorder=0></iframe>

This interactive map allows you to explore crime trends across the city and different time periods. We grouped the data into three-hour intervals, covering the period **from Friday at 6 PM to Sunday at midnight**. Now let's have a look 

### **If You’re a Family Looking for Green Spaces**  
Good news! Most parks are safe havens. Whether you’re planning a picnic or letting the kids play, you generally have little to worry about. That said, **Golden Gate Park** does show a slight uptick in assaults during the afternoon (3–6 PM). This could be due to its big size and popularity, but compared to other areas, it remains relatively safe.  

### **If You’re Exploring San Francisco’s Nightlife**  
If you’re searching for a pub or club, things get trickier. On Saturday night (9 PM–midnight), much of the city center turns red, indicating a high concentration of crime. But don’t worry, there are still safer areas to enjoy.  

- **Tenderloin: A No-Go Zone**  
  Despite its many clubs, theaters, and bars near Union Square, it remains one of the city’s **most dangerous areas**. It’s no secret that the Tenderloin has a bad reputation, and the heat map confirms it. Nearly every street in this neighborhood turns red on Saturday night (9 PM–midnight), indicating high crime levels. As [Wikipedia](https://en.wikipedia.org/wiki/Tenderloin,_San_Francisco#Crime) puts it, this neighborhood has *particularly violent street crime such as robbery and aggravated assault*.  

- **11th Street: Fun but Risky**  
  Located between the **SOMA and Mission** neighborhoods, **11th Street** is home to some of the city’s [most popular clubs](https://www.yelp.com/search?cflt=danceclubs&find_loc=11th+St%2C+San+Francisco%2C+CA+94103). The heat map suggests that while not as dangerous as the Tenderloin, it still has a noticeable crime presence, so stay aware of your surroundings. 

- **🍻 Richmond & Presidio: A Safer Alternative**  
  How about enjoying a **laid-back night with craft beers** in a safer setting? Head to **Richmond or Presidio**. These neighborhoods are home to some of San Francisco’s best [microbreweries](https://www.sftravel.com/article/san-francisco-nightlife-neighborhood) and show **significantly lower crime rates** compared to downtown nightlife districts.  

# Bukeh plot
This plot shows the average 
<iframe src="/assets/images/crime_patterns_by_day.html" width="1000" height="600"></iframe>