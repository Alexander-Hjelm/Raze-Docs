Scene Management
================

Each level is comprised of 5 scenes in total, one **common scene**, and 4 **difficulity scenes**. One difficulity scene is always loaded additively with the common scene when presenting a level in-game, depending on which difficulity is chosen by the player.

The **common scene** contains all level elements that will be presented in a specific level, regardless of difficulity, for example the player GameObject, the HUD, checkpoints and the camera.

The **difficulity scenes** contain level elements that are unique to the current difficulity mode. This includes all the enemy GameObjects.

Naming convention
-----------------

Naming convention for the common scene:

* Level_XX_common

Naming convention for the difficulity scenes:

* Level_XX_easy
* Level_XX_medium
* Level_XX_hard
* Level_XX_expert

where XX is the level number.

Load order
----------

Upon loading a new level, **Level_XX_common** must be loaded first, and then the specific diffiulity scene. **Important**: there may be no referencing between components from the difficulity scene to the common scene at Start() or Awake(). Use a registration pattern instead.


GameObject Hierarchy, Common Scene
==============================


Static
------------------

### Tag

*Untagged*

### Children

* Non-moving objects with collision data, such as boxes
* Plataforms with collision data and the PlatformEffector2D component
* World colliders (ground, right and left)

### Required components

* *None*


BG
------------------

### Tag

*Untagged*

### Children

* Non-moving objects which will be visible in the background, such as city and sky sprites.

### Required components

* Parallax Scroller


Zones
------------------

### Tag

*Untagged*

### Children

### Required components


Grid
------------------

### Tag

*Untagged*

### Children

* 2D Tilemaps without collision data

### Required components

* Grid


CameraParent
------------------

### Tag

*Untagged*

### Children

* The Main Camera object in the scene.

### Required components

* Camera Follow Behavior

Player
------------------

### Tag

Player

### Children

* Feet
* AttackTriggers

### Required components

* Sprite Renderer
* Animator
* Rigidbody 2D
* Box Collider 2D
* Hp
* Credit Counter
* Player Movement
* Player Attack
* Player Death
* Player Constants
* Ammo


PathfindingGraph
------------------

### Tag

PathfindingGraph

### Children

* Pathfinding nodes with the **Node.cs** component

### Required components

* *None*

Checkpoints
------------------

### Tag

*Untagged*

### Children

* Checkpoint objects with the **Checkpoint.cs**, **MusicTrigger** and **Collider2D** components.

### Required components

* *None*

UI
------------------

### Tag

*Untagged*

### Children

* UI Canvases

### Required components

* *None*


EnemyManager
------------

### Tag

EnemyManager

### Children

* *None*

### Required components

* Positional Awareness
* Enemy Notification Manager