# Paper Puppets

*A lab report by Alana C. Student*

## In this Report

To submit your lab, clone [this repository](https://github.com/FAR-Lab/IDD-Fa18-Lab4). You'll need to describe your design, include a video of your paper display in operation, and upload any code you wrote to make it move.

## Part A. Actuating DC motors

**Link to a video of your virbation motor**

![vibrating_motor](https://github.com/AlanaCrognale/IDD-Fa19-Lab4/blob/master/vibrating_motor.mov)

## Part B. Actuating Servo motors

### Part 1. Connect the Servo to your breadboard

**a. Which color wires correspond to power, ground and signal?**

Red: Power

Brown: Ground

Orange: PWM Pin (10)

### Part 2. Connect the Servo to your Arduino

**a. Which Arduino pin should the signal line of the servo be attached to?**

Any PWM Pin (e.g. 9,10,11)

**b. What aspects of the Servo code control angle or speed?**

The control angle is controlled by the pos variable, and the speed is controlled by delay(X). For example, in the sweep example code's for loop shown below, the servo moves to the angle in the pos variable in Xms amount of time from delay(X).

  for (**pos = 0; pos <= 180**; pos += 1) { // goes from 0 degrees to 180 degrees
  
    // in steps of 1 degree
    
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    
    **delay(5);**                       // waits 15ms for the servo to reach the position
    
  }
  
  for (**pos = 180; pos >= 0**; pos -= 1) { // goes from 180 degrees to 0 degrees
  
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    
    **delay(15);**
    
## Part C. Integrating input and output

**Include a photo/movie of your raw circuit in action.**

This servo moves based on the potentiometer reading, where the 0-1023 analog input values are mapped to the 0-180 degrees that the servo will move.
![servo](https://github.com/AlanaCrognale/IDD-Fa19-Lab4/blob/master/Servo.mov)

## Part D. Paper puppet

**a. Make a video of your proto puppet.**

![proto_puppet](https://github.com/AlanaCrognale/IDD-Fa19-Lab4/blob/master/proto_puppet.mov)

## Part E. Make it your own

**a. Make a video of your final design.**

This design is an updated version of my data logger from lab 3, where the FSR measures how much force is applied which corresponds to how much attention you are giving the puppet.  When too much attention is given, the puppet's arms move above its head, when not enough attention is given, the puppet's arms move below its head, and when the right amount of attention is given, the puppet's arms stick straight out.  Likewise, once the data logging is complete and the lcd display presents what percent of attention was received in total, if the puppet received too much attention, it waves its arms rapidly above its head 5 times, if the puppet received too little attention, it waves its arms rapidly below its head 5 times, and if it received the perfect amount of attention, it waves its arms more slowly for the full 0 to 180 degree range.

![too_much](https://github.com/AlanaCrognale/IDD-Fa19-Lab4/blob/master/too_much.mov)

![perfect](https://github.com/AlanaCrognale/IDD-Fa19-Lab4/blob/master/perfect.mov)

![not_enough](https://github.com/AlanaCrognale/IDD-Fa19-Lab4/blob/master/not_enough.mov)

![code](https://github.com/AlanaCrognale/IDD-Fa19-Lab4/blob/master/DataLoggerv2.zip)

 
