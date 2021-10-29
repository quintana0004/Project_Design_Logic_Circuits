# Project_Design_Logic_Circuits
This was made with LogiSim Evolution 3.5.0

The project was made with 6 people in the group and me being the leader, decided to create 2 versions of the project with the first version that contains everything asked by the professor and the second version that has additional features. 

This project was made with LogiSim, it's purpose is to detect " Flip " , that is case sensitive. Once the word is detected one of the screen will be placing all the characters switching  from upper case to lower case and vice versa. Any other characters that are signs will not be altered while flip is detected. As well this system will count from 0 to 3 the times that the word flip has been detected. 

There are two versions made for this project, the First Version does contain flip detector and the switch circuit that changes the letters from upper to lower case and vice versa, but it does not accept any other signs like the enter, tab, etc. The only sign accepted is the space, the other signs will be replaced with a null. As for the second version of the project it does accept all the signs and letters to swictch once the flip is detected. Both versions contain the flip counter. 

This project contains concepts such as sequence detectors, shift registers, flip flops, combinational logic and VHDL. The VHDL is in another repository. 

This is the link of the VHDL code of this project:
https://github.com/quintana0004/VHDL_Project_LOGIC_CIRCUIT_PROJECT


### This is the First Version of the Project

![Version1](https://user-images.githubusercontent.com/66384782/139343471-d929aa40-a46d-4c4d-9355-cb9c63b87478.png)

**Switch Circuit**

![switch circuit](https://user-images.githubusercontent.com/66384782/139350450-af605acf-b502-4d7c-bce6-a26f97dd0c3b.png)

- Inside of the Switch Circuit contains two bypass that will activate with the T flip flop that output will be acting as a selector for the multiplexer that outputs the 7 bits of each character entered by the keyboard, the output will depend by the Bypass_1 and Bypass_2.

**Bypass_1**

![bypass1](https://user-images.githubusercontent.com/66384782/139346765-084ee6b2-5372-4052-a73c-6d1e7780fe90.png)

- This is Bypass_1 that will get the ouput of the Dual_Comporator that identify if there character entered is a letter or a space (in ASCII table the decimal value is 32), the letters can be upper-case (due to the ASCII table that the decimal values goes from 65 to 90) or lower-case (due to the ASCII table that the decimal values goes from 97 to 122). The output will be conected as a selector to the multiplexer 2:1, the multiplexer will give a null to any value that isn't a letter or space. If it is a letter or space then it will proceed to change the letter with the arithmetic boxes that one is addition and the other is subtraction. It first compares if the character is bigger or smaller, then it will pass the value to one of the boxes, the carry out will be acting as a bit selector for the multiplexer 8:1 to pass the output. There is another box comporator that will pass if the value is space. The addition and subtraction boxes are full adders, but unsigned, meaning no negative values. 

**Bypass_2**

![bypass2](https://user-images.githubusercontent.com/66384782/139346770-86250702-c040-41ac-8526-7058cceb466d.png)

- This is Bypass_2 that will get the ouput of the Dual_Comporator that identify if there character entered is a letter or a space (in ASCII table the decimal value is 32), the letters can be upper-case (due to the ASCII table that the decimal values goes from 65 to 90) or lower-case (due to the ASCII table that the decimal values goes from 97 to 122). If it not a letter or space then it will be passing null. Important the values that are contant are in hexadecimal values in 7 bits. 

**Dual Comparator**

![dual comparator](https://user-images.githubusercontent.com/66384782/139346774-d63a7f8a-a390-424e-b47c-a5d685de20b7.png)

- This Dual Comparator is in charge to detect in the range of 65 to 90 (upper case) and 97 to 122 (lower case) and the comparator box that will detect the space. There is a tunnel that connects the output of the comporator boxes to a the EXNOR gate that if both values are the same the output will be high if not the it will be low (this is used for the letters). 

**Counter**

![counter](https://user-images.githubusercontent.com/66384782/139346781-ce6ccd6f-02bd-4271-9b97-4fddcb1be324.png)


* *Counter State Diagram* *

![image](https://user-images.githubusercontent.com/66384782/139362260-0b527534-47fc-427b-b471-c0f27e2cfa8e.png)


* *Counter State Table* *

![image](https://user-images.githubusercontent.com/66384782/139362320-fcdfa0f6-15ab-44ac-800a-620af3c26687.png)

* *Counter K-map* *

![image](https://user-images.githubusercontent.com/66384782/139362340-7104b914-ee9d-45d8-b382-c758e8870b0d.png)


- Uses two D type flip flop, this was implented by creating a state diagram, state table,and k-maps. The number was displayed with a hex display. 




### This is the Second Version of the Project

![version2](https://user-images.githubusercontent.com/66384782/139343684-aa45dc1b-cd60-4e79-a7e0-2d751269a1cb.png)


Both versions contain the same schema. The normal screen will display everything that user has written without any changes, while the other screen will be displaying the change made by the Switch Circuit block that helps to switch the letters from upper to lower case and vice versa when it receives a high signal from the flip detector once is detected as well the counter will count each flip detection, it goes from 0 to 3.
