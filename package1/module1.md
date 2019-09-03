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

So we know that our depth in meters is equal to the pressure in kilo-Pascals (kPa) divded by 100. Let's work on converting that using a function. 

### Instructions
* Create a function definition called `convertToDepth` with an input called `pressureIn` and a return value.
* Create a variable called `depthOut`, slot a `depthOut` getter in the return slot of the `convertToDepth` definition, slot a `depthOut` setter inside the definition.
* Get an `arithmetic` block from the `math` drawer, slot it into the `depthOut` setter, slot a `pressureIn` block into the left side, slot 100 in the right side.
* Use the drop-down on the `arithmetic` block to set the operation to multiplication.
* Slot a `print` block below the *wait* block inside the *loop*, slot a `convertToDepth` call in the `print` block, slot a `pressureSensor` block in the call.

## Task 3 -

### Overview
Why don't you get experimenting with the vertical propeller velocities to figure out how our propellers affect depth. You can create a simple table of propeller RPM and depth in the terminal using the print blocks.

If we compare the propeller speed to the depth we should be able to work out what the conversion factor from propellor speed to depth is. Then we can set depth directly using a function to convert depth inputs from the user to propellor speeds for the L1-R.

### Instructions
* Get a `print` block from the `text` drawer, slot it above the loop, slot a `string` block inside it from the `text` drawer.
* Set the `string` block to read " speed | depth ".
* Slot a `print` block below the *wait* block inside the loop, slot `create text with` block into this, click the blue cog, add an item to the *create text* block. 
* Move the `convertToDepth` call, slot it into the third create text slot, delete the now empty `print` block, slot an `i` getter in the first create text slot.
* Slot a `string` block set to  " | " in the second create text slot.

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
