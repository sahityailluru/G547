# G547
INA 219 current sensor connected with Raspberry pi using I2C interface to measure shunt current and voltage.
  In this project 100 ohms resistor is used as shunt and led is used as load.
PROCEDURE TO BUILD AND INSERT DRIVER IN KERNEL AND TO USE USERSPACE

Step-1 : Change path of the system to the directory where all the required driver files are stored using the following command
cd path_address

Step-2 : Now here Makefile consists of creating object files, kernel object file and compiling userspace application. Following Command is used sudo make all

Step-3 : In this step , we insert the driver in kernel using the following command sudo insmod main.ko

Step-4: To run and create output file in user space the following command is used. gcc -o output user.c

Step-5: As userspace application program is compiled in Makefile so we directly see the output of userspace program using following command sudo ./output

Step-6 : To remove the driver from the kernel use the following command sudo rmmod main.ko

Step-7 : To remove the object files use the following command sudo make clean
