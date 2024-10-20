# Unity

Supports 2D/3D games for most common platforms; note that other build platforms (e.g. web, native iOS) may require additional components.
Programming is done in C#, but I believe there is optional visual scripting.

<!-- Asset files are by default saved to text, making Git merge conflicts easier to resolve.
    
    Actually the only engine that doesn't do that is Unreal - maybe I can omit this?
-->

## Glossary
Sometimes, it can be hard to keep track of what each thing means, so just to make things easier in the beginning, here are some common words that will be popping up.

**GameObject**: Basically, everything you place in the game will be a GameObject with some added behaviour through _components_. Gameobjects are unique; every time you place one, they will be different from others unless made with a prefab. GameObjects can be seen on your scene or hierarchy view. E.g. an enemy, box, bridge, bullet etc;

**Component**: In unity, components give behaviours to most things; they can be added to objects to provide particular properties and store information. They can be found in the details view when a GameObject is selected. E.g. a player's inventory, an enemy's AI, or what makes a wall stop you from going through it.

**Prefab**: a "blueprint" of an object and its components; this allows us to place multiple of the same object and change all of them in the same place instead of one by one. Done by moving an object in a scene back into the assets screen in unity. Located in the assets folder. For example, a generic version of a bullet is used every time a shot is fired to create the bullet object in the game as a copy of it.

**Scene**: A file that holds all the information we want on a screen/level; it contains the camera, UI, and all objects and their positions, etc. All configurations made inside a scene are unique (unless you are working with prefabs. E.g. a Mario level, the entire snake game, etc.

**Inspector**: The panel in Unity that display's a GameObject or Component's data. Can be customized (i.e. a custom inspector).

![Inspector screenshot](Unity/Inspector.png)

**Editor**: Typically refers to the Unity Editor - what you use to modify the game. May also refer to Custom Editors for objects (e.g. custom inspectors).

**ScriptableObject**: A data container to contain shared data in the project, typically saved to an asset in the project.

<!-- Might include UnityEvent/MonoBehaviour/Sprite/Mesh, but that could be too specific?-->