#### Q1/ What does kernel mean ?
##### Ans/ Kernel is the core of the operating system , It the component that have the scheduler inside it that schedules the processes running in the operating system. You can think of it that is the bridge between the software ( Applications ) running on the operating system and the resources you have as a hardware (CPU & Memory for example) . 
---
    
#### Q2/ What does Operating System mean?
##### Ans/ Operating System is a software that provides the user application with services and functions to help the user application to request for hardware resources in order to make its functionality. 
---

#### Q3/ Is Linux a kernel OR operating system?
##### Ans/ Actually it refers to both , So when we say linux we mean by it the operating system which includes the kernel inside it. When we say linux kernel we mean the component that have the scheduler built inside it and we also mean the component that is responsible for managing the hardware resources (CPU, Memory & Peripherals) . But when we say Linux OS , We mean by it the kernel + GUI Applications , System Package managment tools , shells and CLI & System Libraries/Utilities. 
---

#### Q4/ What is an Architecture Layer Diagram ?
##### Ans/ It is the hierarchy of how the Linux System is built , We start by the highest level which is the application level which is built on the user space , after that we have the kernal space which includes many stacks which is the core of the operating system , then the kernal space communicates with the device drivers which communicates with the hardware (where the hardware is the lowest level in the architecture) . 
---

#### Q5/ What is user space ?
##### Ans/ User Space is where the user-mode applications and processes run and of course it uses and allocates memory and uses resources for the user space application and processes. 
---

#### Q6/ What is kernel Space ?
##### Kernal Space is the space where it contains the Kernel itself and also core functions & algorithms for helping the system to manage the hardware resources & also it is the space that provides services and functions that the user space applications can use and call . 
---

#### Q7/ Describe Main Layers for Linux kernel.
##### Ans/ (1)System Call Layer , (2)Process Management Layer , (3)File System Layer , (4)Networking Layer , (5) Security Layer. 
---
    
#### Q8/ Identify the Purpose for each Layer.
##### Ans/ 
##### (1)System Call Layer : A set of functions (System Calls) that are used by the user-space to request resources/services from the kernel space. 
##### (2)Process Management Layer : Simply it is the scheduler which manage the computing resources given to each process taking care of the priority of the process and making it fair and efficient for competing processes. 
##### (3)File System Layer : Manages file systems, including file creation, deletion, and manipulation . Also it have VFS which is an abstraction layer that help the system to operate and deal with different file systems. 
##### (4)Networking Layer : Responsible for managing Network related functionalities , Network device drivers and can communciate with TCP/IP & UDP protocols and much more networking related operations. 
##### (5)Security Layer : Implements various security features and mechanisms, including access control, permissions, and security modules.
---

#### Q9/ Identify how each layer interacts with the lower one.
##### Ans/ 


#### Q10/ What is Glibc Library ?
##### Ans/ Glibc Library is a library that provides a set of functions which you can use in your application development that can help you communicate with the kernel module , each Glibc function calls many system calls under it. 
---

#### Q11/ What does command mean ?
##### Ans/ A Command is a directory path given to the computer and in this path is the binary execution file (script) that do a specific task. 
---

#### Q12/ Describe command in-terms of the following:
##### Ans/ ls  
#####    name: List all 
#####    Location: /usr/bin/ls (using $which ls)
#####    version: 8.30 (using $ls --version)
#####    input: You can input the path of the directory you want to list its files or also you can give -(option) as an input for a specific view of the output.
#####    output: Lists all of the files inside a directory with data of creation and last modification + owner & file type. 
