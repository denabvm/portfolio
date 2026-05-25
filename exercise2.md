Sub-circuit 1 – Connecting the buzzer 

For the second lab we started with adding a buzzer to our circuit , the components we needed were :  

   

Arduino Uno 

Buzzer 

Resistor 

Breadboard 

 Set of male-male jumper wires  

 <img width="392" height="355" alt="ex 2-1" src="https://github.com/user-attachments/assets/737e4cdb-1717-4c03-a6c2-a765839b3327" />

We also need to run the test code file in Arduino with the right pin input  and the pin in code  have to match the pin in board ,  with the  resistor our circuit didn’t work and we removed it  after that we observe that when we hit the button  buzzer makes a sound and if we change delays  and HIGH/LOW signals the longevity and the pattern  of the sound change . 

As we tried to experiment we realized that (buzzerPin, High) and delay(x)  are for how long on ring lasts .  

For instance if the delay is 5000 , it means that one ring will last for 5 second .  

As for the ( buzzerPIn , LOW)  , this defines that how long a pause between two rings last . 

<img width="1532" height="1152" alt="ex 2-1" src="https://github.com/user-attachments/assets/ff97e19a-7004-40df-b43c-30be1ec72edc" />

Sub-circuit 2 – Connecting the LCD screen 
<img width="500" height="375" alt="ex 2-2" src="https://github.com/user-attachments/assets/1f684c68-4407-47b5-ae2c-cc93f95b35c0" />

For task two , we added a LCD screen , and as it was described in the task description we for Arduino we needed to extract  I2C_scanner.ino file from the given zip file so that we can find the address of LCD .  

As for the board we connected SCL and SDA wires .  
 <img width="1400" height="602" alt="ex2-2" src="https://github.com/user-attachments/assets/fb9995af-2eec-44ee-8efc-890a6d3f9d3f" />
<img width="768" height="292" alt="ex 2-2" src="https://github.com/user-attachments/assets/d57c79f1-7739-419c-b1c7-30a3c7c0b485" />
After the address of LCD was scanned  the screen turned on and the showing text was “whatever makes sense to show”.
<img width="1152" height="1292" alt="ex 2-2 c" src="https://github.com/user-attachments/assets/96c2c95c-94fb-4f6c-a544-7e832c0411c1" />
After some expriment with screen we realized that The LCD screen has a fixed limit of 16 characters per row and 2 rows total, which are defined when initializing the screen using LiquidCrystal_I2C lcd(0x27, 16, 2). Setting values beyond these limits has no effect. To control where text appears on the screen, lcd.setCursor() is used — it takes two parameters where the second one determines the row: 0 for the first row and 1 for the second. To test this, we configured the display to show only 4 characters per row and printed "High five", which demonstrated how the screen handles text within its constraints.
<img width="1400" height="602" alt="ex 2 d 1" src="https://github.com/user-attachments/assets/15a68bd4-dbdc-43ed-98b3-2ec28391f779" />
<img width="1152" height="2048" alt="ex 2 d" src="https://github.com/user-attachments/assets/9da53bd2-d5f4-4284-82df-2a6d695246f8" />


 

 

 

Sub-circuit 3 – Expanding the setup with a Real Time Clock 

The problem that we had at first was that we didn’t connect the SDA and SCL wires in series , and we realized that when no address was shown after scanning , after switching to series three addresses  were shown . 

 <img width="754" height="174" alt="ex 2-3-1" src="https://github.com/user-attachments/assets/6e683018-e1ac-4da0-b05f-ed46fe1baa76" />
We set the time with rtc.adjust()  and Data Time-declaration  
<img width="1449" height="1152" alt="ex 3-1" src="https://github.com/user-attachments/assets/aefe190f-b5e1-43aa-92c2-2a671c796010" />

Sub-circuit 4 – Using the Push Button  

The final task was to add four buttons so for that we went  needed to use the test code . 

Below i will explain the functionality of each buttons : 

Yellow : increase hour in set alarm mode  

Green : increase minutes in set alarm mode  

White : activation/deactivation of the alarm  

Red: set alarm mode  

<img width="1740" height="1152" alt="ex 4" src="https://github.com/user-attachments/assets/e5a7267e-76c0-43a1-9968-2c3259175712" /> 

Also the other thing that is good to mention is that we need the male wires to add to the specific pins  so all the buttons work properly . 

# Our final task : customized  alarm clock  
We both were curious and agreed to explore as much as we can , so we  added four functions .  
<img width="1278" height="1531" alt="ex 2 custome" src="https://github.com/user-attachments/assets/15b7d840-6595-4d3c-b930-4e558f199050" />
the picture above is our clock with all functions and below i will explain each Individually  

 













 
