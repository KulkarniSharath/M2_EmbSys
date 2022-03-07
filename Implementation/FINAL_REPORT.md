### Author Name : Sharath Kulkarni
### Document release date : 07/03/2022
### Module : Embedded Systems Project Report

# Table of Contents

1) Introduction
2) Requirements
    *	Low level requirements
    *	High level requirements 
3) Block Diagrams & Design
4) Test Plans and output
5) Implementation
6) Applications and FutureScope

# Chapter 1 : Introduction
As thefts are increasing day by day security is becoming a major concern nowadays. So a digital code lock can secure your home or locker easily. It will open your door only when the right password is entered. The need of safety can be achieved by making locks which can be electrical or mechanical with one or a few keys, but for locking a big area many locks are required. Nowadays every device’s operation is based on digital technology.  

For example, technology based identity devices are used for automatic door unlocking or locking. These locking systems are used to control the movement of door and are functional without requiring a key to lock or unlock the door. These locking systems are controlled by a keypad.

The main objective of this project is to give safety at every common places like home, public places. In this user would give a known password. The information will be stored in database. When the correct passcode will be entered, the microcontroller will give instruction to servo motor. Servo motor will perform the action on door unlocking. Thus, what we want is digital technology to construct an integrated and well customized safety system at a price which is reasonable.

Idea behind this project is of a door-latch opening using a password entered through keypad. As well as turning on the Buzzer when passcode is entered wrong for multiple times. User can modify this password anytime he/she wishes using a keypad. The main component in the circuit is Arduino UNO which is basically used to send a text message to owner of the house about the breach of security. The 4*4 keypad is used to enter the password. The entered password is compared with the known password. If it is correct password, the system opens the door by servo motor and displays the status of door on LCD. If the password is wrong then door remains closed and displays “WRONG PASSWORD” on LCD.

**SWOT ANALYSIS**

![SWOT analysis](https://user-images.githubusercontent.com/98825618/157057418-5fb131d7-a3a3-4a9d-9da9-8fc1c465647d.PNG)


**4W1H**

What : Password Based Door Lock System using microcontroller is a project/prototype where a secure password will act as a door unlocking system. Traditional lock systems using mechanical lock and key mechanism are being replaced by new advanced techniques of locking system.

Where : This project can be used in offices, companies also at home. It will provide keyless entry.
This can also be used in Banks for safety lock.

When : The thing of improvement in technology has bought in the improvements in implementing new features. To keep in pace with the current trends the saftey features can also be improved like mentioned above.

Who : This very useful technology can be used and implemented by the people to keep their belongings in a safe place or to make any place secure from any potential threats.  

How : The very basic implementation can be done by using a motor, keypads, display screens etc. but if you want to make more secure system then you can add gsm module, rfid tags, finger print scanner and so on to make strict user authentication. 


# Chapter 2 : Requirements
    
       2.1 High level requirements (HLR)
           HLR1. The system shall take input of passcode from the user
           HLR2. It shall rotate the motor (servo) on correct input
           HLR3. It shall on the buzzer in case of wrong input 
     
      2.2 Low level requirements (LLR)
           LLR1. The system shall display the things in the lcd display
           LLR2. It shall contain the option to change the password
           LLR3. It shall a have push button there to reset

# Chapter 3 : Block Diagrams and Design

The block diagrams shall have been included with the fingerprint sensor or any RFID tags module for user inputs, but due to the availability of such components in simulide software lead to using of a simple keypad.

More components like biometrics input, sim900 module, GSM etc. could be used to make the system more advanced.

![Block diagram doorlock](https://user-images.githubusercontent.com/98825618/157058343-f31e3307-2a7c-456b-9ae2-c663fb63cb8c.PNG)


The **components** used here are as follows:

* LCD display : This 16 x 2 character LCD module uses I2C interface to communicate with the host microcontroller Arduino. This LCD display is used to display any text, data, characters of all types. Connections to Vcc, gnd, SDA line. 
*	Buzzer : A buzzer or a beeper is an audio signal device, which is piezoelectric. Many applications are present for this like alarm devices, keystroke, notifications etc. to give the user a sound based message.
*	Servo motor(actuator) : A servo motor is a device that has an output shaft and this shaft can be positioned to different angular positions by the code. As long as the code exists it is going to maintain its position. 
*	Keypad(sensor) : A keypad is the most common input device in microcontroller applications like this one. It’s basically a X*Y matrix switch open and takes the input when pressed. If it has 12 keys then it is a 3 columns and 4 rows.
*	Arduino Controller : It is an open source and easy to use hardware and software. They act as a microcontroller and are able to read inputs and produce output and they can be done by the peripherals connected to them example led blinking, motor on/off etc.

**FlowchartImage**

![Flowchart](https://user-images.githubusercontent.com/98825618/157058863-23beeade-0e42-4a6d-bebb-2f61bc88cb61.PNG)

**UMLImage**

NOTE: *All functions mentioned here may not be implemented due to non-availability of components in the software.*

![Capture11111](https://user-images.githubusercontent.com/98825618/157058961-27db2238-268c-46b2-9ba7-ee92ae029ec3.PNG)


# Chapter 4 : Test Cases Plan & Output 

1)	Correct Input given by the user (passcode is correct)

•	**Expected output is** : The door shall open i.e the servo motor shall rotate in a direction, the LCD shall light up and display the open message.

•	**Actual output is** : The door shall open up with the turn of the servo arm from its original position and a clear beep is heard by the buzzer upon this action.   (**IMPLEMENTED**)    

2)	Wrong Input given by the user (passcode given is wrong)

•	**Expected output is** : The door shall not open i.e the servo motor shall not rotate, the LCD shall display “Wrong password” and the buzzer shall beep once.

•	**Actual output is** : The door shall not open in this case and gives a different type of beep and a clear message is displayed of wrong entry of the passcode.  (**IMPLEMENTED**)

3)	Multiple wrong inputs given by the user 

•	**Expected output is** : The door shall not open i.e the servo motor shall not rotate, the LCD shall display “Wrong password” and the buzzer shall beep multiple times and send a message to the user privately informing the breach of security.

•	**Actual output is** : The buzzer beeps multiple times to indicate wrong input of pass code. (**IMPLEMENTED**)
 
In the future to improve this very prototype or project we can add more features like a phone number to which the authentication may go to the owner indicating a security breach, or may add a finger print scanner for secure system etc... 


# Chapter 5 : Implementation

**HARDWARE IMPLEMENTATION IMAGES**

![Hardware implementation 0](https://user-images.githubusercontent.com/98825618/157059339-3e4fc1f2-a045-4c81-aad7-ab605b0ef2cf.PNG)


![Hardware implementation 1](https://user-images.githubusercontent.com/98825618/157059295-2e8f8200-98dd-46ce-9f04-eb135362cf50.PNG)


![Hardware Implementation 2](https://user-images.githubusercontent.com/98825618/157059242-6bfc8c88-5384-428d-b220-cfd27f58938e.PNG)


![Hardware Implementation 3](https://user-images.githubusercontent.com/98825618/157059144-7a4d92b0-c1cb-4a07-b859-95d2121c4436.PNG)

**SOFTWARE IMPLEMENTATION IMAGES**

![Software Implementation 0](https://user-images.githubusercontent.com/98825618/157060701-deb613ed-dbdd-415c-941f-a5c2944db9bd.PNG)

![Software Implementation 1](https://user-images.githubusercontent.com/98825618/157060741-eb3be3fa-b4b6-4cc1-ad8b-3b3dc0df55ff.png)

When the code is incorrect we get a clear audio out.

The following implementation can be improved by adding more equipment like RFID tags for input rather than the keypad, or any voice recognition module for a different approach to this current model.


# Chapter 6 : Applications and Future scope

This simple circuit of a smart door lock system can be used at residential places, security places, organizations where high security is required. It is a smart and most efficient way of detecting threats and adding more advanced features can reduce these kind of risks.  

Various novelty and modifications can be done to this existing design. We can make it more secure by adding more stage. We can make card system where card is scanned first and password is checked next. Biometrics system can also be introduced, it can be more prominent and a recognized means of positive identification. GSM can be used for remote access.  


# References

1.  [ARDUINO Libraries](https://docs.arduino.cc/library-examples/)	
2.	[IEEE_paper](https://ieeexplore.ieee.org/document/9530806)
3.  https://www.hackerearth.com/blog/developers/arduino-programming-for-beginners/
4.	https://www.researchgate.net/publication/354872757_DESIGN_AND_CONSTRUCTION_OF_A_SMART_DOOR_LOCK_WITH_AN_EMBEDDED_SPY-CAMERA
5.	https://www.ijert.org/research/smart-door-locking-system-IJERTV2IS110725.pdf
6.	https://www.electronicshub.org/password-based-door-lock-system-using-8051-microcontroller/
7.	https://microcontrollerslab.com/electronic-lock-pic-microcontroller/


