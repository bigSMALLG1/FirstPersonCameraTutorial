# FirstPersonMovementTutorial
A tutorial on how to program first person movement in Unity 3D using C#. This tutorial also covers a jumping mechanic.

1.  Create a Unity 3D project.
2.  Before we start to program actual movement, the first step in this tutorial is to be able to move camera view in first person by moving the mouse.
3.  Right click in the project box at the bottom and create a MonoBehaviour script (Create ==> MonoBehaviour Script) and name it playerView.
4.  Delete the Start and Update methods.
5.  As always, we want to declare our variables. We are going to declare two float variables for the sensitivity in the x direction and the y direction. A Transform variable to store the orientation of the game object. Finally, create two more floats for the x and y rotation of the player camera.

![image](https://github.com/user-attachments/assets/394fdba2-2b82-45b7-9ca0-270d93449e2f)

6. Next, we can create a private void start method again, where we can lock the cursor and make it invisible, We put this in the start method so that the cursor is locked in the middle of the screen from the start of when the game is run and so that you can't see your cursor when playing.

![image](https://github.com/user-attachments/assets/83b9a065-fc10-4791-ae52-21b1d2adfc2e)

Cursor.visible is a boolean so setting this to false will render the cursor invisible.
Setting Cursor.lockState to CursorLockMode.locked will lock the cursor in the centre of the screen.

7. Next create the void update method again. We will be programming the physical mouse input here. To do this we will need to get our mouse's input in the x and y directions and multiply each by their corresponding x and y sensitivity variables that we set declared earlier. We will also multiply them by Time.deltaTime so that your computer performance won't matter.
 
![image](https://github.com/user-attachments/assets/abce57ad-8544-4dfb-92be-2609d1f170e4)

8. Below this, we will want to add the y rotation to the x input and subtract the x rotation from the y input.
![image](https://github.com/user-attachments/assets/83e3763c-40c8-4159-b709-7344df08b9ff)

9. After this, we want to make sure that the camera stops moving once you have looked up and down 90 degrees. So we will want to clamp the x rotation between -90 degrees and 90 degrees.
 
![image](https://github.com/user-attachments/assets/e7a010c2-e950-43f2-964f-f7a39dd9cf4a)

10. To apply this, we will use Quaternion.Euler. Quaternions are used to represent rotations in unity and euler returns a rotation that in the z, x and y axis. So a Quaternion.Euler represents the rotation of a game object in 3D. We will want to set a transform.rotation to this, as this is the transform attached to the game object allowing us to move our players camera in correspondence to the mouse. We will also want to do the same for the orientation so our actual gameobject will turn in accordance to the camera.
 
![image](https://github.com/user-attachments/assets/61f08f3d-a0c8-4297-bfc2-12c48f0ce798)

11. Go back in to Unity and create an empty game object called "Camera" and add a camera to this empty game object in the hierarchy and call the camera "PlayerCamera". We are doing this seperate to the player game object because attaching a camera to an object with a rigidbody component can cause issues.

![image](https://github.com/user-attachments/assets/9ea0caa6-a52a-4c1c-ae38-29af79838b2d)

12. Create an empty game object called Player and add a capsule game object named "PlayerBody" to the empty Player game object in the hierarchy. Add to more empty game objects to the Player, one called "Orientation" and one called "CameraPosition".

![image](https://github.com/user-attachments/assets/f5f32fea-1db0-4fa1-b911-0ebd877bf760)

13. Add a rigidbody component to the Player and set interpolate to interpolate and collision detection to continous.
 
![image](https://github.com/user-attachments/assets/8afe61f4-6a84-4e14-8d3f-b1863d7e2f34)

14. Now we can assign our playerView script to our PlayerCamera and we can change the sensitivity values in the inspector at will. You can do this by dragging and dropping the script in to the bottom of the inspector of the game object.

![image](https://github.com/user-attachments/assets/3c7d985c-c1d9-4dc7-996a-29a2536e9953)

15. Make sure that you drag and drop your orientation gameobject from the hierarchy in to the orientation box on the script in the inspector.
 
![image](https://github.com/user-attachments/assets/94c618ba-2812-48d9-9a5c-6d9c45e8c966)

16. Lastly, we need to create another script that will be attached to our Camera gameobject, so that the camera moves position in accordance with the players position once movement has been programmed.

17. To do this, create another MonoBehaviour script called cameraPosition. Delete the start method but leave the update method.

18. Before the update method, set a transform variable called cameraPosition. In the update method set the transform.position to the position of the cameraPosition.

![image](https://github.com/user-attachments/assets/17782260-ffa9-4c31-ba49-a2afc0153288)

19. 



 



21. 


    




