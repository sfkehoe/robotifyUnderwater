Module 1 - 3D Movement
======================

## Task 1 - Vertical Movement

### Overview
Welcome to ScrapCorp, the remotely operated vehicle (ROV) powered salvage company. Today is your induction day, and we're going to get you working straight away by understanding and programming our remote ROV L1-R, or Lir. 

The first thing to get to grips with is depth; L1-R doesn't work as an aeroplane, you don't point its nose at something and move there. Instead, we use the fact that L1-R is neutrally buoyant to allow us to use the two vertical propellers to change its depth.

We can set the propeller speed of both the vertical propellers and the horizontal propeller separately. The propeller speed changes the amount of thrust they are going to produce. In the case of the vertical propeller, a particular RPM setting will allow L1-R to float at a certain depth.

### Instructions
* In the `loops` drawer, find the `count with [i] from [] to [] by []` block, add it to the workspace
* In the `math` drawer, find the `number` blocks, slot three into the blank slots of the loop, set them to count from 2000 to 2500 by 20;
* In the `movement` drawer find the `set [vertical] propeller speed to []RPM` block, slot it inside the loop.
* Right-click the loop, click **create get i**, slot the newly created `i` getter into the speed slot of the *propeller speed* block.
* In the `loops` drawer, find the `wait [1] seconds` block, slot it under the *propeller speed* block, set it to 5 seconds.

## Task 2 - Pressure to Depth

### Overview
We measure L1-R's depth by using a pressure sensor. We convert the pressure reading into a depth reading using a physics equation p = gdρ. In English, that's pressure equals acceleration due to gravity multiplied by depth multiplied density. So depth equal pressure divided by acceleration due to gravity times density. 

So we know that our depth in meters is equal to the pressure in kilo-Pascals (kPa) divided by 10. Let's work on converting that using a function. 

### Instructions
* Create a function definition called `convertToDepth` with an input called `pressureIn` and a return value.
* Create a variable called `depthOut`, slot a `depthOut` getter in the return slot of the `convertToDepth` definition, slot a `depthOut` setter inside the definition.
* Get an `arithmetic` block from the `math` drawer, slot it into the `depthOut` setter, slot a `pressureIn` block into the left side, slot 100 in the right side.
* Use the drop-down on the `arithmetic` block to set the operation to multiplication.
* Slot a `print` block below the *wait* block inside the *loop*, slot a `convertToDepth` call in the `print` block, slot a `pressureSensor` block in the call.

## Task 3 - Investigating RPM to Depth

### Overview
Why don't you get experimenting with the vertical propeller velocities to figure out how our propellers affect depth. You can create a simple table of propeller RPM and depth in the terminal using the print blocks.

If we compare the propeller speed to the depth, we should be able to work out what the conversion factor from propellor speed to depth is. Then we can set depth directly using a function to convert depth inputs from the user to propellor speeds for the L1-R.

### Instructions
* Get a `print` block from the `text` drawer, slot it above the loop, slot a `string` block inside it from the `text` drawer.
* Set the `string` block to read " speed | depth ".
* Slot a `print` block below the *wait* block inside the loop, slot `create text with` block into this, click the blue cog, add an item to the *create text* block. 
* Move the `convertToDepth` call, slot it into the third create text slot, delete the now empty `print` block. 
* slot an `i` getter in the first create text slot, slot a `string` block set to  " | " in the second slot.

## Task 4 - Depth to RPM Converter

### Overview
Good work, you can work out from the table that the depth is related to the propeller speed by a factor of 1.25. So whatever propeller speed we set we the robot moves to a depth of 1.25 times that speed. A 2000RPM propeller speed gives us a 2500m below sea level depth, and a 2400RPM speed gives us a 3000m below sea level depth. 

Now we don't want to have to make guesses about RPM to depth measurements as we are trying to work with L1-R. Instead, let's add a user interface to input depth and set the appropriate propeller speed for what we want. Going by our conversion factor calculation, we can then get an RPM value by dividing the desired depth value by 12.5.

### Instructions
* Create a function definition called `convertToRpm`, with an input called `depthIn` and a return value.
* Create a variable called `rpmOut`, slot a getter into the return slot of the `convertToRpm` definition, slot a setter inside the definition.
* Slot a division `arithmetic` block into the `rpmOut` setter, slot a `depthIn` getter into the left side, slot a `number` block containing "1.25" into the right side.
* Slot a `convertToRpm` call into the *set vertical propeller speed* speed slot.
* In the `text` drawer, find the `prompt for [text] with message []` block, slot it into the `depthIn` slot, set it to [number], set the text to "Enter depth (meters): "

## Task 5 - Hit the Target Depths

### Overview
Time to look at implementing this into a user interface with the main function. Developing main functions allows us to compartmentalize the jobs of our program into useful chunks with very defined jobs. Functions are one way of doing that; classes in object-based programming languages is another. In our case, we'll work with functions.

You'll create the main function with no inputs or returns; it'll house a loop to make the core loop of our program. In our case, that core loop will ask for input to either set the depth or exit the loop. You'll use that to get to three different marked depths.

### Instructions
* Create a function definition called `mainFunction` with no inputs or return values, slot `repeat 10 times` loop inside it, set it t repeat 3 times.
* Slot the *"set propeller speed to [convert depth to rpm]"* blocks inside the loop.
* Set move the robot to the following depths: 2780m; 2655m; 2530m.