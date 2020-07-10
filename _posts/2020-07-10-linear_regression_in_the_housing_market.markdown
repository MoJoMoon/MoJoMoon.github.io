---
layout: post
title:      "Linear Regression in the Housing Market"
date:       2020-07-10 09:26:24 +0000
permalink:  linear_regression_in_the_housing_market
---



For the second project of my Data Science cohort with Flatiron School, I was assigned a dataset focused on around 21,000 houses from King County, Washington between 2014–2015:
Image for post
Given this data the task was to establish a novel business case that would utilize this data and create Multivariate Linear Regression Model that would predict the price of houses in the area with high accuracy, and I must say the project was quite enjoyable. I would like to share some of my more proud moments, and challenging obstacles experienced creating my model.
Using the OSEMiN Pipeline, I felt that my methodology was straight forward. I was to Obtain, Scrub, Explore, Model, and Interpret the data given, while relating it to a business case. I chose to assume the hypothetical job assigned by Cocoricos, an innovative tokenization platform for real estate markets across the globe. It took some research to develop a general understanding of what this means, and this is one of my first moments of true excitement. I see more and more that working within data science involves a versatile and well rounded general knowledge about various subject matters. This is something that truly attracts me as I have a passion for finding the connections and relationships between all things, exploring this omni-present inter-connecting web across time and space. After visiting the Cocoricos Platform I could see that using a linear regression model and conducting analysis of housing market data would be quite useful for their advertisement team if they were ever interested in launching in the greater Seattle area.
Image for post
Snapshot of my presentation on Launching Cocoricos in King County.
When looking through the data, I thought it would be interesting to know what days the houses were sold. My initial assumption not being in the housing market or a homeowner myself, I thought most houses would be purchased on days that buyers would be free, i.e. the weekend. I was quite surprised to see that the data showed the exact opposite, that relatively almost none of the houses were sold on the weekend and that Tuesday, and Wednesday took more than 40% of the transactions. It turns out that there is a theory within the housing market that, according to Redfin a real-estate brokerage “most people tour listings over the weekend, and they begin planning their weekends on Thursday… a home gets five times more views on the first day it is listed than on subsequent days. This is likely because most online real estate sites offer alerts of new listings to potential buyers.” Further explained by Karen Kelly of real-estate brokerage Compass “In this competitive market, most of the agents are sort of abiding by the Thursday, Friday and then taking offers on Tuesday.” How fascinating!
Image for post
My next challenge was working with data containing a geographical dimension. It seemed an effective business practice to share visualizations of the data. Initially, I was amused at how seamlessly a scatterplot could be used to create a map of sorts that would tell the story of the distribution of the prices in the area, and this led to a reflection on the inherent power and importance of interpreting data.
Image for post
Seaborn Scatterplot of House Sales by Price in King County 2014–2015
However, this would not tell a detailed enough story for potential investors or executives, and so I took a deeper dive into Choropleth maps in python and was surprised when I came across the Gmaps API. It felt like I was a child again playing with video games to alter the map types, check various features within the data, and change layers.
Image for post
Image for post
Taking a look at the streets, and successfully utilizing the Gmaps API I felt like trying something new, Reverse Geo-Coding. My dataset came with latitude and longitude features, which I could use to find the actual street addresses of the houses. With this information I was able to make a list of all the addresses and find the streets that contained the most expensive properties.
Image for post
Image for post
How useful is it for businesses to be able to take data such as the latitude and longitude of houses and extract the actual streets that their advertising campaigns can focus on.
With my Obtaining, Scrubbing, and Exploring processes completed, it was then time for the actual modeling. This was quite an iterative process as I had set a goal of creating a model with an Adjusted R² value of 0.75. My baseline model came to 0.739. In order achieve my goal I conducted more feature engineering, this meant creating features of what decade a house was made, making dummy variables for how many bathrooms and bedrooms were present and for each of the 70 zipcodes. I was realizing that I was going to far when I found myself making splitting the square feet of the house feature into 65 different bins to add even 0.001 to my Adjusted R² value. It was quite exciting to continue trying different methods, using scaling and log transforms, XGBoost and VIF to create as best as a model as I could. Finally I came to a linear regression model with an Adjusted R² value of 0.839, which would underestimate 12% of houses by over $100,000 and overestimate 15% of houses by over $100,000.
Image for post
It is clear that when predicting house prices with machine learning, today there are many more effective options that linear regression, but it is within the process of creating the model that so many valuable insights can be extracted and used for good business practice. Needless to say for myself, I have been thoroughly enjoying my time with the Flatiron school, and the projects I have been assigned, and look forward to the next chapter in my data science endeavors.
