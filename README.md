# Digital-Control
Roomba Simulink/Stateflow Library
** Hattan Badya **

-This library contains three blocks that help in controling iRoomba wirelessly through creating a TCPIP object and share it between the IRsensors-Block and the Control-Wheel block.
...

![BigSwitch](https://github.com/tuf76885/Digital-Control/blob/master/BigSwitch.png)
- This block generates a TCPIP object and it send it to both blocks to create the wireless connection between Simulink and the Roomba.
![IRsensors_Blocks](https://github.com/tuf76885/Digital-Control/blob/master/IRsensors_Block.png)
- This block helps in reading the output of the six IR sensors of the Roomba. Those sensors can be used in detecting if there are any obstacles in front of the Roomba.
![Control_Wheel](https://github.com/tuf76885/Digital-Control/blob/master/Control_Wheel.png)
- This block is used to control the left and right wheels of the Roomba. The speed range is between -0.5 and 0.5 where 0.5 is the maximum speed in the forward direction and -0.5 is the maximum speed in the backward direction.
![Example_P1](https://github.com/tuf76885/Digital-Control/blob/master/Example_for_Project.png)
- This file is a simulink file and it show how the two blocks are working simultaneously. 

