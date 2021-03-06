V 3.1.3, Work In Progress
-------------------------
- input uses its own update loop using Event.FRAME_CONSTRUCTED.
- fixed a bug in Keyboard's input where some actions weren't performed.
- fixed a problem with parallax when zooming.
- Nape's Hero no longer has a static friction.
- fixed Nape's Hero was able if the collisionAngle was really close to 0.
- moved SpriteDebugArt and StarlingSpriteDebugArt into their respective package.
- SpriteArt/StarlingArt/Away3DArt content property becomes private with a getter. It should only be set internally.

V 3.1.2, 01 17 2013
-------------------
- improved physics performance removing the update call to the debug view if it isn't visible.
- outsourced camera stuff into a ACitrusCamera class and one camera by view : BlittingCamera, SpriteCamera, StarlingCamera and Away3DCamera2D.
- renamed CitrusView into ACitrusView class.
- addSound method has now two arguments : the id (String) and the sound (*, String or Class).
- added CitrusGroup class to group different kind of objects.
- added createAABB method in MathUtils package.
- added CollisionGetObjectByType into Box2DUtils and NapeUtils.
- added getObjectsByName method.
- added a fla with Citrus objects components to create quickly objects using Flash Pro as a level editor.
- you can change physics step thanks to their public var.
- updated on Starling 1.3.
- fixed a bug where the group property wasn't updated using Away3DView, SpriteView and StarlingView.
- fixed on StarlingArt, the object's view changed but animation doesn't update on the new view.

V 3.1.1, 12 20 2012
-------------------
- created starling and away3d package in citrus.core for StarlingCitrusEngine, StarlingState, Away3DCitrusEngine and Away3DState classes.
- removed stage argument in setUpStarling function, override the handleAddedToStage method to call setUpStarling function instead.
- added Nape parser for polygon/polyline.
- AVirtualJoystick : action value scaling.
- TimeShifter now listens to and routes input to his defaultChannel which remains channel 16 when instanciated.
- fixed a bug where Starling couldn't dispose.
- fixed a bug on TimeShifter using params.
- fixed camera offset for BlittingView.

V 3.1.0, 12 14 2012
-------------------
- Renamed package "com" and "citrusengine" into "citrus".
- The LevelManager can load levels made with Flash Pro on iOS using a LoaderContext.
- The setUpStarling function may take the flash stage as an argument (useful if not the root class).
- AnimationSequence's dictionary is now accessible thanks to a getter.
- Changed _input to protected to allow custom Input.
- Added the new input package supporting keyboard, joystick, button, channel, key action...
- Added a TimeShifter à la Braid! Allow also to replay an action.
- Upgraded on Nape 2.0.
- Nape's gravity is equal to Box2D's gravity.
- Nape's object physics behavior are closed to Box2d one (friction, speed, hero & enemy interaction...)
- refreshPoolObjectArt handles the startIndex.
- Now we can easily read the velocity of a body thanks to a getter.
- Thanks to ObjectMaker we can define vertices using Tiled Map Editor software.
- Update on Starling RC 1.3 + added its new AssetManager class.
- StarlingArt is now able to dispose automatically basic DisplayObject.
- Starling's AnimationSequence has a clone method.
- Starling's AnimationSequence dispatch onAnimationComplete Signal

V 3.0.4, 11 29 2012
-------------------
- DragonBones support for StarlingArt class.
- Moved ObjectMaker2D & 3D classes and tmx package into a new objectmakers package.
- Create a new ObjectMakerStarling class with a parser for Tiled Map Editor’s files optimized for Starling. 

V 3.0.3, 11 28 2012
-------------------
- optimized MathVector class.
- a PoolObject can be rendered through the State/StarlingState classes.
- the LevelManager class can load tmx file.
- ATF file format are supported by the StarlingTileSystem class.
- tiled map objectmaker uses dynamic tileset name.
- ObjectMaker FromTiledMap support now multipe tileSets.
- added a RevolvingPlatform in box2d platformer’s package.
- the Starling’s AnimationSequence class has a new parameter : the smoothing. Default is bilinear.

V 3.0.2, 11 20 2012
-------------------
- fixed a bug where the MovingPlatform speed parameters wasn’t applied.
- fixed a critical bug using Android where the state could be instantiated before the context3D is created.
- fixed a bug if a flash display object was added using StarlingState, there were a problem destroying the state due to the physics debug view.
- the entity/component system works fine now with Box2D pure AS3 and enable interaction with “normal” object.
- all Box2D objects implements the IBox2DPhysicsObject interface.
- CollisionGetOther CollisionGetSelf Rotateb2Vec2 functions have moved into a new class : Box2DUtils
- Box2DShapeMaker class moved into physics/box2d package

V 3.0.1, 11 16 2012
-------------------
- fixed a bug on Nape’s Hero colliding with a Sensor.
- fixed a bug where the Box2D Hero was able to double jump thanks to a Sensor or a Cloud.
- fixed a bug where a passenger falls on a Moving Platform if it changes direction to downward.
- optimizing States loops.
- an Enemy doesn’t move anymore during the period it is hurt (don’t forget it is killed after this period).
- Hero switches facing direction while in mid-air.
- DistanceBetweenTwoPoints method added in MathUtils.
- CitrusEngine’s handleAddedToStage method is now protected.
- Adding auto setting of a component’s entity when adding to an entity, also added 2 utilites that search for a component by class type.
- Frame Rate Independent Motion support added!

V 3.0.0, 11 6 2012
------------------
- Moved from Box2D Alchemy to Box2D pure AS3 for better performance
- Starling support
- Nape physics engine supported with some pre-built platformer objects
- Level Manager and an abstract game data class
- Object Pooling and Entity/Component System
- Away3D support
- AwayPhysics support
- New Level Editor handlers for: Tiled Map and Cadet 3D.
- Lots of examples with assets
- A new forum on Starling’s website
- Other cool features and performance improvement