# Aneonen_Miscellaneous

This repository contains the Aneonen Miscellaneous package. Add it to BEE2 by downloading the aneonen_misc.bee_pack file and placing it with your BEE2 packages. There is no guarantee that the package will function in BEE2 versions older than 4.41. If you wish to try, you may need to unpack the .bee_pack file and re-pack it as a .zip file.

# Item List

A thorough description of the items and their functions. Ordered by significance.

## Check and Timer Indicator Panels
![indicators](https://user-images.githubusercontent.com/126639978/222040993-ea444d0c-76eb-44ff-91de-be5094a3e063.jpg)

Placeable checkmarks and timers that appear identical to the standard connection indicators generated by the puzzlemaker.  
They use the quarter tile editor model, and function similarly; use the widget to reposition the indicator on a surface until it sits on the correct quarter tile. *Note that they will always automatically right themselves when placed upon vertical surfaces.*   
Use **Start Reversed** to switch which set of 8 quarter tiles the indicator can be placed upon by moving the widget.

To activate either item, connect an input into the item. Make sure to set the indicator's connection visibility to none; *this item is best used with the antline corner and not standard puzzlemaker antlines.*

For the Checkmark, **Start Enabled** will start the Checkmark checked.  
For the Timer, **Start Enabled** will cause the timer to count down when activated. Otherwise, it will count down when deactivated.

For the Timer, **Start Open** will cause the timer to emit a ticking sound when counting down. Otherwise, it will be silent.  
The Timer item's **Timer Delay** controls the number of seconds the Timer will count down. 


## Angled Light Bridge
![angbridges](https://user-images.githubusercontent.com/126639978/222042368-f73665f5-7195-49d7-baa6-2ca8bf25d692.jpg)

An angled bridge emitter that sits upon a sliced 1x4x1-tile block. The item is templated, and so the block will change color per quarter-tile and will update between styles. However, the emitter itself will not.

**Cube Type** determines the angle at which the bridge will project, measured from the path the standard light bridge will take.
- *Standard* will position the emitter with the bridge extending at about 26.565 degrees, with a slope of 1/2. Note that this will function as if the emitter had been placed upon the "30" degree geometry block.
- *Companion* will position the emitter with the bridge extending at 30 degrees.
- *Reflective* will position the emitter with the bridge extending at 45 degrees.
- *Sphere* will position the emitter with the bridge extending at 60 degrees.
- *Franken* will position the emitter with the bridge extending at about 63.435 degrees, with a slope of 2. Note that this will function as if the emitter had been placed upon the "60" degree geometry block.   

The bridges can be positioned in 8 locations on a surface using the widget.   
By selecting **Start Reversed**, the bridge emitter will face towards the center of the surface instead of away from it.   

By unselecting **Start Opened**, the automatic portal magnet will disappear from the terminus of the bridge. This is useful if the bridge lines up well with an existing portal magnet.   

**Start Enabled** causes the bridge to start enabled.

## Angled Funnel
![angfuns](https://user-images.githubusercontent.com/126639978/222043314-00721604-a7e9-444f-8c55-9427d628fdd2.jpg)

Angled funnel emitters that are housed in larger blocks that occasionally extend out of the voxel they are supposed to occupy.   
The funnel's geometry will always be black, but is templated and will change with style. The emitter will not change with style.   
The funnel will not place an automatic portal magnet. 

This item uses A/B inputs in order to control connections to both state and polarity. See the **A/B Inputs** section at the bottom of this document for more information. 

**Start Enabled** and **Start Reversed** control the standard funnel properties.

**Cube Type** determines the angle at which the funnel will project, measured from the path the standard funnel will take.
- *Standard* will extend a funnel at about 26.565 degrees, with a slope of 1/2. Note that this will function as if the emitter had been placed upon the "30" degree geometry block.
- *Companion* will extend a funnel at 30 degrees.
- *Reflective* will extend a funnel at 45 degrees.
- *Sphere* will extend a funnel at 60 degrees.
- *Franken* will extend a funnel at about 63.435 degrees, with a slope of 2. Note that this will function as if the emitter had been placed upon the "60" degree geometry block.   

**Start Open** will change the position of the funnel slightly with dependence on *Cube Type*. This will cause the funnel to always hit the center of certain surfaces.   
When the funnel is angled upon the edge of a surface, the center of the funnels path won't necessarily travel through the center of surfaces, which can lead to odd results if the designer wishes to have the funnel project onto a portal surface on a wall/floor/ceiling. The 30 and 60 degree variants, which have irrational slope, are somewhat unpredictable and thus are not used when *Start Open* is checked.    
Below, references to 'parallel' and 'perpendicular' are with respect to the surface the funnel item is placed upon.
**When Start Open is Checked:**
- *Standard* will move the shallow funnel forwards slightly such that it hits the center of parallel surfaces.
- *Companion* will be switched to the *Standard* funnel and raised by a half-voxel such that the funnel hits the center of perpendicular surfaces.
- *Reflective* will move the 45 degree funnel forwards by almost a quarter tile such that it hits the center of both parallel and perpendicular surfaces.
- *Sphere* will be switched to the *Franken* funnel and raised by a quarter-voxel such that it hits the center of parallel surfaces.
- *Franken* will move the steep funnel forwards slightly such that it hits the center of perpendicular surfaces.   

If this is confusing, I recommend you experiment with the option when you wish an angled funnel to very predictably hit the center of a wall/floor/ceiling surface.


## 45-Degree Block Stairs
![45stairs](https://user-images.githubusercontent.com/126639978/222044974-579e809b-060a-4a17-bcf7-267772290b06.jpg)

Steeper block stairs that allow players to ascend one voxel without using a slope.   
They are templated, and so will change with styles and quarter-tile colors, but are not guaranteed to look well in any style other than clean.    

**Start Enabled**, when checked, will cause the item to use the denser, flat stairs seen on the right of the attached image.   
Otherwise, they will use the semi-sloped, quarter-tile sized stairs on the left of the attached image.
The stairs feature player clips and thus the differences between the two types are effectively aesthetic, up to interactions with physics objects.  

The stairs can be combined to make larger staircases if desired.
**Cube Type** changes the particular component of a larger staircase the item will become.
- *Standard* is the normal 1-voxel-wide staircase with two edges.
- *Companion* will place the *left edge* of a larger staircase.
- *Reflective* will place any *middle piece* of a larger staircase.
- *Sphere* will place the *right edge* of a larger staircase.
- *Franken* will place block stairs that are not meant to be used with edges and which can be combined freely, like the usual BEE2 block stairs.


## Flipped Steep Geometry Block
![flippedblocks](https://user-images.githubusercontent.com/126639978/222045783-13575d5e-11fc-4437-8348-9e3f8f881b2b.jpg)

A flipped version of the standard "60" degree geometry block. This has only been performed for some easier placement/construction. There is nothing else to say.

## Arrow and Diagonal Arrow Signage
![arrowsignage](https://user-images.githubusercontent.com/126639978/222190450-07b19bfe-b719-41c4-906f-1bd5264ab7dd.jpg)

Extra signage that features 512x512 directional arrows and diagonal arrows. Best used when **Start Enabled** (which adds a standard arrow) is not checked on the signage item.


## Glass Box
![glassbox](https://user-images.githubusercontent.com/126639978/222046205-32d820f1-4bde-43a6-8de8-3dbba2ffae3d.jpg)

Small glass boxes that come in three kinds. These are designed to protect relays when allowing lasers to be intersected too close to them is dangerous for a puzzle. They can also be placed over static cubes when the cubes have been placed in certain positions.

**Button Type** changes which glass box is set. 
- *Weighted* will place a 2x2x2 glass cube.
- *Cube* will place a 4x2x2 glass box.
- *Sphere* will place a 4x4x2 glass box. 

Because we cannot inherit the usual handle for relays, we use **Cube Type** to simulate the correct positioning.   
First, rotate the item to face in a desired direction. Then:
- *Standard* will place the box in the center of the surface.
- *Companion* will displace the box forwards in the direction it is facing to the position of a offset relay.
- *Reflective* will perform the same action as *Companion* but with a single clockwise turn.
- *Sphere* will perform the same action as *Companion* but with two clockwise turns.
- *Franken* will perform the same action as *Companion* but with three clockwise turns.


## Large Funnel Emitter
![largefun](https://user-images.githubusercontent.com/126639978/222047127-8bb3e46c-6cfd-406d-996b-524e6de37350.jpg)

A large funnel emitter, as seen in the campaign.   
Takes up more embed space than the usual funnel, and must be used more carefully.   
The funnel itself is not any larger; only the emitter, which makes the item a purely visual addition. 

This item uses A/B inputs in order to control connections to both state and polarity. See the **A/B Inputs** section at the bottom of this document for more information. 

**Start Enabled** and **Start Reversed** function as they do on the standard funnel item.


# A/B Inputs

An item using A/B inputs can control two different outputs at once by activating connections through the *A/B Input* item.   
The item comes with standard BEE2 packages and is associated with the *SR Latch*.   
In the case of this package, *Input A* will always control funnel state and *Input B* will always control funnel polarity.   
To hook up these items to a funnel,
1. Place the *Input A* and *Input B* items into the map.
2. Connect *Input A* and *Input B* **into** the desired item.
3. Connect all inputs which you wish to activate the item's first output into *Input A*.
4. Connect all inputs which you wish to activate the item's second output into *Input B*.
