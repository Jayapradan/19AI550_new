# Ex.No: 3  Basic movements in Unity 
### DATE: 24/07/2026                                                                          
### REGISTER NUMBER : 212224240061
### AIM: 
 To learn the basic movements translation,scaling and rotation of game objects through code.
### Procedure:
1. Setup the Scene
2. Open Unity and create a 3D Scene.
3. Add three objects:Cube → Rename to Object1 (for movement),Sphere → Rename to Object2 (for rotation).Capsule → Rename to Object3 (for scaling).
4. Add the Script,Create a C# Script → Name it TransformOperations.cs.
5. Write the code for translation,scaling and rotation,save and close the script
6. Save the script
7. Select any empty GameObject (or create one: GameObject → Create Empty).
8. Attach the TransformOperations script to it.
9. In the Inspector, assign Object1 → Drag the Cube,Object2 → Drag the Sphere.Object3 → Drag the Capsule.
10. Run the Scene Press Play ▶️ in Unity
11. Stop the program.
### Program 
```
using UnityEngine;
public class TransformOperations : MonoBehaviour
{
    public Transform object1; // Object for translation
    public Transform object2; // Object for rotation
    public Transform object3; // Object for scaling

    public float moveSpeed = 2f;  // Speed of translation
    public float rotateSpeed = 50f; // Speed of rotation
    public float scaleSpeed = 0.5f; // Speed of scaling

    void Update()
    {
        // Translate (Move) object1 along the X-axis- Time.deltaTime to make movement smooth across all frame rates
        if (object1 != null)
        {
           // object1.position += Vector3.right * moveSpeed;
               object1.Translate(0.02f,0,0);

        }

        // Rotate object2 around the Y-axis
        if (object2 != null)
        {
            //object2.Rotate(Vector3.up * rotateSpeed * Time.deltaTime);
            //object2.Rotate(0,0.02f.0);
        }

        // Scale object3 up and down
        if (object3 != null)
        {
           // float scaleChange = Mathf.PingPong(Time.time * scaleSpeed, 1f) + 0.5f; // generates a value that moves back and forth between 0 and length
           // object3.localScale = new Vector3(scaleChange, scaleChange, scaleChange);
            object3.localScale+=new Vector3(0.02f.0.02f,0);

        }
    }
}
```
OR
```
using UnityEngine;

public class program : MonoBehaviour
{
    // Start is called once before the first execution of Update after the MonoBehaviour is created
    public Transform o1;
    public Transform o2;
    public Transform o3;
    void Start()
    {
        print("welcome");
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyUp(KeyCode.X))
        {
            o1.Translate(0.2f, 0f, 0f);
        }
        if (Input.GetKeyUp(KeyCode.Y))
        {
            o2.localScale += new Vector3(2f, 2f, 2f);
        }
        if (Input.GetKeyUp(KeyCode.Z))
        {
            o3.Rotate(0f, 2f, 0f);
        }
    }
}
```
### Output:
<img width="1536" height="863" alt="image" src="https://github.com/user-attachments/assets/e2bf6bbd-548a-4225-948b-a0fb3b625ba2" />

<img width="1535" height="863" alt="image" src="https://github.com/user-attachments/assets/e7fad96d-a0d4-4d20-a833-f2daf6891f82" />







### Result:
Thus the basic movement is learned through scripting


