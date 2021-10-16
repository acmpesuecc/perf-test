# Perf-test

> :warning: **All the code present in this repository must be run preferably on a virtual machine as there is a possibility the code can harm the machine!Any how a force reboot should fix it.**


## Project Contributors:

* [Navin Shrinivas](https://github.com/NavinShrinivas)<br>


# Project Info:
Use CMake to build this project. This may seem like an over-engineered solution, however it is essential to make the program platform independent, which would solve all package problems faced at once. <br>


## Usage:
### Linux
  On Linux systems, after ensuring ```cmake``` is insatalled, run:
  ```bash
  $ git clone https://github.com/acmpesuecc/perf-test
  $ cd perf-test
  $ chmod +x install.sh
  $ install.sh
  $ ./perftool
  ```
  No additional external libraries are required. <br>
  
## Access style:
  The entire program is fully accessible through commands in the terminal, but also can be used as a menu driven program with 
  ```./perftool menu``` <br>

## Issues faced and resolved:

*  Multithreading was one of the most major issues, deciding where the controls flow, etc. We figured it out by asking other developers in StackOverflow
   and analysing other multithreaded application.
*  We encountered the race conditions problem, due to multithreading, multiple IOs on a single memory and rapid `while` loops. Our workaround was introducing      consistency by using various buffers and adding them up in the end.

