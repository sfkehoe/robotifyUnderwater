Module 1 - 3D Movement
======================

## Task 1 - Ballast

### Overview
Welcome to ScrapCorp, the remotely operated vehicle (ROV) powered salvage company. Today is your induction day and we're going to get you working straight away by understanding and programming our remote ROV L1-R, or Lir. 

The first thing to get to grips with is depth; L1-R doesn't work like an airplane, you don't point it's nose at something and move there. Instead we use the fact that L1-R is neutrally buoyant to allow us to use the two vertical propellers to change its depth.

We can set the propeller speed of both the vertical propellers and the horizontal propeller seperately. This changes the amount of thrust they are going to produce. In the case of the vertical propeller a certain RPM setting will allow L1-R to float at a certain depth.

### Instructions
* In the `loops` drawer, find the `count with [i] from [] to [] by []` block, add it to the workspace
* In the `math` drawer, find the `number` blocks, slot three into the blank slots of the loop, set them to count from 2000 to 2500 by 20;
* In the `movement` drawer find the `set [vertical] propeller speed to []RPM` block, slot it inside the loop.
* Right click the loop, click **create get i**, slot the newly created `i` getter into the speed slot of the *propeller speed* block.
* In the `loops` drawer, find the `wait [1] seconds` block, slot it under the *propeller speed* block, set it to 5 seconds.

## Task 2 -

### Overview
We measure L1-R's depth by using a pressure sensor. We convert the pressure reading into a depth reading using a physics equation p = gdρ. In english that's pressure equals acceleration due to gravity times depth times density. So depth equal pressure divided by acceleration due to gravity times density. 

So we know that our depth in meters is equal to the pressure in kilo-Pascals (kPa) divded by 100.

Why don't you get experimenting with the vertical propeller velocities to figure out how our propellers affect depth.

### Instructions
* 
* In the `sensor` drawer, find the `pressure sensor` block,
*
*
*

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
