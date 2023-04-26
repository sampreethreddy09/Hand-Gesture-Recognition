# Hand-Gesture-Recognition
This project aims to provide speaking aid to dumb and blind people. Users will have to display numbers assigned to leters for eg: (a, 1) (b, 2) (c, 3)….. (z, 26). Gestures must be recognised and converted to equivalent leter and concatenated to a string. The string should then be displayed on a LED screen connected via Arduino.

# PROJECT REQUIREMENTS SPECIFICATION
• PC with python installed with following libraries: OpenCV, media pipe, TensorFlow, pandas and NumPy.
• Arduino with LED Display atached through I2C module and its respec􀆟ve libraries installed through IDE with a code to display Serial Inputs

# PROJECT DESIGN
- Ini􀆟ally we setup a gesture recogni􀆟on service in python using the OpenCV library.
- Then the media pipe library was used to log the co-ordinates of required gestures (represen􀆟ng numbers) to a .csv file.
- Then we used TensorFlow module-based training module to train our program to recognise the gestures.
- On receiving an input,
    1) Handiness of the input is obtained
    2) Received gesture is converted to numeric form and saved in a variable
- Left hand is considered as ten’s digit and right hand as one’s digit. So, on receiving both the hand values (both are set to 0 by default) we compute the rela􀆟ve number by the formula 10*le􀅌 + right.
- The computed number is then converted to text and is ready to be sent to Arduino over Serial port.
- We connected a LED Display to Arduino and coded it to accept Serial inputs as a string and display it on the LED.

On startup :
![image](https://user-images.githubusercontent.com/115579102/234520614-3d653693-cd64-498d-8900-fd452d9884b8.png)

Output after recieving gestures (left-0 right-2, left-0 right-1, left-2 right-0):
![image](https://user-images.githubusercontent.com/115579102/234521007-6d6de708-cc56-4faa-b0d8-09f54d19e581.png)

