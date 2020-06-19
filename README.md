# Labs-Sprint-Challenge-2.3-Accountability-and-Delivery

This challenge allows you to practice the concepts and techniques learned over the past week and apply them by providing answers to questions related to working with others of your Labs product.

In your challenge this week, you will demonstrate understanding over these topics by responding to prompts.

## Instructions

Read these instructions carefully. Understand exactly what is expected before starting this Journal Entry.

You are not allowed to collaborate during the Journal Entry. However, you are encouraged to follow the twenty-minute rule and seek support from your TL if you need direction. Your work reflects your proficiency in being able to adapt to changes that approach you during Labs.

We have allocated time on your schedule to ensure that you get this done at the end of each sprint.

For Full Time Students: Please submit your work on this journal entry before 11am PT every Friday.
For Part Time Students: Please submit your work on this journal entry before the end of your B-Week Thursday class period.

## Introduction

Now that you have been down in the thick of the Labs process for a while, we want to hear how you've come to a few conclusions and dealt with requirements changing throughout your delivery process.

Any time that you've deviated from your original plan, as documented in your release canvas, we want you to tell us about why you pivoted from the plan which you agreed upon as a team.

**Please respond to the following prompt to detail out the reasons your team pivoted away from the plan upon which you agreed as a team.**

### Prompt 1

As you have now been in the process of delivering and building your product, we'd like to know what has changed along the way:

- Describe how the requirements of the features you have been building/designing have changed.
- What caused these requirements to change?
- **Engineering Students:** What types of architectural requirements changed? Did you have to make any trade-offs or add any new packages/libraries or dependencies to your application's technical stack in order to meet the new changes? **Please be as specific as you can. Provide details via screenshots to Trello cards or your release canvases to support your response.**
- **UX Students:** Describe any design patterns or user flows that had to change as a result of the requirements above. **Please be as specific as you can. Provide details via screenshots to design files or your release canvases to support your response.**
- **Data Scientists:** Tell us about how your work has evolved from the beginning stages of finding and cleaning the data with which your team is working all the way down to delivering that data model through your project's data pipeline. **Please be as specific as you can. Provide details via screenshots to Trello cards, Python/Jypyter Notebooks or your release canvases to support your response.**

1. Our inputs for the project from the beginning have been "emails". 
2. During the initial phase of planning our project we decided we would support the retrievel of emails through IMAP. 
3. It quickly became apparent, after that initial phase, that using IMAP would be a larger task than we had time for if we were to accomplish the rest of what we had decided we would accomplish.
4. In addition to this IMAP is a burden on the end-user as most email SaaS vendors do not support IMAP out of the box. This service usually requires custom settings on the part of the user on their SaaS platform. It is assumed that most email users do not have the knowledge or patience to deal with such advanced settings such as IMAP.
5. The result of all of this is that we ended up choosing to use the Google API to retrieve email strictly from Google accounts.
6. A natural result of the Google API is that Google is quite restrictive in how access to their API works and this curtailed our ability to use multiple accounts. Barring use of the standard Google Oauth forced us to create authentication tokens manually for each account used.
7. On the data science side of this I was forced to create an email account from scratch in order to run tests specifically on messages retrieved through the app. This would involve crafting an email message in a specific format, such as a plaintext - or a multipart with an attachment, etc. The process involved sending specific email to account and run the API to determine if the current code was doing what it should, until it is, and then crafting a new email for a different use case. Each time I changed the use case I had to delete the existing email from the inbox. This method was tedious but it allowed for a lot of freedom in debugging the various ways that the Google API packages emails.
8. The Google API does not consistantly package emails in JSON objects. Or rather it uses differently shaped JSON objects for different types of email payloads. There is no documentation on this that we were able to find so I literally spent several days exploring the ways that the Google API was packaging different types of emails.
9. Monica did most of our modeling. I did some but in order for me to do my work I would take her initial ideas and translate them into a the application environment. She was working with the Enron email database and I was working with live emails pulled directly from an inbox. There is a substantial difference in the data in these two instances and as I had to be able to work effectively with Monica and her models I ended up working with both sets of data. This required that I had to develop tools to reflect the state of all 3 code bases: that in the notebooks, that in my CLI scripts, and that in the built out app. Each one required subtly different pieces of code and the way the data was cleaned and organized.
10. Our final model engineering took several days of trial and error and we never did find an adequate implementation. After a meeting with Ryan it was clear that we should go for MVP and lay out a plan for future development with the plans we had while implementing a bare bones closing of the loop on the API.

![](https://raw.githubusercontent.com/filchyboy/Christopher_Filkins_Labs-Sprint-Challenge-2.3/master/IMG_0108.PNG)

![](https://raw.githubusercontent.com/filchyboy/Christopher_Filkins_Labs-Sprint-Challenge-2.3/master/Screenshot%202020-06-19%2010.22.14.png)


## Submitting your work

Please submit a link to your journal entry for this sprint, in the Sprint Retrospective Form. This is to be done every _Friday before 11am PT_ -- for Full Time -- and before the end of your 2nd '5th' day -- for Part Time -- to be counted as a submission for that sprint.

## Rubric & Samples

[Here is a link to the rubric](https://www.notion.so/lambdaschool/2-3-Rubric-Accountability-and-Delivery-Diff-Entry-a35bcf0776194cdbba1c849007860b46) that will be used to assess your answers to the prompts. _Use this as a guide_ as you craft your responses.

[Here is a link to a sample submission](https://www.notion.so/lambdaschool/2-3-Accountability-and-Delivery-Diff-Entry-4dc1dbb2b1164b74849cd065adf8e209) that you can use for inspiration.
