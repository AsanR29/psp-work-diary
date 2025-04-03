
# The week after Sprint week 2
The module isn't over yet, so we can still add to the code, right?

-   Me and Jake both tried our hand at finishing the code merge which we failed to have done in time on Thursday (if only it was due Friday like initially expected...)
It was very difficult and took too long.

-   After I successfully merged the *code*, I realised that all the new Godot Scenes that Alex added for his Tutorial were using the old screen size, not the new one.
So I had to go through each one and resize them and reposition thr ui elements. Which took so long. I think Jake had to do it too, very unfortunately.

-   I added Unit Testing. Right after thinking to add it, I had the idea which I went on to use for my approach, and it wasn't hard to add. However, it wasn't very robust. Our code isn't designed in a Unit-Test pliable way. I would've liked to test user input reactions but we don't have a way to disable the game sensing the "mouse isnt pressed down" without complicating some of our essential code.

-   Tom noticed a bug where you couldn't interact with cards after the 1st match. I figured out pretty quickly that it was because I'd forgotten to Dispose of old CardScenes, despite the fact I'd anticipated this and programmed the methods to do so much earlier. The fix was ~6 lines.

-   The group complained about my version of the merge having lost Alex's differently coloured box borders. I went into Alex's stuff, exported his custom box themes as actual files, and then made all the boxes load one of the 3 files they were supposed to have. I don't know why Alex didn't make his themes into files, and I'm wondering whether he custom applied that theme to all of them individually or not.

-   I wrote down some of the integration testing I'd constantly been doing, while debugging my code, into our testing plan.