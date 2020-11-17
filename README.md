#Blaseball_better
I have recently gotten interested in the game of Blaseball. An online splort simulation game that is equal parts silly and charming. The community is enthusiastically welcoming and home to many talented creatives. The lore is in-depth and ever changing and is driven entirely by the interaction between the devs and the community. The devs make sure that the choices presented are interesting and many times nearly indecipherable.  
Players die, get revived, sent to the shadow realm, and teams may end up fighting gods after the end of a long fought season. All in all it has a choose your own adventure/twitch plays pokemon feel to it that is a welcome distraction to current events. 

One of the only mechanics that you can actually interact with in this game are coins and betting on teams. This in turn lets you buy votes so you can help decide which of the Decrees and Blessings will be chosen at the end of the season.The betting mechanics are not difficult, the game gives you a percent chance for each team to win against each other and that chance is pretty accurate. Which means that as long as you are betting on the teams with over a 50% chance to win, over the long run you will make money. You can also be a little safer with this by only fully betting when you have a greater that 60% chance to win and doing smaller percentages of your max bet as the percentages to win decrease. All in all this makes making money easy but tedious. Which is exactly what programming is great at doing. I'm going to code up an auto-better so that I never miss any games to bet on and can get the maximum amount of coins possible. 

I am going to be using Python as my language as I am most comfortable with that and it has a great library called Selenium that makes intereacting with webpages as painless as possible. 

This is my first time making something like this so writting out my design ideas will hopefully make the coding of this as painless as possible. 

First off I will need to check if I have zero coins. If I do Blaseball has a mechanics to get more coins everytime you are at zero by going to the shop and "begging". So if I end up with zero coins I go to the shop and beg. 

Once I have coins I need to go to the upcoming games and found out which games have the highest win chances associated with them. I will bet on those games starting with the highest win chances and working my way down following a few simple rules. 
If the chance to win is 60% or higher I will bet either my max allowed bet or my full amount of coins if I don't have enough to cover a max bet
If the chance is between 55% and 59% I will bet 75% of my max bet or my max amount of coins If I can't cover that.
Any chances between 50% and 55% will be at 50% of my max bet or my max amount of coins if I can't cover that. 
Between each of these bets I will be checking on if I have 0 coins. 
Once all the games have been bet on then the program will sleep until the next time it gets called. 

Once I have around 20K coins I will change this strategy up but i don't need that automated since once I have all this set up I can change the behavior as I see fit. 
Some stretch goals for this would be to create a GUI so change the behavior easily without having to go into the code as well as making it easier to share to others and have them change the behavior 

Another important thing to note is that the games all start at the top of the hour. So I will want to set this program up to run sometimes between 10-5 minutes before the top of the hour. 
