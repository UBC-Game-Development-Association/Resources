# Unity: The Basics

## How do I get an object to move via script?

There's two ways to do it.

### Directly modify transform position

If you're not too worried about collisions or doing this movement as a one-off, you could simply directly modify the transform's position:
```csharp
public class YourBehaviour : MonoBehaviour
{
    //...

    private void Awake() {
        transform.position = new Vector3(5, 6, 7);
    }
    //...
}
```

Alternatively, you could modify the local position of the object via `transform.localPosition` if you want to modify it relative to its parent.

However, keep in mind doing modifications in local space would also use any local rotations and scaling (see below as an example).

![Objects moving in local and global space](./LocalVsGlobal.gif)

### Using Rigidbodies

Note there's a pitfall with constantly moving objects: they would need Rigidbodies in order for collisions to be consistently detected.

![Example of when collisions are not detected](./RigidbodyOrNot.gif)

If the object will be repeatedly moving, it would be better to give the object a Rigidbody before performing motion to allow better collision detection.

```csharp
public class YourBehaviour : MonoBehaviour
{
    //...
    private Rigidbody _rigidbody;
    private void Awake() {
        // since Update() runs every frame, it's better to not call GetComponent every frame since it's not performant
        // thus we save it here
        _rigidbody = GetComponent<Rigidbody>();
        // if 2D, use GetComponent<Rigidbody2D>();
    }
    //...

    private void Update() {
        // instantly moves from A -> B, in world space
        _rigidbody.position = new Vector3(5, 6, 7);
        // moves (interpolating in between) from A -> B in 1 physics update (approximately 0.02 seconds)
        _rigidbody.MovePosition(new Vector3(5, 6, 7);
    }
    //...
}
```

Alternatively, you can modify the rigidbody's velocity instead, especially if you want it to obey physics:

```csharp
public class YourBehaviour : MonoBehaviour
{
    //...
    private Rigidbody _rigidbody;
    private void Awake() {
        _rigidbody = GetComponent<Rigidbody>();
    }
    //...

    private void Update() {
        // instantly sets velocity
        _rigidbody.velocity = new Vector3(5, 6, 7);
        // applies a force; there's multiple types:
        //  - Force (the default): modifies velocity by inputVector * Time.fixedDeltaTime / _rigidbody.mass
        //  - Acceleration: modifies velocity by inputVector * Time.fixedDeltaTime
        //  - Impulse: modifies velocity by inputVector / _rigidbody.mass
        //  - VelocityChange: modifies velocity by inputVector
        _rigidbody.AddForce(new Vector3(5, 6, 7));
        _rigidbody.AddForce(new Vector3(5, 6, 7), ForceMode.VelocityChange);
    }
    //...
}
```

There's a few other methods as well, see Unity's documentation for more: ([Script reference](https://docs.unity3d.com/ScriptReference/Rigidbody.html), [Manual](https://docs.unity3d.com/Manual/RigidbodiesOverview.html)).
