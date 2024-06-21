
## How to do this?

Every program can be divided into states that it is in, meaning you can account for every variable and its representation in the machine.
So, how does that help, you ask, it works kinda like this:

![[States.png]]

Excuse the crude drawing, but you can see that every program has states that it can be in, similar to a graph.

![[labeledStates.png]]

So, as you can see, the processes can be read as having states that it can go into, for instance, this basic process just abstractly opens and uses a file, and then uses that to do whatever, and the *star* represents the final state of the program, if it ends.

But, how does a process get stuck, how do you know if a program will halt?
Look at a #flowchart:
![[Process.png]]

Look at the red box, that is what prevents halting, flowchart wise. Cool, you say, but how does that relate to anything else you said.

## Any transition between states involves a #flowchart.

The red box, refers to Jumping (lit. jmp in assembly) where the program goes back, away from the finish (the green star). This is indicative of the analysis of the conditions may assist with jumping, and knowing what states are similar and what abstractly causes a jump can help us naively solve the halting problem.

