# CollegeBellSystem_using_FPGA_Verilog


**INTRODUCTION**

Educational institutes like colleges, universities and schools have various periods and classes throughout the day. To indicate the end of each class and the start of each period a bell is used. This bell is usually rung by a person after each hour. However this bell might not be accurate all the time. So we propose a system to automate this process. The primary objective of designing this project is to reduce human intervention for the purpose of manual switching operation of a bell, thus increasing the accuracy. Our system is designed in such a way that it is exactly dependent on real time clock and the switching of the bell is controlled automatically.

<br/>

**BLOCK DIAGRAM**

![Aspose Words e36210b2-57fb-4d84-a979-1d47c27f579a 001](https://github.com/sourabhshanbhogue/CollegeBellSystem_using_FPGA_Verilog/assets/84284202/38ca9d17-0be9-4547-a09c-b3de127b3c43)


<br/>

**WORKING PRINCIPLE**

<br/>

**Clock generation:**

The Spartan-6 FPGA kit has a 4MHz internal clock. A Verilog code designed to generate a 1Hz clock using this 4MHz and clock division concept, so as to generate a time of 1s which matches the real world timing. 

**Time generation:**

Using this 1Hz clock seconds, minutes and hours are incremented. A 24-hour format is chosen. At every negative edge of this clock, the seconds gets incremented. After 59 seconds, the minutes start incrementing and after 59 minutes, hours start incrementing. After 23 hours, 59 minutes and 59 seconds, the time is set back to 0 and seconds start incrementing again. All variables keep incrementing continuously. The initial value of all variables can be changes so as to start the clock from a particular time. The reset switch is used to reset all time values to zero.

**Bell time settings:**

The bell timings are set to ring only from 9:00 hours to 16:00 hours. There are a total of 8 bell rings. The first being at 9:00 hours indicating the start of college day, the next bell rings are at 10:00 hours, 11:00 hours, 12:00 hours, 13:00 hours, 14:00 hours, 15:00 hours respectively. The last bell ring is at 16:00 hours indicating the end of the college day. The first and the last bell rings for 8 seconds each and the bells in between ring for 5 seconds each.  

The current value of time is given as initial condition to the clock and switched on. The clock and bell works according to the conditions mentioned.

<br/>

**RESULT**

![Aspose Words e36210b2-57fb-4d84-a979-1d47c27f579a 007](https://github.com/sourabhshanbhogue/CollegeBellSystem_using_FPGA_Verilog/assets/84284202/696c3e9f-5d65-4266-8b1b-04ab69049ade)


The college Bell System is implemented and outputs are verified. 

This project can be further improved by displaying the seconds and by designing a provision for manual input of time to the clock.
Page 9

