
# Table of Contents
1. [Required Components](#required_components)
2. [Optional Components](#optional_components)
2. [Animation State Machine](#animation_state_machine)

Required Components <a name="required_components"></a>
===================

Sprite Renderer
---------------

Box Collider 2D
---------------

Animator
--------

### Parameters
* **Controller**: assign the animation controller to be used.

Rigidbody2D
-----------

### Parameters
* **Constraints**: *Freeze Rotation* must be checked.

Character Constants
-------------------

### Parameters
* **Hp**: the maximum hitpoints of the enemy.
* **Walk Speed**: how fast the enemy walks.
* **Jump Height**: how high the enemy jumps.
* **Knockback Resistance**: any knockback applied to the enemy will be reduced by this factor.
* **Gravity Scale**: the gravity of the enemy will be multiplied by this factor.

AI Pathfinding
--------------

### Parameters
* **Path Efficiency Distribution**: a curve that determines how likely the enemy is to take a path depending on its length.
	- X-axis: the relative efficiency of a path, compared to the shortest path (1 = length equal to the shortest path, 0 = path length is infinite)
	- Y-axis: the tendency to choose a path at the corresponding x-value.

AI Movement
-----------

### Parameters
* **Jump Audio**: the FMOD Audio Event which is played when the enemy jumps.

AI Death
--------

AI Awareness
------------

### Parameters
* **Aware Icon**: the prefab of the icon which is displayed above the enemy when they become aware of the player. Found at *Assets/Prefab/Attention*.
* **Aware Audio**: the FMOD Audio Event which is played when the enemy becomes aware of the player.

AI Combat Behaviour
-------------------

### Parameters
* **Min Dist To Player**: how closely the enemy follows the player at a minimum during the combat state.
* **Max Dist To Player**: how closely the enemy follows the player at a maximum during the combat state.
* **Prioritized Dist To Player**: how close the enemy prefers to stay to player during the combat state.

AI Attack
---------

### Parameters
* **Melee Range**: how close the enemy must be to the player until they can attack.

Hp
--

### Parameters
* **Hit Audio**: the FMOD Audio Event which is played when the enemy is hit.

Knockback
---------

Credit Drop
-----------

### Parameters
* **Drop Amount**: how many credits the enemy will drop upon dying.
* **Green Credit Prefab**: the prefab of the Green Credit GameObject. Found at *Assets/Prefab/CreditGreen*.
* **Silver Credit Prefab**: the prefab of the Silver Credit GameObject. Found at *Assets/Prefab/CreditSilver*.
* **Gold Credit Prefab**: the prefab of the Gold Credit GameObject. Found at *Assets/Prefab/CreditGold*.

Invincibility Manager
---------------------

### Parameters
* **Invincible Time**: how many seconds the enemy is invincible for after being hit.
* **Invincible During Recoil**: will the enemy will get invincible in the Recoil state (after being hit)?

Recoil
------

Blink Animation
---------------

### Parameters
* **Alpha High**: the upper transparency level in the blinking animation.
* **Alpha Low**: the lower transparency level in the blinking animation.
* **Interval**: how fast (in seconds) the enemy will blink upon dying.

Audio Reaction
--------------

Optional Components <a name="optional_components"></a>
===================

AI Shield Behavior
------------------

Animation State Machine <a name="animation_state_machine"></a>
=======================