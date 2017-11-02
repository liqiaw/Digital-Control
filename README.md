# Digital-Control
Roomba Simulink/Stateflow Library
**Hattan Badya**

-This library contains three blocks that help in controling iRoomba wirelessly through creating a TCPIP object and share it between the IRsensors-Block and the Control-Wheel block. 
- You have to download all the files in the Project_Roomba folder in order for you to use the library without facing any problems.


![Big_Switch](https://github.com/tuf76885/Digital-Control/blob/master/Block_Pictures/BigSwitch.png)


- This block generates a TCPIP object and it send it to both blocks to create the wireless connection between Simulink and the Roomba.


![IRsensors_Blocks](https://github.com/tuf76885/Digital-Control/blob/master/Block_Pictures/IR_S.png)


- This block helps in reading the output of the six IR sensors of the Roomba. Those sensors can be used in detecting if there are any obstacles in front of the Roomba.


![Control_Wheels](https://github.com/tuf76885/Digital-Control/blob/master/Block_Pictures/C_W.png)

- This block is used to control the left and right wheels of the Roomba. The speed range is between -0.5 and 0.5 where 0.5 is the maximum speed in the forward direction and -0.5 is the maximum speed in the backward direction.



![Example_P1](https://github.com/tuf76885/Digital-Control/blob/master/Block_Pictures/Example.png)




- This file is a simulink file and it shows how the three blocks are working simultaneously. 
- As you can see, there is a swithc connected to the BigSwitch port in each of the operational blocks- those are the IRsensors_block, the Control_Roomba block, and the Control_Wheel block- that control the sharing of the TCPIP object.   

![Control_Roomba](https://github.com/tuf76885/Digital-Control/blob/master/Block_Pictures/C_R.png)

- This block contains the algorithm to control the Roomba incase of any obstacles facing the Roomba.
- For the SonarRanges port, use a constant block and creat a vector with six zeros and attach it to the port. This makes the Roomba compare all the values read by the IR sensors to the values of the vector and it allows it to decide whether a specific reading for one of the sensors is a zero or a one.

