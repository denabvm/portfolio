#Exercise 3 - Sensors and actuators 
this exercise was about adding sensors to an electrical circuit to deflate - inflate .
for this exercise i was working with mai-linh 
<img width="1920" height="2560" alt="exx 3" src="https://github.com/user-attachments/assets/939f5ad4-ef26-41a6-b653-d20a99d7078c" />
as you can see in the image :
inflatable pillow is the yellow one 
two air pumps 
and air valves 
first we tried to make our circuit and sensors the same way as Juliusz so that we reach a point and then go furthur .
our first test for checking if everything is working was  by ubloading a test sketch and checking if 3 MOSFEts blink in red or not,
which turned out working .
we also relized that both air pumps were wired for deflators so we changed one as well, then we started to code a button for controling deflation which did not work and only worked for deflation instead of inflation .(the pump ran but no air came out ) 
afterwards we realized that the pumps were connected to the wrong ports on the air valve .
we figured that deflation pump to the metal-end port and inflation pump to the plastic-end port also the valve is tied to the same pin through a MOSFET (pin8) so it opens the correct path when inflating .


#adding sensors 
we chose three sensors to check and control inflation and deflation 
first one was a PIR motion Sensors
<img width="348" height="338" alt="exx 3_pir_sensor" src="https://github.com/user-attachments/assets/365eb9d8-850d-402c-a2c0-0b455e73404e" />
we took this sensor thinking that it might just work with hand movement above it but as we exprinced further we realized that it's way more sensitive to any movement and start to pump .
then we decided to add a delay so the pumping would not get activated all the time and we added a 7 seconds delay .
<img width="704" height="762" alt="exx 3" src="https://github.com/user-attachments/assets/51ac0f17-c6ad-41b8-9638-3572f00767f1" />
so because of a extreme sensitivity of this sensor we decided to choose another one .

#Flex sensor 
we connected a flex sensor to the sysytem but as much as we tried it did not give us any values in printing. 
so we just thought that there is a problem with our coding or wiring but then decided to test another sensor and then the values started to change so the first flex sensor was broken after all .
the flex sensor value even when it was unbend was one so in our code we just put the flex value more than 2 for inflation .

#adding a joystick instead of a button 
we decided to add a joystick instead of the button for deflation so we checked joystick datasheet and 
we decided to use the moving up side and our whole system looked like the picture below : 
<img width="1600" height="900" alt="ex 33 f" src="https://github.com/user-attachments/assets/668d9ee1-8206-48b8-b9a8-6b6770379b4e" />

