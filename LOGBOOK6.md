# **LOGBOOK 6 - SEED Labs – Format String Attack Lab**
## **Task 1**
- We start this task by running the servers. After that, we send a "hello" message to the server running on 10.9.0.5.<br/>
![1](images/6.1.PNG)

User | Server
:---------:|:---------:
![2](images/6.2.PNG) | ![3](images/6.3.PNG)

- The other objective in this task was to crash the program. It's visible that by sending "%s" to the server, the program crashes.

User | Server
:---------:|:---------:
![crash1](images/6.4.PNG) | ![crash2](images/6.5.PNG)


## **Task 2**
### **2.A**
- Our goal was to print out the data on the stack.
To know how many "%x" where needed we tested a big number of them after a "A B C" string.

User | Server
:---------:|:---------:
![task2](images/6.7.PNG) | ![task2](images/6.8.PNG)

- In the server side we can see the printing of B and A in ASCII, so we removed the extra "%x" until our string wasn't printed in. The number of "%x" was 63.

User | Server
:---------:|:---------:
![task2](images/6.7.PNG) | ![task2](images/6.9.PNG)


### **2.B**
- Our objetive were was to print the secret message. In order to do that we needed to place the address in the binary form in the beggining of our message and a "%s" in the end.<br/>

User | Server
:---------:|:---------:
![6](images/6.10.PNG) | ![7](images/6.11.PNG)


## **Task 3**
### **3.A**
- In this sub-task, we needed to change target value to a different value. To do that, we changed the address in the begging to the address of the target and added a "%n" in the end. This special format specifier changed the target value to the number of characters printed before it: 8 times 63 plus 4 of the address equals 508, in hex 0x1fc.


User | Server
:---------:|:---------:
![8](images/6.12.PNG) | ![9](images/6.13.PNG)


### **3.B**
- In this sub-task, we need to change the content of the target variable to 0x5000. This time we needed that sum was equal to 20480 (0x5000 in decimal). 8 times 62 plus 19980 plus 4 equals 20480.<br/>


User | Server
:---------:|:---------:
![10](images/6.14.PNG) | ![11](images/6.15.PNG)
