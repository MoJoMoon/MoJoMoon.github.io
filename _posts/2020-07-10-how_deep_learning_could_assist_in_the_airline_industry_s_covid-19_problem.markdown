---
layout: post
title:      "How Deep Learning could assist in the Airline Industry’s COVID-19 Problem."
date:       2020-07-10 09:24:14 +0000
permalink:  how_deep_learning_could_assist_in_the_airline_industry_s_covid-19_problem
---


Disclaimer: This work is meant to fulfill educational purposes. The hypothetical business case, and results of modeling are not meant to be considered as medical advise, and has not been approved by any governmental, professional or medical body.
At the risk of oversimplification, it could be said that coronavirus is not inherently in itself, but in how it harnesses the power of the normally healthy interactions between cells within the body against itself. It confuses immune cells into identifying healthy cells as malignant through a kind of disinformation by manipulating chemical signals within the body.
In observing media over the past months, one could note a similar effect of the coronavirus when analogizing the global population as a societal body. Our normally healthy (some arguably so) have now become potentially lethal events, as currently hundreds of thousands of unrecovered cases could attest. This not only effects our interpersonal relationships, but on a macro scale the world economy and those industries that comprise it.
Image for post
Safe-Graph Data on Covid-19 https://www.safegraph.com/dashboard/covid19-commerce-patterns/?utm_source=newsletter&utm_medium=email&utm_campaign=weekly_patterns_launch
One of the industries most heavily impacted by this pandemic is the passenger Airline Industry.
Image for post
Safe-Graph Data on Covid-19 https://www.safegraph.com/dashboard/covid19-commerce-patterns/?utm_source=newsletter&utm_medium=email&utm_campaign=weekly_patterns_launch
Until a vaccine is designed and tested, the most effective remedy our society can engineer is social distancing, which inherently is damaging to the airline industry and the concept of travel in general. Even after an effective testing system and vaccine have been created, precautions will most likely need to be put in place to combat the spread of covid-19 as the industry attempts to regain it’s footing. Here a proposal for aiding in this recovery is presented with a focus on on-site CT scanning of high risk travelers at targeted international and domestic airports, and Convolutional Neural Networks (CNN) that predict coronavirus infection from the resulting imaging.
Proposal
Image for post
Airport arrival
Upon arrival at an airport terminal, more verification systems have been put in place at the checkpoints. Along with the typical luggage scanning, there are state-of-the-art social tracing and infrared imaging for temperature readings that assess a traveler for their risk coefficient of being covid-19 positive. Depending on the spread rate and other factors at that time, a threshold is set for that airport at that time which if the traveler’s risk coefficient does not exceed, they are cleared for travel as usual.
Image for post
Low risk-coefficient
However in the event the risk coefficient is higher than said threshold, the traveler would be asked to agree to further testing. One option which is the focus of this proposal is non-invasive and involves taking an x-ray scan of the traveler’s lungs.
Image for post
High risk coefficient
These images are then treated as data to be run through AI, a Convolutional Neural Network which produces an accurate probability of whether or not this traveler is infected with covid-19. If the outcome is most probably negative, the traveler is cleared for travel. If the outcome is most probably positive, further testing would need to occur before safe travel.
Image for post
Testing
This is where the power of Deep Learning can assist in the problem for the travel industry as it recovers from the covid-19 pandemic. There are several data scientists around the world that have generated models that have high accuracies in predicting covid-19 in x-ray scans of lungs. The model featured in this proposal is VGG19 model which is a 19 layer convolutional neural network created by the Oxford Visual Geometry Group for the ImageNet Large Scale Visual Recognition Challenge ILSVRC-2014 competition trained on 4 GPUs for 2–3 weeks.
Image for post
Using transfer learning which is defined by Goodfellow et al in *Deep Learning* as a “Situation where what has been learned in one setting is exploited to improve generalization in another setting”. By this definition, we will use the weights gained from the large imagenet dataset, and the architecture of VGG19 to generalize for our covid-19 dataset.
Image for post
Image for post
Our model will assess these images in ways that are not humanly possible, making comparisons and analyzing the data in millions of ways until it has effectively learned the telltale signs of covid-19 in these images.
Image for post
After training this model, it has met the FDA standards for recall, but would need further extensive testing to be considered for performing on the field.
Image for post
My aim is far from transforming the experience of traveling into a conveyor of surveillance, or to infringe on any individuals rights, very far from it. This proposal is an option that can be used to reduce the spread of covid-19 and should not be imposed on any individual against their wishes. Implementation of this proposal would have benefits and drawbacks, some of the benefits being leading to further treatment of covid-19 and data collection of covid-19 related cases. For example these images produced by the model show what key factors the network uses in determining covid-19
Image for post
In one of these images could be a vital clue in medical research that could save lives. Until then I wish any one reading safety during these uncertain times, and an expression of the hope and will that things will get better over time.
To view the work used in this proposal visit the git hub repository at this link: https://github.com/MoJoMoon/dsc-mod-4-project-v2-1-onl01-dtsc-ft-012120
Have a great day!
