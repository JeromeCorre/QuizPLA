
# Quizz - Assembly Language Programming

## Notes:
**Assembler**: A computer program which translates assembly language to machine code ("programme assembleur" in French)
**Assembly**: a program code in a more readable interpretation of a processor's machine code, allowing easier understanding and programming by humans ("language assembleur" in French)


## The **ALIGN** and **ORG** directives
Here is an example of an assembly code. Where is located the instruction of line 6 in the address memory? 
And what about data2 and data3?

```
Line	Machine Code						Address
1		AREA Example, CODE, READONLY				
2	start	LDR r6, #10						0x00
3		LDR r7, #0						0x..
4	data1	DCB #32 						0x..
5		ALIGN
6		MOV r0, r1 						0x..
7
8		ORG 0x5000
9	data2	DCB #10 						0x..
10	data3	DCB #2 							0x..
```

## The **EQU** directive
Given the following code : 

```
	Y	EQU 5
	X	EQU 0x100
	Z	EQU X + 10

		MOV r0,#Y
		MOV r1,#X
		MOV r2,#Z
```

What are the values stored in registers r0, r1 and r2 in hexadecimal? 
r0 = 
r1 = 
r2 = 

## The **GBLA**, **GBLL**, **GBLS**, **SETA**, **SETL**, and **SETS** directives
Which of the following code snippet correctly set the value of a variable to 0x7F?
|| True | False|
|:-------------------------------------------|:--------:|:--------:|
| GBLA myVal 0x7F | [ ] []() | [ ] []() |
| myVal SETA 0x7F | [ ] []() | [ ] []() |
| myVal GBLL 0x7F | [ ] []() | [ ] []() |
| SETS myVal 0x7F | [ ] []() | [ ] []() |

## The **Export**, **Global** and **Extern** directives
No question on this topic yet!

## The **DCB**, **DCW** and **DCD** directives
Given the following assembly code, fill in the memory addresses and values
```
	ORG 0x4000
	data1	DCD 1, 432, 0xAEFC8730
	data2	DCD data1 + 1950
```

![Memory stack](https://i.imgur.com/xlXSidT.jpg "Memory stack")

## The **Space** directive
* What does the space directive do?
=>

* Circle the right answer. The size of a memory block is expressed in:
	* bit
	* byte
	* nibble
	* halfword
	* word


* In the following line of code, What does the value **23** represent?  
```buffer SPACE 23```
=>  


* Should we take precautions when calling the SPACE directive ? If so why?
=>     

## The **MACRO** and **MEND** directives
|| True | False|
|----------------------------------------------|:--------:|:--------:|
| The directives **MACRO** and **MEND** are used to define a macro| [ ] []() | [ ] []() |
| The definition of a macro does not create any machine code| [ ] []() | [ ] []() |
| When the macro is called, the assembler does a "macro expansion" which copies the macro code where it was called| [ ] []() | [ ] []() |
| A macro can be defined with parameters | [ ] []() | [ ] []() |
