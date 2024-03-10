I started by interacting with the chatbot, and it gave me a lot of useful information, such as the data Mecerdes F1 uses in the race and acts upon. However,  the more questions I asked it, the more I got the impression that Mercedes was already taking into account every possible data point. This point was exaggerated when the chatbot confirmed the fact that strategy was impacted by the help of AI, already taking into account 1000s of data points that no human would.

I looked through the link it gave me to OPENF1, and there was an obvious culprit for what was being underutilised. The weather can be predicted, tyre degradation can be predicted, but you can’t predict what a driver is going to say. From watching a my fair share of F1 in the past, I knew that all F1 teams can hear all team radio. Now, obviously Meceredes takes into account team radio whilst making strategy calls. But what if an AI could analyse the team radio and feeback to the team what the driver might actually mean based on similar times they said such things in the past. Being a fan of the sport, I knew that teams like to communicate in codes: PlanA or PlanB etc… and some drivers try to deceive other teams over the radio. I think Hamiliton at the 2021 portugese grad prix did this on a couple of occasions. 

After all of this research I knew I wanted to tackle and work on the underutilised area of team radio, with my end goal being to give each incoming radio message a probability that it would affect a drivers race based on times they said similar things in the past.

This is the protype that I came up with. For this specific project, I knew the UI was not going to be of highest priority for this specific challenge, so I used swift which provides a quick way of presenting the data. The opening list is just a list of all the recent communications which Mercedes already has software for. The first few communications are at the end of the race, shown by the date the API updated. If I press the Hulkenburg radio, I can hear that he spoke negatively about his tyres. 

What the application aims to achieve is to find the probability that this radio communication is an indicator that his lap time will decrease in the next few laps. Not to say he is lying about sliding all over the place, but if the last few times he said this he ended up gaining positions within the following laps (with car failures and pitstops accounted for), there is a higher chance that this driver just tends to overexaggerate about this issue.

When I chose to press on the radio communication, it takes me to a screen with all of his other recent radio communications where he spoke negatively about his tyres, and what the calculated accuracy was of that communication. 

The calculated accuracy of a communication of this type is related to the r value of the lap times he set after saying it. In other words  if he started to improve his lap times after saying he had no grip, then the chance of what he said being meaningful are lower, therefore a lower probable accuracy. 

This being a prototype, there are quite a few areas in which I would like to work on if I had more time. The main being creating an AI entirely from scratch that handles the classification of driver communications. This was one of my main goals when I started the project, however when I saw that it would take this long for an AI on my local machine to transcribe enough radio communications for this to be plausible, this quickly shot down my hopes.




Not all scores and calculated off of the r value of the following lap times, for example if a driver finished the race and spoke negatively about the strategy, it would look at his position in the race compared his average position. Using these past communications I am able to put a probability that this radio message will correlate with an impact on his pace after saying it.
