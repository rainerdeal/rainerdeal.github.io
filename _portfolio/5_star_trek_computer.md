---
title: Star Trek Computer
description: 'Minimalistic natural-language processor with Star Trek: TNG themed queries.'
image: /images/portfolio/trek.png
tech_stack: [Swift, iOS]
live_link: null
live_link_name: null
source_link: https://github.com/katelandmesser/Computer
source_link_name: GitHub
---

#### Dependencies:
* Coffee ☕️
* Extensive knowledge of Star Trek 🖖🏼

#### Background
This was a project for a very strange class in college. TBH, I couldn't even really tell you what the class was or what I was supposed to get out of it, but I remember learning about Lisp, Lis.py, and "Automata." The class was taught by someone of the [Professor Trelawney](http://harrypotter.wikia.com/wiki/Sybill_Trelawney){:target="_blank"} vein... Anyway, there was an opportunity to come up with a project and my partner and I decided to do a natural language processor app on iOS. Luckily the professor was a *HUGE* nerd. In *Star Trek: The Next Generation*, the crew of the Enterprise makes liberal use of an onboard computer that is omnipresent and omnipotent. They can be standing anywhere on their ship and simply say, "computer..." followed by a command and in a matter of seconds, the computer will respond with an answer. The project goal was just to try to mimic what was on the show as best we could (this project went above and beyond the requirements for the class so the sky was the limit).

#### Details
Our version of the computer ended up being a very simple personal assistant with a *Star Trek* flavor. You press a button, triggering the phone to listen to you, and when you speak a command, it is translated from speech, to text and then parsed. In our case, it was looking for keywords and the first thing you said had to be "computer" (which is how it works in the show).

#### Grammar
###### Sample commands & queries:
    Computer, what is our current location?
    Computer, where is the Starship Enterprise?
    Computer, what is the destination?
    Computer, open captain’s log.
    Captain’s log, star date <number>…
    Computer, is crewman <last_name> on the ship?
    Computer, where is crewman <last_name>?
    Computer, what is the mission of the Starship Enterprise?
    Computer, modify authorization for Crewman <last_name> to <number>.
    Computer, initiate auto destruct sequence authorization <number>.

###### If statement based on second word:

Simplification         | Alternatives
---------------------- | -------------------------------------
what                   | location, destination, mission, date
where, locate, is      | starship, crewman
open                   | captain’s log
modify, change, update | crewman (auth.), mission, destination
initiate               | destruct

###### Case statement based on second word:

Simplification | Alternatives
-------------- | ----------------------------------------------------------------------------
verb           | open, is, modify, initiate, locate, change, update
pronoun        | what
adverb         | where
identifier     | location, destination, mission, log, crew member, destruct
crew member    | Captain, Commander, Crewman, Lieutenant, Ensign, Admiral, Lieut. Capt. Cmdr.