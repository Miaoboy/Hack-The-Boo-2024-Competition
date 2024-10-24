![image](https://github.com/user-attachments/assets/24ec11e3-632b-452a-acc1-f3c5441230f5)

Difficulty: easy

First since this is a reverse engineering question, mostly i will using binary ninja, IDA freeware and ghidra to do analyse on the program.

This is a the main function view in the IDA freeware

![image](https://github.com/user-attachments/assets/62376e75-501a-407e-8c1e-ba31422163b0)

Ghidra view

![image](https://github.com/user-attachments/assets/061d74b1-a7f1-4d3d-b260-4b8da87a95b5)

Binary ninja view

![image](https://github.com/user-attachments/assets/b5c676e2-070d-4330-8816-b10b492f7791)

We can understand that the program is prompt user for and input as a recipe and it will fo through a fryer function to shuffle the input.

The desire expected output which has been shuffle will be '1_n3}f3br9Ty{_6_rHnf01fg_14rlbtB6Otuaru', mostly the different tools provide similar analysis just the level of the programming language different

I try to figure the shuffle algorithm of the fryer program but it come to fail

![image](https://github.com/user-attachments/assets/b5615e89-499d-4e01-9449-36f18752966a)
![image](https://github.com/user-attachments/assets/1fddd264-be56-4bf8-b58e-f6e11fc2fe40)


Since there is  H T B { } those flag element in the expected recipe i try to place the format correctly and see what shuffle output i will got

![image](https://github.com/user-attachments/assets/483a9367-0277-492d-a476-39ba99501725)

I found out that everytime the shuffle algorithm is fix and flag element in shuffle output i got, is same as the expected recipe which mean the recipe could be the flag of this question with HTB{} format

![image](https://github.com/user-attachments/assets/0e3f5afd-b308-4c32-b3f8-3f10720e9ce9)

I try to replace the element that i can recognize with same amount of characther 

then i rearrange the expected recipe with the location by the sequence of my regconize element which 0 = 4 , 1 = _ , 3 = t and this is what i get at the end and the recipe is correct now 

![image](https://github.com/user-attachments/assets/1df913c8-25ec-4f06-a93d-db58957694b0)
