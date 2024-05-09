# Ex06-Redirecting-the-Scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
Step 1:
To open the unity engine.

Step 2:
Create a new 3D project.

Step 3:
Create plane and name it as ground and create cube and name it as player.

Step 4:
Add WinText in Hierarchy.

Step 5:
Create a C# Script and name it as playercontroller and add the script to player.

Step 6:
Use the R button to change the level2

Step 7
Print the Output and end the program.

## Program:
### NAME: JAYASRI DODDA

### REG NO: 212222240028
## PLAYERCONTROLLER
```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class playercontroller : MonoBehaviour
{
    // Start is called before the first frame update
    Rigidbody rb;
    public GameObject WinText;
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level2");
        }
    }
    private void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "sphere")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
```
## Output:
![Screenshot 2024-05-09 113231](https://github.com/jayasridodda/Ex06-Redirecting-the-Scene/assets/123259278/6d228c54-baae-4d6c-9e13-7976536e1a6c)
![Screenshot 2024-05-09 113013](https://github.com/jayasridodda/Ex06-Redirecting-the-Scene/assets/123259278/38899968-293d-4a40-889a-e4ca6b0bcb56)


## Result:

The above C# coding is successfully redirecting the scene in the unity engine.
