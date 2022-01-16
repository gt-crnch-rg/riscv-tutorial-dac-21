# RISC-V tutorial at [DAC-58](https://www.dac.com/Conference)  (Dec 08 2021) 

**Description:**

This is an in-person workshop hosted at DAC-54. The tutorial information can be found on the [official DAC page](https://58dac.conference-program.com/presentation/?id=TUT101&sess=sess326).


## Date: 2021-12-18 (10:30 AM - 12:00 PM PST)
## Location: Room 3000, Moscone Center

## Organizers/Speakers:

* David Donofrio, John Leidel - Tactical Computing Laboratories 
* Anastasiia Butko - Lawrence Berkeley National Lab
* Jeffrey Young - Georgia Institute of Technology

## Registration 
How to register: [DAC-58 registration link](https://www.dac.com/Attend/Registration) 



## Tutorial schedule

|  Time | Contents  | Presenter   | Slides  | Notes  |
|---|---|---|---|---|
| 10:30-11:00 | Open-source Hardware / Software Co-design | David Donofrio  | [Slides](https://github.com/gt-crnch-rg/riscv-tutorial-dac-21/blob/main/Slides/DAC58%20-%20Closing%20the%20HW-SW%20Codesign%20Loop%20-%20Opensource%20HW%20SW%20Codesign.pdf)  |   |
| 11:00-11:20 | Hands-on Exercises | John Leidel, Dave Donofrio  |   |   |
| 11:20-11:40 | Open2C: Open-source Generator for Coherent Cache Memory Subsystem | David Donofrio |[Slides](https://github.com/gt-crnch-rg/riscv-tutorial-dac-21/blob/main/Slides/DAC58%20-%20Closing%20the%20HW-SW%20Codesign%20Loop%20-%20Open2C.pdf) | Research by Anastasiia Butko and colleagues |
| 11:40-12:00 | Novel RISC-V Implementations and Accelerators | Jeffrey Young | [Slides](https://github.com/gt-crnch-rg/riscv-tutorial-dac-21/blob/main/Slides/DAC58%20-%20Closing%20the%20HW-SW%20Codesign%20Loop%20-%20Novel%20RISCV%20Implementations.pdf) | |
| 12:00 | Wrap-up |  |  | 

## Materials for the Hands-on portion 
We'll be using the System Architect CoreGen repository [here](https://github.com/opensocsysarch/CoreGen) for the hands-on portion of this tutorial. The [BasicRV32I.yaml file under Exercises](https://github.com/gt-crnch-rg/riscv-tutorial-dac-21/blob/main/Exercises/BasicRV32I.yaml) will be used as the starting file for the hands-on portion of the tutorial.

## VM Images and Remote Temporary Accounts

[Remote Access for the DAC-58 RISC-V GPGPU tutorial](Remote%20Access%20for%20the%20DAC-58%20RISCV%20tutorial.md)

VM Access (Optional): Please see the ["VM README"](VM_Imgs/VM_README.md) to get instructions for downloading and running the System Architect tools using Vagrant and VirtualBox. We suggest you use this option to continue your exploration after the tutorial as the image is somewhat large (1.1 GB).

For remote account access, please see [this page](Remote%20Access%20for%20the%20DAC-58%20RISCV%20tutorial.md). If you'd like a longer-term account to work with Coregen and the tools on a remote testbed, please [request an account for the CRNCH Rogues Gallery testbed here](https://crnch-rg.cc.gatech.edu/request-access/).

## Relevant Repos 
* [CoreGen](https://github.com/opensocsysarch/CoreGen) 
* [Vortex - Georgia Tech RISC-V GPGPU](https://github.com/vortexgpgpu/)
