# Project_Design_Logic_Circuits
This was made with LogiSim Evolution 3.5.0

This project was made with LogiSim, it's purpose is to detect " Flip " , that is case sensitive. Once the word is detected one of the screen will be placing all the characters switching  from upper case to lower case and vice versa. Any other characters that are signs will not be altered while flip is detected. As well this system will count from 0 to 3 the times that the word flip has been detected. 

There are two versions made for this project, the First Version does contain flip detector and the switch circuit that changes the letters from upper to lower case and vice versa, but it does not accept any other signs like the enter, tab, etc. The only sign accepted is the space, the other signs will be replaced with a null. As for the second version of the project it does accept all the signs and letters to swictch once the flip is detected. Both versions contain the flip counter. 

This project contains concepts such as sequence detectors, shift registers, flip flops, combinational logic and VHDL. The VHDL is in another repository. 

This is the link of the VHDL code of this project:
https://github.com/quintana0004/VHDL_Project_LOGIC_CIRCUIT_PROJECT

This is the First Version of the Project

![Version1](https://user-images.githubusercontent.com/66384782/139343471-d929aa40-a46d-4c4d-9355-cb9c63b87478.png)

The normal screen will display everything that user has written without any changes, while the other screen will be displaying the change made by the Switch Circuit block that helps to switch the letters from upper to lower case and vice versa when it receives a high signal from the flip detector once is detected as well the counter will count each flip detection, it goes from 0 to 3.

Switch Circuit
![switch circuit](https://user-images.githubusercontent.com/66384782/139346713-c320e5d9-df9f-4ffb-8eca-8a3959f70ac5.png)

Bypass 1

Bypass 2

Dual Comparator

Flip Detector

Flip Counter

This is the Second Version of the Project

![version2](https://user-images.githubusercontent.com/66384782/139343684-aa45dc1b-cd60-4e79-a7e0-2d751269a1cb.png)

Both versions contain the same schema. 
