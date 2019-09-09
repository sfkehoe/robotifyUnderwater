Module 1 - 3D Movement
======================

## Task 1 -

### Overview
With the vertical depth part of our code taken care of it's time to start working on getting L1-R moving around a bit more. As an ROV, L1-R runs on a propeller system for moving forward and backward. We control that with a simple rudder system that we can use for setting the turning radius of the ROV.

Now the ROV has a minimum turning radius of XXX, we need to take that into account when L1-R is moving. We also need to take into account collisions and some collision avoidance.

For now, let's get to grips with moving L1-R through some turns. We've disabled the functions you built earlier, we'll add them back in once you've got this part of the movement process down.

### Instructions
* Add a `count with [j] from [] to [] by []` block to the workspace
* Slot a `set [vertical] propeller thrust to []N` block inside the loop, change the drop-down to `horizontal`.
* Populate the loop with blocks to set the horizontal thrust to values from 1000N to -1000N in steps of -200N.
* Add wait times of 2 seconds inside the loop after the thrust setter step.

## Task 2 -

### Overview
We use a steering rudder to change the direction of thrust for the horizontal propeller. It's a reliable method of steering but it does mean we can't turn on a dime or spin in place.

The rudder position is measured in degrees from neutral to either port (left) or starboard (right). We have an abosolute limit of 45º from neutral on both sides. So with that in mind it's time you took L1-R through some horizontal turns.

### Instructions
* Add a counting loop to the workspace set it to count from 0 to 45 by 5.
* Slot a `set rudder to [] degrees to [port]` inside the loop, slot a `k` iterator into the degrees slot.
* **Duplicate** the rudder control block, slot the new block under the original in side the loop, change the drop-down to starboard.
* Slot wait blocks below each of the rudder control blocks, set them to 3 seconds. 

## Task 3 -

### Overview

### Instructions
* 
*
*
*
*

## Task 4 -

### Overview

### Instructions
*
*
*
*
*

## Task 5 -

### Overview

### Instructions
*
*
*
*
*
