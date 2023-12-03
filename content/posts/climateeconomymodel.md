---
title: "How (not) to model like a pro"
date: 2023-11-09
description: "How plausible but flawed models hijacked climate policy."
tags:
   - pluralistic
   - extraordinaryphysics
---

The first thing I learned as a new management consultant is to build analytic models to answer business questions.
The way this works is to decompose the question into its main drivers, and assess each of them in a series of clear input-calculation-outputs steps (usually in Excel).
Once you have the model in place, you can evaluate different scenarios, do sensitivity analyses and other useful things.
Many problems can be addresed in this way, from building the business case of deploying fiber broadband across a country to optimizing a portfolio of assets.

To make it concrete, let's look at the example of a client asking you to assess the impact of climate change on the US economic outlook.
This is a tall order and could be the subject of an entire PhD thesis.
Now, as a consultant, you need to provide a reasonable answer in a short timeline, i.e. in weeks instead of months or years.
How to go about it?

Let's decompose the problem in it sub-components.
First, the economy is composed of multiple sectors, such as agriculture, mining, financial services, transportation, etc. From this list, you quickly realize that most of these actually happen indoor or in "carefully controlled environments".
These indoor sectors represent ~87% of US GDP.
So, if you assume that the impact of climate change on those sectors will be limited, you have already reduced the problem complexity by an order of magnitude - not bad for a first step!

Now, how do you assess the impact of an increase in temperature on the "outdoor" industries?
We don't want to go into the rabbit hole of modeling individual industries, so we need to find a good proxy.
Here our clever consultant will think of an analysis she could run: let's figure out if there is a relationship between current climate conditions and GDP.
Interestingly, if you look at US cities you indeed find a correlation between their average temperature and their GDP per capita.
Basically, both very hot and very cold areas have comparatively lower GDP per capita, while the cities closer to the average temperature fare, on average, better.
While the correlation is not perfect, it is enough for us to move forward, with the added benefit of having a fact-based and easy to explain methodology to our client.

So now we have all the ingredients to put together a first answer.
Combining the GDP at risk from outdoor industries with the empirical climate-GDP relationship we measured, we can estimate the impact of a 2°C or even a 4°C or 6°C climate scenario.
The output is reassuring: Even in a 6°C scenario the US GDP would only be reduced by ~10%.

While I skipped over some details to make the model more precise and robust, I would expect a junior consultant to be able to build the entire model and calibrate it in 2-3 weeks. 
Mission accomplished. 

Even better, it turns out that professional economists have been using precisely the same logic to understand the impact of climate change on the economy. 
One of the most famous of these models, called DICE, has even been used as a reference model by the IPCC.

Many people would likely stop here. 
Someone a bit more curious might explore a bit more the litterature, and find out that climate scientists are warning about disastrous outcomes for humanity when going beyond a 2°C increase. 
What is going on here?

> *"The current risk category of dangerous warming is extended to more categories, which are defined by us here as follows: >1.5°C as dangerous; >3°C as catastrophic; and >5°C as unknown, implying beyond catastrophic, including existential threats"*. Xu & Ramanathan, [PNAS](https://www.pnas.org/doi/10.1073/pnas.1618481114), 2017

If you take the time to think through the model logic I just outlined, you will quickly realize that, while plausible-looking, it is in fact completely and utterly wrong.

Let's start with the fact that “the outdoor part of the economy that is sensitive to climate change” includes agriculture.
A >2°C temperature increase could lead to water stress, loss of yield and suitable cropland, or even complete disruptions of food supply chains in certain areas. 
But, according to this model, because agriculture accounts for just 3% of US national output, climate disruption of food production cannot produce a very large effect on the U.S. economy.
For economists, the other 97% of the economy can function without food, so presumably without humans as well.

We then used a climate-GDP correlation *in space* to made a prediction *in time*. 
It is a big strech of the imagination that, say, Edinburgh's economic output will automatically grow to match London's because the average local temperature increases.

DICE inventor William Nordhaus even makes additional head-scracthing assumptions.
One of these is that the relationship between GDP and temperature is quadratic, without permitting any discontinuity.
This does not reflect the risks of climate tipping points, such as Arctic ice sea collapse, shutdown of ocean currents, or the Amazon Rainforest dieback. 
All of which would have dramatic consequences for human and natural ecosystems [^1].

Yet another simplistic assumption is that GDP growth is “exogenously determined".
That is, GDP growth is *not modeled* but simply assumed to grow at a fixed rate (~4% per annum until 2100) regardless of climate shocks - or any other type of shock for that matter.
Unmitigated climate change could result in mass migration, conflicts over water and natural resources, and overall political instability. 
None of this is expected to impact GDP growth in DICE.

> *"Nordhaus' model - known as DICE - is so badly flawed that it shouldn't be taken seriously". In fact, it's dangerous because we don't have another planet we can go to if we mess this up. The message he's been conveying is foolhardy"*. [Joseph Stiglitz](https://phys.org/news/2020-07-climate-economics-nobel-good.html), 2001 Nobel prize in Economy

DICE has been used to inform climate policies for years - essentially telling politicians and decision makers that there is nothing to worry about and to let future generations deal with climate actions and mitigation as the optimal course of action[^2]. 
DICE and its variants - or rather the economists behind - will partially be responsible for many of the upcoming climate disasters we'll be facing.

So, how do we get to a point where a simplistic, flawed and unrealistic model becomes the reference amongst economists and decision makers?
This is part of a broader issue about economists and their culture that deserves a separate post.

But perhaps the most baffling part about this story is that William Nordhaus received the *2018 Nobel Prize in Economy* for his work on DICE. 
I guess I should start revisiting some of the plausible models I built as a junior consultant. 
One of them could be worth a Nobel.

<br>

**References and further reading**

- [Exceeding 1.5°C global warming could trigger multiple climate tipping points](https://www.science.org/doi/10.1126/science.abn7950)
- [The Appallingly Bad Neoclassical Economics of Climate Change](https://www.patreon.com/posts/appallingly-bad-38048063)
- [When Idiot Savants Do Climate Economics](https://theintercept.com/2023/10/29/william-nordhaus-climate-economics/)

<br>

[^1]: To further illustrate how disconnected economists are from reality, in their 2021 study [Dietz et al](https://www.pnas.org/doi/10.1073/pnas.2103081118) concluded that *if all eight tipping points were reached*, the economic cost by 2100 would amount to an additional 1.4% of lost GDP on top of the ~10% percent that Nordhaus projected. 

[^2]: In his work, Nordhaus assesses the cost of implementing various policy responses such as carbon taxes.
But since the economy is assumed to grow at a fixed rate (again, GDP growth is an exogeneous assumption), we basically always end up 'economically better off' by postponing any climate actions since future generations will, according to the DICE model, have more economic resources to deal with it (technically, Nordhaus considers the Net Present Value of different options. Using a positive discount rate reinforces the bias towards delaying any actions since future costs have lower contributions to the NPV). 
