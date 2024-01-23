# Step by Step :

#### First of all we want to check our cores performance , We can see all the cores in our system by running ` $top ` command and press '1'. 
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/Process-Management-Stack-Task/cores.png)
#### As we can see here I have 12 cores. 🤓

---

#### Now we want to run our process. ` $dd if=/dev/zero of=/dev/null `
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/Process-Management-Stack-Task/dd%20commnad.png)
#### After that we want to assign 2 cores to hold the process ( here I will assign the process to core 7 & 8 ) and we will do this by using ` $taskset -cp 7,8 29317 `
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/Process-Management-Stack-Task/changing%20core.png)
#### Now we want to check the effect of the process on the assigned cores 
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/Process-Management-Stack-Task/whole%20performance.png)
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/Process-Management-Stack-Task/two%20cores%20performance.png)

---

#### Now let us play a little bit with the kernel and change the priority of the task one time with the lowest priority possible and second time with the highest priority possible
#### Lowest priority possible using ` $sudo renice -n -20 -p 29317 `
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/Process-Management-Stack-Task/renice%20-20.png)
There is no big difference here , The difference we will see in assigning it higest priority. The user space cpu percentage will reduce a lot and all the load will by on the system to handle the high prioriy task. 
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/Process-Management-Stack-Task/renice%2019.png)

---

#### Now we will kill the process using ` $kill -SIGKILL 29317 `
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/Process-Management-Stack-Task/sigkill.png)
#### Now as you can see the process "dd" is killed in the top monitor and the using percentage over the cores are similar. 
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/Process-Management-Stack-Task/after%20killing.png)



