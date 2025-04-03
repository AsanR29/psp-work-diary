
# This week I finalised github commits of the previous week's work, and I did alot of new work too

•	March 5th: On “methods-(awesome)” branch: “Gosh Darn” commit:
[https://github.com/Jek204/IBM-Skills-Build-Game/commit/23cad37767081f8e56fbc601b7a16eb4ba371cdf#diff-93f3ce42b5e5936d5be1b4cf5fd0325c5dfba4f77f07dda19dfae873d8c34858]
-   I resized a lot of the godot packed scenes, to make more room for cards on the screen. Extremely tedious work because our scenes aren't created using anchors, but I'm not in charge of those so I don't take the time to fix it.
-   Taking advantage of that space, I add more placement sleeves on the screen ( a "sleeve" is a collection of playing-cards. Please respect our eytmology) and program the ability to move cards between them instead of only from the hand to a sleeve and back. 
-   This functionality is extremely glitchy, due to the inherit defects of Godot’s Button elements (so I will move away from using them). I realising that my original plan, seen in a prior class diagram, with the "stage" class for handling the View, *was* necessary; in order to regulate what is allowed to respond to a click, or a hover, event I need to hand out Z-Indexes to anything which is supposed to have overlap on the screen -the cards! Then those input events can check the Z-indexes of everybody affected and target only the one with the highest Z-index.
-   Online they suggest using Godot's "Raycast" instead of what I described, but I'm sick of Godot. All its tools are poison. I'm only at this point because of how terrible their buttons are. 
-   In addition, I need to control the Z indexes of the cards anyway. If the player's hand of cars doesn't have them with ascending z indexes, left to right, then it looks garbage on an unacceptable level. This is why I need Stage.

•	March 9th: On “methods-(awesome)” branch: “”click. readds The Click” commit:
[https://github.com/Jek204/IBM-Skills-Build-Game/commit/5b4170e120b22b1f239749287f7edd25df9d6a8d#diff-d9237b2a8a613f0749aaf022505410ecf69fef8e49d68173b0a5db26eb79a29b]
-   I added the classes “Puppet”, “Conductor”, and “Stage”. 
-   I read in a book about composite classes, and the controller being a subclass of the controlled. So I applied it here, and it worked great.
-   Then I made the pre-existing classes of CardScene and SleeveScene inherit from these.
-   I reprogrammed user input entirely to stop using godot buttons (which were buggy and unreliable) and to instead detect the position of every click and, through the stage class, figure out which card to implicate. 
-   A lot of ground work for future ui interactions. In my ideal world, anything visibly on the screen would inherit from Puppet or one of Puppet's subclasses. To disambiguate from Godot's wretched awful systems as much as possible. 
-   Thanks to Stage, only the element on the screen with the highest Z index is the one selected (beforehand, everything beneath where a mouse clicked would run their own functions). This means only the thing ontop gets clicked.
