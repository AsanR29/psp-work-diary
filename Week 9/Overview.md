
# The week before sprint week is almost more productive than the sprint week itself.
Except I think it actually was, for me.

•	March 23rd I finish a commit to “from-refactor” called “Commit”
[https://github.com/Jek204/IBM-Skills-Build-Game/commit/8a1ece2169e55ba7f09897522f04256f19aacf44#diff-0276aba4892268c690b3aa2ea8356a7881f11dff09a3ecf485f6c9fb495332b6]
-   It creates a distinction between placements on the game board and the player’s hand of cards, using subclassing off of SleeveScene. In addition, I split SleeveModel into 2 subclasses, off of a virtual base class, for a respective array & list format. Check the Week 10 diagram if you don't understand.
-   I resolve a circular issue where the SleeveScene needed to know the order of the cards inside of itself, but saving that order on it would mean that the order is duplicated, with it being there & recorded on the SleeveModel. It took a fair amount of thought to figure out how to avoid that data integrity issue because it gave me anxiety over how I couldn't get a perfect solution.

This week was in part defined by cutting up my prior code and preparing it for the sprint week. Everything I wrote tip-toed around the actual battle system -the code which would govern who can play a card, when, and what playing a card means. I thought it was too important for me to start off alone, I wanted to let Tom establish the foundations for it, and I also knew that there was enough work for me to do outside of it. None of the code I wrote for the ui can be called unnecessary, I think it all ended up as essential requirements.

-   I Added a class called “Agent”, and 2 subclasses: “PlayerAgent” and “EnemyAgent”. 
-   These represented the player’s collections of cards & corresponding CardScenes, in addition to the enemy’s versions. 
-   These classes gave a good place to store the SleeveScenes -storing them only as Puppets on the Stage makes some of their code as the *class* SleeveScene inaccessible, and creates issues with respect to the godot scene tree (which cannot be resolved, only avoided). By Refactoring the preexisting code managing the Sleeves in Game.cs and placing it into the player agent, adding the entirely new EnemyAgent sleeves became significantly easier.
-   Made it so that starting a new game would create the player & enemy agents, & a “GameData” class, and store the majority of transient data within them. As a result, I was able to instantiate the differently based on whether it was the player’s first match or a subsequent match, and the game can now save the player’s cards and play multiple matches.


"Commit" was close to 1000 lines of code. 