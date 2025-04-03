
# Sprint Week 2


•	March 24th 
-   Fixed a major visual bug in the last commit.
-   Organised & commented the code to make it easier for the others to read.
-   Updated an older class diagram.

•	March 25th
-   Created a new special sleeve called Reserves, and some new code to initialise a match’s starting deck to draw from.
-   Spent several hours watching Tom while he programmed, and worked together with him to speed up the resolution of conflicts between eachothers’ battle-code. 

The BattleController class he added at the beginning of the day was big and monumental for our game, and I also knew that Tom hadn’t previously written much code which interacted with mine (before the BattleController), so I reasoned that the best use of my time would be to just watch and help him, and that that process would kill 2 birds with 1 stone by also familiarising me with the BattleController. I was right tbf. I’d heard about companies in the past trying out a method of organisation where developers worked in pairs, simultaneously, and that apparently it didn’t result in a huge loss of efficiency.

•	March 26th
-   Using the code provided by the BattleController, I expanded the UI to add the Targeting system whereby the player could click on one of their own ships and then choose another ship to attack (instead of moving the selected ship like what happened up until now). That’s all I added, but I added it quite fully and in the grand scheme of our game, its really one of the most important actions that the player can take… I based my approach off of the class diagram I drew in week 9 but couldn't act on because I had other stuff to do before I wanted to start adding the Turn Order. I'm glad Tom set it up instead of me; I preferred reading someone else's code and taking from it. I added targeting using signals because Tom had tried to use them elsewhere in the BattleController.
-   I also added a class called a “SignalButton”, where essentially the buttons would be governed in our code and appear/disappear in accordance with the gameplay. As an example: I added buttons for the player to end their own turn and to “abort targeting” (in case they changed their mind about firing an enemy ship). They emitted unique signals, and the code responded to them properly.


•	March 27th
-   I combed through our code and enforced the conditions on where players were allowed to interact with cards in certain ways, or not. I spent a lot of time trying to merge this branch with the others’ work on the main branch. I fixed an oversight where crew members didn’t die when their ship died.
