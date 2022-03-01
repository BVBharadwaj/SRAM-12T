# Quadruple Cross-Coupled Latch-Based 12T SRAM
## Table of Contents 
1. [Abstract](#Abstract) 
2. [Synopsis Custom Compiler](#Synopsis-Custom-Compiler)
3. [Operation](#Operation)
4. [Reference Circuit Details](#Reference-Circuit-Details)
5. [Simulated Circuit Details](#Simulated-Circuit-Details)
6. [Acknowledgement](#Acknowledgement)
7. [References](#References)
8. [Author](#Author)
## Abstract 
Now-a-days among different memory elements SRAM(Static Random Access Memory) became very popular because of their high speed operations and low power consumption.The most common SRAM cell used in todays applications are 6T SRAM.The read operation in 6T SRAM is slow because of the time taken by the access transistors to access the memory part(latch) of the SRAM, which further results in increase of leakage power.So,In this paper we will discuss about the quadruple cross-coupled storage cells (QUCCE) 12T SRAM which has better soft error tolerance, time performance,read static noise margins,hold static noise margins solves the limitations of conventional 6T SRAM.
## Synopsis Custom Compiler 
The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. It delivers industry-leading productivity, performance, and ease-of-use while remaining easy to adopt for users of legacy tools.

![custom_compiler](https://user-images.githubusercontent.com/100586116/156113543-8e429db2-809c-4439-8a1c-53f9264caeca.png)
## Operation 
The QUCCE 12T memory cell has four storage nodes A, Q, QN and B. Node Q and B are connected to BL through access transistor N5 and N7 respectively while node QN and A are connected to BLB through access transistor N6 and N8 respectively. Access transistors N5, N6, N7 and N8 are controlled by word line WL and will be activated when WL is set to be high. As is presented in Fig. 1, the stored ‘0’ value is assumed and the four storage nodes A, Q, QN and B are set to be ‘1’, ‘0’, ‘1’ and ‘0’ respectively. There are three modes of operation of 12T SRAM:
1. In hold mode WL=‘0’ to turn off the four pass gates N5, N6, N7 and N8. Transistors P1, N2, P3 and N4 are turned on while transistors N1, P2, N3 and P4 are turned off. Thus storage nodes A, Q, QN and B keep their original value without being changed.
2. For read operation, two bit-lines BL and BLB will be pre-charged to supply voltage and WL=VDD to turn on pass gates N5, N6, N7 and N8. As for the ‘read 0’ operation in
Fig., BLB will keep its original state Meanwhile, BL will be discharged through two paths, one from transistor N5 and N2 to the ground, and the other from transistor N7 and N4 to the ground. The voltage difference obtained from BL and BLB will be amplified and afterwards the data stored in the memory cell will be output. Due to the two discharging paths,the QUCCE 12T cell acquires a high speed read operation.
3. In order to write ‘1’ into the QUCCE 12T cell, as Fig. portrays, WL=BL=‘1’ while BLB=‘0’. The access transistors N6 and N8 activated, BLB pulls down the potential at nodes
QN and A to be ‘0’ and thus transistors N2 and N4 are turned off while transistors P2 and P4 are turned on, resulting in nodes Q and B being charged to be ‘1’. On the other side, the access transistors N5 and N7 enabled, BL pulls up the potential at node Q and B through transistor N5 and N7 towards (VDDVTHn) respectively. The pull-up strength of high state bit-line is weak because of an NMOS threshold voltage (VTHn) drop.Meanwhile, the cross-coupled latch structures will further amplify the voltage difference between the related node pairs in the latch, accelerating the buildup of voltage difference.
## Reference Circuit Details 
### Reference Circuit 
![circuit](https://user-images.githubusercontent.com/100586116/156113502-fd0c8583-4b9e-43d4-959c-5b694fa1b4df.PNG)
### Reference Waveforms
![refwaveforms](https://user-images.githubusercontent.com/100586116/156113559-19ffc695-f0c5-44e0-9882-3f918ed49a2b.PNG)
## Simulated Circuit Details 
### Circuit Schematic 
![1](https://user-images.githubusercontent.com/100586116/156121649-32b9f78e-4bad-4537-8d81-18224b1cbefd.PNG)
### Ciruit Symbol 
![2](https://user-images.githubusercontent.com/100586116/156121664-7988f665-3cba-445a-9e54-e9a5c176e93b.PNG)
### Circuit testbench Schematic 
![3](https://user-images.githubusercontent.com/100586116/156121666-da6c7fc7-7381-4031-a31c-6c5589a76c32.PNG)
### Waveforms 
![5](https://user-images.githubusercontent.com/100586116/156127927-f1914f6e-2afa-49fc-bb7c-a1ff5de14072.PNG)
## Acknowledgement 
1. Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.
2. Chinmay panda, IIT Hyderabad
3. Synopsys Team 
## References 
[1] Jianwei Jiang , Yiran Xu, Wenyi Zhu, Jun Xiao, and Shichang Zou "Quadruple Cross-Coupled Latch-Based 10T and 12T SRAM Bit-Cell Designs for Highly Reliable Terrestrial Applications"
IEEE Transactions on Circuits and Systems–I: REGULAR PAPERS,
VOL. 66, NO. 3, MARCH 2019
## Author 
B.Venkata Bharadwaj, 4th Year B.TECH, ECE, Indian Institute of Information Technology Design and Manufacturing(IIITDM) Kancheepuram

Email: venkatabharadwaj125@gmail.com
