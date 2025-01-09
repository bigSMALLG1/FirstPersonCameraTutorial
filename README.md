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

7.


