# Redirecting-the-scene
## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
### Step 1:
To open the unity engine.

### Step 2:
Create a new plane and create a cube and give color for the cube.

### Step 3:
Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

### Step 4:
Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

### Step 5:
Create the C# script file in the Assets and write the Coding for the Redirecting to the page2 after hit the sphere to cube.

### Step 6:
Next Create a another new scene named as page2.

### Step 7
In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.

### Step 8:
Click the Build and run button in the Build settings and run the scene.

### Step 9:
The Sphere after touching the cube it will disappeared and Press the key [R] the redircting to the new scene that is page2.

## Program:
```
DEVELOPED BY: KRISHNA PRAKAASH D M
REG NO: 212221230052
```
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class CubeProg : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("level2");
        }
    }
    public void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "Sphere") 
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
```

## Output:
### Scene 1:
![EX7](https://github.com/Krishna-Prakaash/Redirecting-the-scene/assets/93427144/5698ed4b-53aa-4cca-8d8d-ad2f3cf1e7c2)

### After the Ball Hit the cube:
![op1](https://github.com/Krishna-Prakaash/Redirecting-the-scene/assets/93427144/427bc10d-4038-4e4c-9b5e-a985236eedd0)

### Redirected scene 2:
![op2](https://github.com/Krishna-Prakaash/Redirecting-the-scene/assets/93427144/f0a75fa4-746d-422d-9d1e-311caa9bd69e)


## Result:
The above C# coding is successfully redirecting the scene in the unity engine.
