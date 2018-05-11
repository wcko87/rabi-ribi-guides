---
title: Map Transition RCS Setups
---

# Beach Skip (Running Method)

**Step 1:**
* Transition from beach to forest

**Step 2:**
* Hold left

**Step 3:**
* Switch from holding left to holding right at this exact frame (image).
* Do not leave any frames in between where you aren't holding any directional key.
* Continue holding right all the way.

![turning_point](https://user-images.githubusercontent.com/27341392/39659061-a41d458a-5052-11e8-8be1-df19f6c196fb.png)

### Demo:
<img class='gfyitem' data-id='FaroffPaleHarpyeagle'/>

### Additional Notes
1. Playing on keyboard makes this much easier. Hold down both left+right during the transition to forest. This makes you walk left. Let go of the left arrow key to start walking right.
    - pause menu buffer to switch directions might work for controller users(edited)
2. There is a recovery method if you turn around too early. Continue walking right, and turn around only after you pass the white flowers on the bush (see gif). Don't ever stop walking.
    - If you turn around before the white flowers, your alignment will be wrong later on.
    - Try not to turn around too late, or you would trigger the duck

### Explanation (not like it really needs any)
- doing an RCS by this method (walk at full speed, then immediately switch to holding the reverse direction) has a window of 0.28 pixels wide (smaller than the 3L1R method)
- doing the above setup puts you within this subpixel window

**Why the recovery method works:**
- The distance from where you spawn to the map transition point is approximately how far you need to walk to reach maximum speed. If you failed by turning around too early, it is likely that you did a full turnaround from maximum speed. To keep your subpixels, you'd need to mirror that action exactly. Walking all the way to the white flowers puts you at maximum walking speed, so turning around after that point gives a full turnaround at maximum speed, mirroring the previous action and keeping your subpixels.

-----------------------------

# Generalized RCS Setup
This works for any RCS. Note that event trigger RCS only works in v1.65 and below. In later versions, only map transitions RCS works.

![rcs_setup](https://user-images.githubusercontent.com/27341392/39659090-52d424fe-5053-11e8-975d-dbab3a33c39d.png)

### Diagram explanation:
- Red Area: event trigger you want to RCS
- Cyan Area: open space
- Green Area: ground

1 tile is 1 pixel. The numbers 1,2,3,4,5 represent how many pixels you are from the trigger

### Steps
**Step 1:**
* Stand on pixel 3. (use slow walk to inch into it)

**Step 2:**
* While holding slow walk, do "right 2 frames, left 1 frame" repeatedly to move 0.30 pixels right at a time, until you are in pixel 4.(edited)

**Step 3:**
* Let go of slow walk, do "right 2 frames, left 1 frame" once. (so you move 0.83 pixels right)(edited)

**Step 4**
* (don't hold slow walk) do "left 3 frames, right 1 frame"
* (note: don't hold any directional keys after you are done with the 'right 1 frame')(edited)

This will 100% give you an RCS. Buffer your actions with the item menu for 100% consistency.

<img class='gfyitem' data-id='ThatHarmoniousFallowdeer'/>

<img class='gfyitem' data-id='SelfreliantBoldFireant'/>

### Why it works:
* You can do an RCS by doing a "3 frames forward, 1 frame back" when standing between 3.797 and 4.162 pixels away from a trigger.
* This setup (steps 1-3) puts you between 3.83 and 4.13 pixels away from the trigger.


### Faster Method
You can chain the "right 2 left 1" etc. actions without leaving a frame in between for erina to stop moving. this can speed things up slightly

<img class='gfyitem' data-id='InnocentHappyHylaeosaurus'/>

* You can just execute all the actions in sequence without stopping in between
* In the gif: walking 2R1L, walking 2R1L, non-walking 2R1L, then non-walking 3L1R all in sequence
(note that releasing hammer mid-sequence is fine)

**Note:** If you are chaining, you have to drop the first input of each subsequent action (the input that usually does nothing)
* So it becomes `2R1L -> 1R1L -> 1R1L -> 2L1R` when chained.
