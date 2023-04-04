# Process Management and Monitoring in `linux` System
A process is basically a program in the execution. _For example:_ Suppose we have a **_C language_** program file _**` welcome.c `**_ and this program file will be given to the **_C language Compiler_** like _**` gcc `**_. Compiler will just convert this **_high level language_** (source code) to **_low level language_** (machine code) that is a binary code or file, which is directly executes on the hardware and provides the appropriate result.

The original code and binary files or codes both are called program only and generally reside in the secondary storage device i.e., **_HDD/SSD_**. In order to exeute this program Operating System loads this program into the **_main memory_** i.e., **_RAM_** and starts executing it. When program loads into **_main memory_** it creates data structures into the **_RAM_** and this structure is called as process.

![Process Structure](../../images/process-mgmt/peocess-structure.png)

  - **_Executables/text_**

    This section of memory contains the executable codes which are being executed or the current activity represented by the value of the **_Program Counter_**.
  - **_Static Local or Global variable_**

    This section contains all the **_local_** and **_global_** variables defined in the program. 
  - **_Stack_**

    Most of the program has the function calls or recursion . So the stack require to contain the temporary data, such as function parameters, returns addresses, and local variables.
  - **_Heap_**

    Program also has dynamic array, linked lists, etc. So heap requires to conatin the dynamically allocated memory to process during its execution time. 
    
This structure of memory is known as process boundary and eveythig required by the particular process will lies in this boundary only. While **_Operating System_** executing this particular process should never cross these boundaries. This boundary is called process.

### Identification of Process
There are number of process created in the system randomaly at any point of time in that senerio we are supposed to keep track of which process is what, how many process are there and what is the current state of a particular process. So to identify a particular process among various process there is a set of attribute are recorded at specific location called **_Process Control Block_** or **_PCB_**. <br>
**_Attributes of Process:_** <br>
  - **_Process ID_**

    A unique numerical identification number assigned by the operating system to the process.
  - **_Program Counter_**

    It is a register in **_CPU_** and contains that memory address from where the next instruction is to be fetched for execution.
  - **_Process State_**
  - **_Priority_**
  - **_General Purpose Register_**
  - **_List of Open Files_**
  - **_List of Open Devices_**
  - **_Protection_**




