# RoboticArm
Demo: https://www.youtube.com/watch?v=y60emdIJogM
--Mode One


When the arm initializes, it is in mode one. In mode one, the arm is controlled through 4 potentiometers.
A potentiometer is a variable resistor. The potentiometer allows me to control the current let into the arduino read pin and turn that into a value
In mode one, the arm is also searching for two possible events
1)The button is pushed
2) A command is sent through the Bluetooth module

If a button is pressed the mode is changed to two. 
If a command is received, the arm moves to a central position and then the mode is changed to three


--Mode Two


Mode two is the autonomous mode of the project.
How it works
The arm first goes to a starting position of  all the way to the right, down, and claw open
The arm starts rotating to the left, while constantly checking the distance sensors.
If an object is read to be closer than 20 cm, the object stops
It then moves forward(which involves moving up and forward due to the way the arm is engineered) until it reaches 3 cm
Once it is 3 cm away, the claws of the body close, and the object is brought up
The mode is changed back two one


--Mode Three


Mode three is entered by connecting the kindle app to the Bluetooth module and sending any signal
The mode begins by gradually bringing the arm from the position of the potentiometers to the starting position of the mode(Center, medium height, arms open).
When one presses down a button it sends a number to the arduino and the arduino reads that as a command
When the button is released, another number is sent and the arduino stops carrying out the action
The controller can also click on “mode 1” or “mode 2” to make the arm gradually go into position to go into those modes, and then enter them.
LASTLY, there is a button that says Gyroscope.
When one clicks that button they are brought to a new screen on the app. The app measures the x and y tilt of the kindle and sends values back to the kindle telling it to move left or right, and forward and backwards.
