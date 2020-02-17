---
layout: post
title:      "Exploratory Data Analysis as an Artform for Expressing Business Insights"
date:       2020-02-16 19:49:30 -0500
permalink:  exploratory_data_analysis_as_an_artform_for_expressing_business_insights
---


Business understanding is often cited as the first component of the Data Science Lifecycle. It is in this initial discovery that the Data Scientist or Analyst will communicate with their client, or themselves to ascertain the goals and methodology of the work being done. Questions, many questions must be asked about what ultimate problem is being solved, or what final question is being answered. What kind of data would be needed to acheive this goal. If it is avaliable, where is it housed, and if it is not available how can it be created. After acquiring the data and cleaning it, it is time to explore the data. Here one looks for insights in visualizations that can answer those first questions posed in the business understanding stage.

Exploratory data analysis is at its core an act of expression. Plots rendered by popular libraries such as `matplotlib` and `seaborn` have been created by transmuting raw, oftentimes unrecognizable information into translated and well formed patterns and shapes that people can recognize, and understand, and hopefully even connect to. This is often the same approach that an artist will take, at least speaking for myself as an artist for over ten years. I have long held a passion for this type of expression with my medium in previous years being oil on canvas. I now find myself using bits on machines, translating not emotions but data that represents some aspect of the world into actionable insights to be shared. Expression that connects is a vital and yet often underrated aspect of business, and is a critical stage in the data science process.  This view has been fortified for me working on my latest project with Flatiron School.

The premise for this project was quite interesting to me. Microsoft is interested in creating a new movie studio, and has hired me to *help the company better understand the movie industry*. The key question Microsoft wants answered through data analysis is: 
What **type** of **films** are currently doing the **best** at the **box office**?
Upon answering this question, they would like me to translate these findings into **actionable insights** for the studio to use when deciding what films they should make. 

After the data mining and cleaning stages were complete, it was time to begin making visualizations of the data. I see this stage as a way to listen to the story the data wants to tell. Just like any other part of the world that an artist wants to express, whether external or internal the ability to listen is key. This is how an artist can then express something, and with any luck it will be with a perspective that is new and visceral for those experiencing the art. Where in the past my expression may have looked like this:

![title](img/paintingm_m.JPG)

It now takes a new shape:

![title](img/eda1_5.png)

This boxplot is beautiful to me. It expresses the trend in movie length of the top 100 grossing contemporary films by their production budget. It makes apparent something that many of us movie-goers already know but perhaps had not seen put in these terms, the fact that most high budget movies are over 2 hours long. What will never cease to amaze me is the fact that as opposed to hours of brushing, allowing paint to dry, head tilting and brushing some more, this art was created with only a few lines of code:

``` python
# Create a plot and define its size.
    plt.figure(figsize=(15, 10))
# Draw a boxplot showing the runtime minute distributions among the ranges of
# production budget.
sns.boxplot(x=df_prod_100['budget_range'],
            y=df_prod_100['runtime_minutes'], palette="Set3")
# Set the plot title
plt.title('Top 100 grossing films by Distribution of Production Budget by Runtime')
# Set the x-axis Label and define fontsize
plt.xlabel('Production Budgets in USD', fontsize=15)
# Set the y-axis label and define fontsize
plt.ylabel('Runtime Minutes', fontsize=15)

# Show plot
plt.show()
```

With the information that this plot shares, a film studio could make more informed decisions about the runtime of a film they plan to make in the future based on the budget they have allocated for it's production. The exploratory data analysis phase gives the data handler much opportunity to make a statement, or several. One of the most powerful and beautiful plots I find is the `seaborn pairplot`, as it tells so many stories at once, all of which share the same core. As an artist, when I made such an expression it would reveal itself like this:

![title](img/painting_better_multiple.JPG)

And when applying the same intentions through python, the end result appears like this:

![alt text](https://github.com/MoJoMoon/dsc-mod-1-project-v2-1-onl01-dtsc-ft-012120/blob/master/img/eda1_3.png)

Here we can see so many stories being told. I can see that typically an American film's production budget does not increase it's US domestic gross, as well as worldwide gross, at least when the budget is over 150 million dollars. There is also a very strong almost linear correlation between a film's domestic gross and worldwide gross, which may come to no one's surprise.

As someone who considers themselves to be a data enthusiast and an artist, I find myself immersed in something I love, connecting to some part of the world and learning from it and expressing that lesson. In the business world I find that this is an invaluable ability, and one I intend to improve throughout my time in my Data Science cohort with Flatiron School.




