# Communication with Hardware in Linux System

The **` device driver `** is the abstraction layer between software concepts and hardware circuitry as such, it needs to talk with both of them. In this chapter we will discuss, how a driver can access **` I/O ports `** and **` I/O memory `**. 

Whenever we inserted the devices to the running machine, dynamically a file gets created for that particular device and generally it shows into the **` /dev/ `** directory with some meaningfull name.

Suppose we require to connect **` USB Device `** to the running machine or system. Then **` kernel `** quitely does their job internally and executes the various services to acheve the goals. 
  - Post inserting the **` USB Device `** to the running system or machine the corresponding **device driver** which resides in the **` kernel space `** detects the state change and generates the events.
  - The **` udev `** daemon, **systemd-udevd.service**, receives device **` uevents `** directly from the kernel whenever a device is added or removed from the system or it changes its state.
  - When **` udev `** receives a device event, it matches its configured set of rules against various device attributes to identify the device.
  - **` udev `** supplies the system software with device events, manages permissions of device nodes and may create additional symlinks in the ${\color{purple}/dev/}$ directory.
  - The **` udev `** rules are read from the files located in the directories ${\color{green}/usr/lib/udev/rules.d}$ and ${\color{green}/usr/local/lib/udev/rules.d}$, the volatile runtime directory ${\color{green}/run/udev/rules.d}$ and the local administration directory ${\color{green}/etc/udev/rules.d}$.
  - Once the process is completed the newly inserted or attached device will shwon in the **` /dev/ `** directory with dynamic name created by **` udev `** Dynamic Device Management. 
  - **` udev `** is basically a piece of code or a **User Space** program, which receives signal or notification from **` kernel `**.

  <img src="../../images/core-concept/connect-device/attach-device.png" height="550" width="600" >
