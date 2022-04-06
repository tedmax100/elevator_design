# Design an Elevator System

## An elevator system design question

## Requirements

1. An elevator can open, close, move, stop
2. Elevator door can only open when it is stop in a floor (i.e. not moving)
3. An elevator can transfer passengers from one floor to another floor

### Additional requirements

1. Two control directions
   1. external request; this request will be having the direction(move up/down) and the floor on which the button has been press by the user i.e. source floor. The elevator will check the available requests if any and then process this request depending on some priority. The elevator reaches the source floor.
   2. internal request; the passenger press 5th floor button in the elevator to indicate the elevator to go to 5th-floor. When reaching the target floor and the elevator stopped the passenger then exits the elavator.
2. If suppose when the elevator is moving from the 1st-floor to the 5th floor and it reaches the 2nd-floor. At this moment, another person on the 2nd-floor want's to go in the UP direction. Then the elevator will stop for this request.
3. If suppose when the elevator is moving from 1st-floor to the 5th-fllor and it reaches the 2nd-floor. At this moment another person on the 2nd-floor want's to go in the DOWN direction. Then the elevator will not stop for this request.

## Test Cases

1. Assertion state  

   - When the elevator is moving, then it can stop.

   - When the elevator is stopped, then it can open or move.

   - When the elevator is opened, then it can close.

   - When the elevator is closed, then it can open/move/stop.

2. Assertion direction
   - When the elevator is moving up from 2F to 6F, the passenger at 3F press UP, then the elevator will stop at 3F.

   - When the elevator is moving up from 2F to 6F, the passenger at 3F press DOWN, then the elevator will not stop at 3F.

   - When the elevator is moving up from 2F to 6F, the passenger at 1F press DOWN, then the elevator will keep the request.