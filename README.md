# WeaponController

Add and combine all these components to different 3D objects in order to be able to shoot a gun, switch between different guns and be able to destoy other game objects with health.

## Contents

This component is made from the following behaviours:
- `Weapon Controller`

And the following states:
- `Gun`
- `WeaponSwitching`
- `Target`
- `BulletDestroy`

### Gun

This state allows us to use any object as a weapon by clickin our mouse left button. It will instantiate a bullet prefab everytime we press the button. For this to work, this state will need to be added to all the weapons we have, in the inspector we will need to set the suitable gun's damage and range, the preferred camera from our character player needs to be dragged and lasty the bullet prefab and its force. This state will also shoot a Raycast and will show us the name of the object we are hitting in the console.

### WeaponSwitching

 This state allows you to use the mouse wheel to scroll through an array of weapons. For this to work, an empty object needs to be created and added to the camera that is within the character controller. After creating the empty game object, our weapons will need to be dragged as children objects in the order we prefer, this will be the order of our array. The state is then added to the empty object in order to control the weapons. One of them should be visible and the other two should be not visible.

### Target

When added to any 3D object with a collider, this state will give health to the chosen object and will make it disappear or destroy itself when the suitable health goes below 0. The object's health can be changed in the inspector when the state is added to any object.

### DestroyBullet

This state will simply make the chosen bullet disappear or destroy itself when in contact with an object containing a collider. This state needs to be added to the bullet object prefab. Its object collider will need to be ticked as `is Trigger`.

