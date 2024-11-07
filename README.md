# traffic-lights-state-machine
Initial State - "All Lights Orange":

The system begins with all traffic lights set to orange as a cautionary measure.
This state is the default for system startup or potential errors. If there's a system malfunction, the lights will revert to "All Lights Orange" for safety.

State 1 - "E-W Green, N-S Red":

East-West (E-W) traffic lights are set to green, allowing traffic to flow in the east-west direction.
North-South (N-S) traffic lights are red, stopping traffic in the north-south direction to prevent collisions.
The system starts an E-W green timer during this phase.

State 2 - "E-W Orange, N-S Red":

When the E-W green timer expires, the E-W light transitions to orange as a warning that it will soon turn red.
N-S lights remain red, continuing to hold N-S traffic.
This state is brief, only lasting as long as it takes for the orange light to give a cautionary signal.
The transition to the next state happens automatically after a short delay, allowing E-W traffic to clear the intersection.

State 3 - "E-W Red, N-S Green":

E-W lights turn red, stopping traffic in the east-west direction.
N-S lights turn green, allowing traffic to flow north-south.
The system starts an N-S green timer for this state, controlling how long N-S traffic can move freely.

State 4 - "E-W Red, N-S Orange":

When the N-S green timer expires, N-S lights transition to orange to signal that they will soon turn red.
E-W lights remain red, holding E-W traffic.
Similar to the E-W orange phase, this state is brief, allowing N-S traffic to clear the intersection.
After this transition time, the system will cycle back to "E-W Green, N-S Red."

Cycle Repeats:

Once the N-S orange light expires, the cycle returns to "E-W Green, N-S Red."
This cycle continuously repeats, allowing each direction a fair share of time to move while avoiding traffic conflicts.
System Malfunction:

If a malfunction is detected, the system will switch to the "All Lights Orange" state to signal caution and ensure safety at the intersection until the issue is resolved.
