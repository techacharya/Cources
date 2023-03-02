# Communication with Hardware in Linux System

The **` device driver `** is the abstraction layer between software concepts and hardware circuitry as such, it needs to talk with both of them. In this chapter we will discuss, how a driver can access **` I/O ports `** and **` I/O memory `**. 

Whenever we inserted the devices to the running machine, dynamically a file gets created for that particular device and generally it shows into the **` /dev/ `** directory with some meaningfull name.

Suppose we require to connect **` USB Device `** to the running machine or system. Then **` kernel `** quitely does their job internally and executes the various services to acheve the goals.  

  - **` udev `** is basically a piece of code or a program, which receives signal or notification from **` kernel `**
