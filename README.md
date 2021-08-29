# Virtual-Painter
An simple project detect color in an video using webcam
So here’s how we will achieve this, first, we will use color masking to get a binary mask of our target colored Pen, (I’ll be using a blue colored marker to as the virtual pen) then we’ll use contour detection to detect and track the location of that pen all over the screen.

Once we’re done with that it’s just a matter of connecting the dots literally, yes you just have to draw a line using the x,y coordinates of pen’s previous location (location in the previous frame) with the new x,y points (x,y points in new frame) and that’s it, you have a virtual pen.
So here’s a breakdown of each step of our application.

Step 1: Find the color range of the target object and save it.
Step 2: Apply the correct morphological operations to reduce noise in the video
Step 3: Detect and track the colored object with contour detection.
Step 4: Find the object’s x,y location coordinates to draw on the screen.
Step 5: Add a Wiper functionality to wipe off the whole screen.
Step 6: Add an Eraser Functionality to erase parts of the drawing.
