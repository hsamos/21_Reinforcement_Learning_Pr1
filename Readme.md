# Capstone Project
At each position there are 6 different actions that can be taken.

Action 0: Go South if on field.
Action 1: Go North if on field.
Action 2: Go East if on field (Please notice, I mixed up East and West (East is Left here)).
Action 3: Go West if on field (Please notice, I mixed up East and West (West is right here)).

Action 4: Pickup item (it can try even if it is not there)

Action 5: Drop-off item (it can try even if it does not have it)
Based on these actions we will make a reward system.
If the agent tries to go off the field, punish with -10 in reward.
If the agent makes a (legal) move, punish with -1 in reward, as we do not want to encourage endless walking around.
If the agent tries to pick up item, but it is not there or it has it already, punish with -10 in reward.
If the agent picks up the item correct place, reward with 20.
If agent tries to drop-off item in wrong place or does not have the item, punish with -10 in reward.
If the agent drops-off item in correct place, reward with 20.
That translates into the following code. I prefer to implement this code, as I think the standard libraries that provide similar frameworks hide some important details. As an example, and shown later, how do you map this into a state in the Q-table?

# Demo adding
demo adding