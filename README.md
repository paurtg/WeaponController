# WeaponController

Combining 
Add both of these states to a 3D object with a Player Controller component added to it. One state will allow you to move and control the character around the game scene, including the gravity element with ground checking and a jumping feature.
The other state will allow you to rotate the camera attached to a player, making it able to turn our character around.

## Contents

This component is made from the following behaviours:
- `Weapon Controller`

And the following states:
- `Gun`
- `WeaponSwitching`
- `Target`
- `BulletDestroy`

### Gun


### WeaponSwitching

 

### Target

When added to any 3D object with a collider, this state will give health to the chosen object and will make it disappear or destroy itself when the suitable health goes below 0. The object's health can be changed in the inspector when we add the state to any object.

### DestroyBullet

This state will simply make the chosen bullet disappear or destroy itself when in contact with an object containing a collider. This state needs to be added to the bullet object prefab. Its object collider will need to be ticked as `is Trigger`.

