---
layout: post
title:  "My Sinatra Portfolio Project - Garm Road"
date:   2017-09-26 02:47:15 +0000
---

For this assignment I looked to my wife for inspiration. We recently had a child (5 months old now) and one issue we've been running into is clothing. A child will quickly outgrow their clothes and we find ourselves left with a heap of clothing we used briefly and no longer need.

This is not a very unique problem; clothing exchanges already exists for local populations, but what if there was an app for that?

This is the foundation for "Garm Road". For my project I made an application that allows users to present their unwanted clothing items up for other local users to take, while also providing a platform to find the next age appropriate clothing items the user wants.

##The Setup

I ended up setting up 3 simple models: user, item, and review.

User - sets up the user with username, email, password, location, image, and profile details
Item - sets up an individual item and contains name, item_type, image, etc.
Review - is a review for an individual item from an individual user (who has possessed the item)

I could have gone further and made an item_type and location class, to make searching easier, but I didn't feel that minor functionality was entirely necessary to show proof of concept for the project.

##Coding

This ended up taking me 2 days to complete, with the help of previous code from other projects which had some overlap (user login/signup).

I also added some CSS styling because the default style was giving me a headache.

##Final Product

[This is the GitHub link to the project.](https://github.com/mahdiASC/garm_road)

