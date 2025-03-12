# Introduction
A computer consists of the following components:
- Input Unit
- Storage
- Central Processing Unit (CPU)
- Output Unit
# CPU
consists of 3 components:
- Arithmetic Logic Unit
- Control Unit
- Registers

### Arithmetic Logic Unit (ALU):
- Performs all four arithmetic operations (+, -, \*, /) and some logical operations (>, <, =, >=, <=, !=)
- When an operation is called, numbers are sent from memory to ALU where the operation takes place and the result is put back in the memory.

### Control Unit (CU):
- Controls and guides the interpretation, flow of data and information, program execution
- It get program instructions from the memory and the instruction is then decoded and interpreted. Then the opertaion is carried out and the signal to send the next instruction is sent to memory.
- It even controls the flow of data from input devices to memory and memory to output devices.

### Registers
- Small units of data holding places.
- Registers are used to store important processing information during the processing.
- CPU may store some part data, memory address or instruction in process registers.

# Memory (Storage)
- Each memory location has its own memory address
- a bit (b) is an elementary unit of the memory. Can be either 0 or 1.
- 8 bits form 1 Byte (B).
- (2^10^) 1024 bytes form 1KiloByte(KB) and so on.
- Primary memory is fast, volatile (temporary) memory which is lost upon power being switched off.
- Secondary memory is slow (comparitively), permanent memory which is retained upon power being switched off.

## Random Access Memory (RAM)
- In RAM, the memory cells can be accessed for information transfer from any desired memory location.
	- Therefore, the process of location something in memory is same and requires equal amount of memory, thus the name "random access".
- It is volatile memory.
**Note:** the amount of time taken to produce data from memory, from the start of access until the availability of data is called memory access time.

There are 2 basic types of RAM:
1) Dynamic RAM (DRAM):
	- Made from transistors & capacitors.
	- Access time range from 20 to 70 ns
	- Used in the primary storage sections of most computers.

2) Static RAM (SRAM):
	- Made of flip-flops: binary cell capable of storing one bit of information.
	- Access time ~ 10ns
	- Used in specialized applications.

## Read Only Memory (ROM)
- Performs read operations only, does not have write capability.
- Used for applications where it is known that information does not ever need to be altered.
- Slower than RAM

ROM has the following types:
1. PROM (programmable ROM):
	- Also called OTP (One Time Programmable).
	- User programmable memory which is burnt using ROM burner.
2. EPROM (Erasable Programmable ROM):
	- One can program the memory chip and erase it as many times as needed.
	- Erasing can take place through various mechanisms e.g. UV Radiation which takes upto 20mins.
	- Here, the erasing erases fully.
3. EEPROM (Electrically Erasable Programable ROM):
	- EPROM is erased electrically which is faster.
	- Here, selective bytes can be erased.
4. Flash EEPROM:
	- similiar to EEPROM but is comparitively fast. (erasure of entire contents take less than a second.)
	- It erases fully, not selectively.
5. Mask ROM:
	- Type of ROM in which the contents are programmed by the IC manufacturer.
	- It is not a user-programmable ROM
# Cache Memory
- Memory cache also called cache store or RAM cache
- Special, high-speed storage mechanism.
- It can be either a reserved section of main memory, independent high-speed storage device or even on CPU chip.
- Whenever data is required, the CPU first looks in the cache and only then proceeds to memory. If it is found in the cache, CPU does not access memory and hence the process becomes very fast.
- A portion made from high speed Static RAM (SRAM) instead of slower and cheaper Dynamic RAM (DRAM) used for main memory.
- Memory caching is effective because most programs access the same data over & over again.
- When a data is found at cache, it is called a cache hit, and the effectiveness of a cache is judged by its hit rate.

# Common Storage Devices
These are secondary storage devices that are used to store large amount of data permanently.
|<center>Magnetic</center>|<center>Optical</center>|<center>Flash Memory</center>|
|:---|:---|:---|
|Hard Disk|CD, DVD, Blu-Ray|USB-Stick, SD-Card
## 1) Hard Disk
- Information is stored on one or more circular platters (or disks) which are continually spinning.
- These rotating disks are coated with a magnetic material and stacked with space between them.
- Information is recorded on the surface of rotating disks by magnetic heads as tiny magnetic spots.

## 2) Optical Media
Consists of :
- Compact Disk (CD)
- Digital Versatile Disk (DVD) / Super Density Disk (SD)
- Blu-Ray (BD)

Here, CD & DVD use a red laser (650nm) whereas Blu-Ray uses a blue-violet laser(405nm) and due to smaller wavelength the laser spot can be focused for greater precision which allows data to be packed tightly and stored in less space which allow Blu-Ray to fit more data on the disc even though it's the same size as CD/DVD.
1. X-ROM: 
	- Short for X-Read Only Memory
	- Read only, cannot write any data to it.
2. X-R
	- Short for X-Recordable
	- Can be written only once and becomes read-only after that.
3. X-RW
	- Short for X-Rewritable
	- Erasable disk that can be written on multiple times.
4. X-RAM

## 3) Flash Memory
- Small, ultra portable storage device with 'solid state' memory.
- It has no moving parts nor does it make use of lasers, instead it works in a similiar way to RAM but retain memory after power is switched off.

# System Bus
- An electronic pathway composed of connecting cables that connect the major components.
- Through system bus, data and instructions are passed among the computer system components.
- It can be categorized as: 
	- The data carrying part of the system is called the data bus.
	- The control instruction carrying part is called control bus.
	- The memory address carrying part is called address bus.
- A separate bus connecting the input & output is called the I/O bus.

# Mobile System Organization
These days major components of a mobile system are integrated on a single chip called System on Chip (SoC). The SoC consumes less power compared to the other alternatives.
## Mobile Processors
Contain 2 major sub-processor types:
1. Communications Processing Unit (Mobile System I/O Unit)
	- Responsible for making and receiving phone calls.
	- It has a Digital Signal Processor (DSP) that helps it work with RF Transceiver and the Audio subsystem.
	- Radio Signal Management Unit (Radio Signal Processors) is responsible for connecting SIM (which provides a type of modem) to the base stations through radio signals.
2. Applications Processing Unit (APU)
	- Responsible for governing, controlling all types of operations taking place on a mobile system by running various types of mobile applications. (apps)

## Display Subsystem
Includes display and touch-sensitve components

## Camera Subsystem
It has an integrated Image Signal Processor that controls image capture, high-resolution support, image stabilization, image enhancements etc.