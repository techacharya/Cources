# The Linux kernel

**${\color{green}Kernel}$** is the core component of the Linux based Operating System and has complete control over everything in the system. It always resides in the memory till system shut down and facilitates interactions between hardware and software components. It virtualizes the hardware resources of the machine to provide each process with its virtual resources. This makes the process seem as it is the sole process running on the machine. Different types of kernel listed below:
  - **Monolithic Kernel**

    Monolithic Kernel implements fundamental features of a machine such as managing files, process, memory, and other resources in which all the resources are associated with kernel-space. This increases the size of **Kernel** and the execution of a process is faster.
  - **Mirco Kernel**

This type has a minimal features with virtual memory and thread scheduling. It has less services in the kernel space and puts rest in user space. So the kernel size reduces and communication among services is done through message parsing and that reduces the speed of execution.
  - **Hybrid Kernel**
  - **Exo Kernel**
  - **Nano Kernel**

  - Linnux based Operating System uses **Monolithic Kernel**, hence **kernel** carries out process scheduling, device management, memory managemrnt and several operations by itself.
  - The **linux kernel** is also modular, hence it extends its capabilities through the use of dynamically loaded kernel modules without the need to reboot the system. A module can be configured as **built-in** or **loadable**.

