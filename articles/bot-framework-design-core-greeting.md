---
title: Bot Framework Designing Bots - First Interaction | Microsoft Docs
description: Provides guidance about designing for the first interaction between user and bot. 
keywords: Bot Framework, Bot design, core principles
author: matvelloso
manager: larar
ms.topic: Designing for the first interaction between user and bot

ms.prod: botframework
# the ms.service should be the section of the IA that the article is in, with the suffix -article. Some examples:
# get-started article, sdk-reference-article
ms.service: design-article

# Date the article was updated
ms.date: 01/19/2017

# Alias of the document reviewer. Change to the appropriate person.
ms.reviewer: rstand

# Include the following line commented out
#ROBOTS: Index
---
# Designing for the first interaction

##First impressions matter


![bot](media/designing-bots/core/hello-bot.png)

The first interaction between the user and bot is critical to the user experience. Developers should keep in mind that there is more to that first message than just saying “hi”. When you build an app, the first screen is usually where the key navigation cues are given: Your will tell the user where the menu is, maybe give some cues on how it works, where to go for help, information about its privacy policy and so on. Now switch from app to a bot and we still have the same user hoping to get access to the same kind of information. In other words, just saying “Hi user” won’t be enough.

So what is that a bot needs to tell the user upfront?

Let us compare these two designs:

Example 1:

![bot](media/designing-bots/core/hello1.png)


Example 2:

![bot](media/designing-bots/core/hello2.png)


Starting the bot with an open ended question such as “How can I help you?” is usually a bad idea. If your bot has a hundred different things it can do, chances are users won’t be able to guess the vast majority of them. Your bot didn’t tell them what it can do, so how can they possibly know?

For decades, developers have used a simple solution to that problem: Menus. Turns out, breaking down the available options into some sort of menu is still a great idea. First, it mitigates the basic discoverability problem. Second, it spares the user from having to type too much: They can just click, which is always the fastest option. As an additional benefit, it can significantly simplify your natural language models.

>[!TIP]
>Menus are your friend. Don’t dismiss them as not being “smart enough”

Note: You can still use free form input along with menus. Users can still type whatever they want and your bot can try its best to parse their request. There is absolutely nothing wrong with it. But usage will likely tell you that the majority of users still prefer to just click at the buttons. Don't try to force them to use your bot the way you would like them to instead.

Beyond the basic navigation, there are things you should tell the user. Again, no different than an app or a website: If your bot collects personal data from the user, that is something you should be telling them about. This is where your bot should have some information about terms and privacy on web pages and offer the user a link to that data. In fact, the [Bot Framework registration portal](https://dev.botframework.com/) already offers a place for you to add links to your terms and conditions to be associated with your bot.

>[!TIP]
>Tell the user upfront about your policies and what you will be doing with their personal information