---
layout: post
title: "BGE using collision sensor"
date: 2014-05-15 23:17:49 +0800
comments: true
categories: BGE
---
### Environment: ###
Blender 2.69


### Concept: ###
The BGE **Collision Sensor** can detect collision of object with `property`. Yes ! You declare a `property` in the object A, then the other object B _can observe any colliding object_ who carries the `property`, and take the **Actuation**.
<!--More-->
Simple enought? Yes! only be careful for some settings ...


### Prepare to make it ! ###

Open Blender, load factor settings.

Select Game Logic layout, and select Blender Game renderer.

Add 3 Cubes, given names of "Player" "Gate" and "Box". The "Player" is the one we can move, the "Gate" will be a **Near Sensor**, the "Box" will be a **Collision Sensor**.


### Important: add property ###

Select "Player", in **Properties Window** (on lower left), add `hero` property for it.


### Configure movements ###

Add 4 (forward, backword, left, right) **Key Sensors** for "Player".

(Fig: "Player" object)
![Player](http://coding-addict.com/pictures/blender/bge_collision_sensor_player_obj.png)

### Configure Gate (test Near) ###

Add **Near Sensor** for "Gate" object, observe `hero` in the sensor's **property**, set **Distance**/**Reset Distance** to 3.00, then add an **And** controller, a **Motion Actuator** for it, and set **Rot:** z for `2` degrees. Remember to connect them.

(Fig: "Gate" object)
![Near](http://coding-addict.com/pictures/blender/bge_collision_sensor_near_obj.png)


### Configure Box (test Collision) ###

Add **Collision Sensor** for "Box" object observe `hero` in the sensor's **property**, then add an **And** Controller, a **Motion Actuator** for it, and set **Rot:** z for `-2` degrees. Remember to connect them:

(Fig: "Box" object)
![Near](http://coding-addict.com/pictures/blender/bge_collision_sensor_collision_obj.png)

### Important: set Physics Property ###

For "Box" object, set **Physics Type** in **Physics Property** (lower right window) to **Sensor**. (see Fig: "Box object")

For "Player" object, set **Actor** in **Physics Property** (lower right window) to be checked. (see Fig: "Player object")


### Conclusion ###

Why the **Collision** should be **sensor** instead of being **static** in the **Physics Property**? This is the **MOST** error prone place when configuring the **Collision Sensor**. Indeed, to figure out how to make it working, I have wasted nearly 2 days on it. #

Note: [The final .blender file](http://coding-addict.com/pictures/blender/collision_test.blend)

