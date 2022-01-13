# Week challenges 💻
---
Thursday 2022-01-13
---
1. Search for real word applications of Javascript
~~~
JavaScript is used in: Web development, web applications, presentations, Server applications, Web servers, 
games, art, smartwatch applications, mobile applications, robots.
~~~
2. Follow the github course, you can find it here
~~~
STARTED
~~~
Wednesday 2022-01-12
---
1. Learn about binary, decimal and hexadecimal numbers
~~~
DONE
~~~
2. Translate the year you where born to binary, decimal and hexadecimal
~~~
Birthyear. 1992 
Binary = 11111001000
Decimal = 1992
Hexadecimal = 7C8
~~~
3. Translate 51966 into hexadecimal and binary
~~~
Binary = 1100101011111110
Hexadecimal = CAFE
~~~
4. Use a Low-level language, for example MIPS aseembler
~~~
DONE
~~~
5.1 Create a program to add two numbers given by the user
~~~
.data
	number1: .asciiz "\nInput first number: "
	number2: .asciiz "\nImput second number: "
	result_message: .asciiz "\nThe result of the sum is: "
.text
	main:
		li $v0, 4
		la $a0, number1
		syscall

		li $v0, 5
		syscall

		move $t0, $v0

		li $v0, 4
		la $a0, number2
		syscall
		
		li $v0, 5
		syscall
		
		move $t1, $v0
		
		add $t2, $t0, $t1

		li $v0, 4
		la $a0 result_message
		syscall

		li $v0, 1
		move $a0, $t2
		syscall
~~~
5.2 Create a program that display your name
~~~
.data
    buffer: .space 20
    str1:  .asciiz "Enter your name:\n"
    str2:  .asciiz "Your name is:\n"

.text

main:
    la $a0, str1   
    li $v0, 4
    syscall

    li $v0, 8       

    la $a0, buffer  
    li $a1, 20      

    move $t0, $a0   
    syscall

    la $a0, str2    
    li $v0, 4
    syscall

    la $a0, buffer  
    move $a0, $t0   
    li $v0, 4       
    syscall

    li $v0, 10      
    syscall
~~~

Tuesday 2022-01-11
---
1. Watch this video about compilation and interpretation.
~~~
DONE
~~~
2. Search and answer the question: Java language is compiled or interpreted?
~~~
Java can be considered both a compiled and an interpreted language because its source 
code is first compiled into a binary byte-code. 
This byte-code runs on the Java Virtual Machine (JVM), which is usually a software-based interpreter.
~~~
3. Create an algorithm to calculate the equivalent of your local currencty to USD
~~~
  1. Get amount to convert to USD.
  2. Get USD exchange for local currency.
  3. USD_CURRENCY <-- GET
  4. NEW_EXCHANGE <-- LOCAL_CURRENCY / USD_CURRENCY
  5. PRINT NEW_EXCHANGE
  6. END
~~~
4. Read about Pseudocode.
~~~
DONE
~~~
5. Anwser to the question: Why is pseudocode helpful?
~~~
Pseudocode is helpfull because it is the begining of coding. It helps to the programmer to have a glboal view 
of all of the inputs, procceses and tasks that are gonna be coded.
Gives a model and a structure of how the code shoud look, without worring about especific grammar and sintaxis.
~~~
6. Create a pseudocode to calculate the aproximated age of a user base on the year they born.
~~~
1. START
2. Birth_Year <-- 2022
3. Age <-- 2022 - Birth_Year
4. PRINT Age
5. END
~~~
7. Read about flowcharts.
~~~
DONE
~~~
8. Answer to the question: Why are flowcharts important to us as developers?
~~~
Flowcharts are really important for developers because the show exactly all the proccess that our program, web site or app 
should work, not only in code, but in logic, structure, proccess and operations. Besides, it gives a graphic view of all
the entire system, allowin to improve every section if it is neede.
~~~
9. Search about High-level languages and Low-level languages.
~~~
High-level languages are easy understanding for humans, but the have to be interpreted in order to be understood by the
computer. This languages are compiled or interpreted, depending on the situation.
Low-level languares are most closer to computer understanding, but hard udnerstanding for humans. The better example is Assembler, 
wich is the most common Low-level language. It is hard to understand for humans, therefore is hard to code also.
~~~

