# Basic Operational Concepts
- Program Counter (PC): Register which holds the memory address of the current instruction.
- Instruction Register (IR): Holds the current instruction.
- General Purpose Register: Holds data and addresses (`R0, R1, ...`)
- Control Circuits and ALU fetch and execute the instructions.

## Another Example
```asm
STORE LOC, R4
```
1. Send address in PC to memory; issue Read.
2. Load instruction from memory to IR.
3. Increment PC to point to next instruction.
4. Send address LOC to memory; issue Write.
5. Store word from register R4 into LOC.


## Example for `OPERATE`
```asm
ADD R4, R2, R3
```
1. Send address in PC to memory; issue Read.
2. Load instruction from memory to IR.
3. Increment PC to point to next instruction.
4. Add the contents of R2 and R3.
5. Store the result (sum) in R4.

\<addition and subtraction comes here>

# Memory Locations & Addresses.
- Memory consists of millions of storage cells called **flip-flops**.
- Each cell can store 1 bit of information.
- Each group of $n$ bits is called a **word** of information.
  - Where $n$ is the word length.
    - This value can vary from 8/16 to 64 bits.
- A group of 8 bits is called a byte
  - A group of 4 bits is called a nibble.


- Accessing the memory to store or retrieve a single item of information (word / byte) requires distinct addresses for each item locations:
  - It is customary to use numbers from $0$ to $2^k-1$ as the adderss of successive locations in memory.
    - Where $k$ is the size of address (in (address length) bits).
  - If $2^k = \text{number of addressable locations}$:
    - Then $2^k$ constitutes the address space of the computer.
      - e.g. a 24-bit address generates an address space of $2^{24}$ locations. (16 MB)

\<insert example here>

## Byte Addressability
- Byte size is always 8b.
- Word length can range from 16-64b.
- Impractical to assign an address to each bit.
- Instead, provide byte-addressable memory that assigns an address to each byte.
- Byte locations have addresses 0, 1, 2, ....
- Assuming word length = 32b
  - Word locations have addresses 0, 4, 8, ...

### Two ways of Byte address assignment accross words.
- Big endian and little endian are terms that describe the order in which a sequence of bytes are stored in computer memory.
1) Big Endian: Assigns lower byte address to <u>MSB</u> of words.
2) Little Endian: Assigns lower byte addresses to <u>LSB</u> of words.

e.g. 2064 when using 4 bits per digit i.e. 2 digits per byte.
|Big-endian|Little-endian|
|:--------:|:-----------:|
|20(MSB) 64(LSB)|64(LSB) 20(MSB)|

\<keyboard char example>

### Memory word alignement
- Words are said to be aligned in memory, if they begin at a byte-address that is a multiple of number of bytes in a word.
  - for e.g. if the word length 16 (2 bytes), aligned words begin at byet address 0, 2, 5.
- Words are said to have unaligned addresses if they begin at an arbitrary byte-address.

# Instructions
- A computer must have an isntruction capable of performing the following operations.
  - Data tranfer between memory and process registers (e.g. `LOAD, MOVE, STORE`)
  - Arithmetic and logical operations on data (`ADD, SUB`)
  - Program sequencing and control (`BRANCH, CALL, RET`)
  - I/O transfer (`IN, OUT`)

## Register Transfer Notation
The possible locations that may be involved during data transfer are:
1. Memory Location
2. Processor Register.
3. Register in I/O subsystem.

Use `[]` to denote contents of a location.

Use `<-` to denote transfer to a destination.

Example:
```
R2 <- [LOC]
```
(Transfer from LOC in memory to register R2)

## RISC & CISC
Two fundamental approaches in design of instruction sets for modern computers.

|Reduced Instruction Set Computer (RISC)| Complex Instruction Set Computers (CISC)|
|:-------------------------------------:|:---------------------------------------:|
|Have one word instruction and require arithmetic operands to be in registers.|Have multi-word instructions and allow operands directly from memory.|


## RISC Format
1. `LOAD`
```
LOAD dest, source
//or
LOAD proc_reg, mem_loc
```

2. `STORE`
```
STORE src, dest
//or
STORE proc_reg, mem_loc
```
2. `LOOP`
```
LOOP:
  body
Branch_if_<condition> LOOP
```

## Addressing Modes
The term addressing modes refers to the way in which the operand of an instruction is specified.

Information contained in the instruction code is the value of the operand of the address of the operand.

Following are the main addressing modes that are used in various platforms and architectures.

1. Register Addressing Mode
2. Immediate Addressing Mode
3. Absolute (or Direct) Addressing Mode
4. Register Indirect Addressing Mode
5. Index Addressing Mode
6. Base with Index Addressing Mode

### 1. Register Addressing Mode
Effective address: Register name specified in the instruction.

e.g. `ADD R0, R1, R2`

### 2. Immediate Addressing Mode
Effective Address: Operand value given in the instruction

e.g. `ADD R1, R1, #10` implies R1 <- [R1]+10

e.g. `MOVE R1, #10` implies R1<-10


### 3. Absolute (or Direct) Adderssing Mode
Here, the operand is a memory location.

Effective Address: Address of the memory location given directly in the instruction.

e.g. `MOVE R1, LOCA` implies R1 <- [LOCA]

### 4. Register Indirect Addressing Mode
Neither operands nor addressis are given explicitly. The instruction provides the information from which the address of the operand is determined.

i.e. The instruction provides effective address of the operand using register. The indirection is denoted by `()` around register.

Effective Address: Contents of a register that is specified in the instruction.

e.g. `ADD R2, R2, (R1)` imples R2 <- [R2] + [[R1]]
<br>where R1 contains the memory address of R2.

e.g. `ADD (R1), (R1), R2` implies R1 <- address of ([[R1]] + [R2])
<br>again, here R1 contains the memory address of R2

### 5. Index Addressing Mode
- The effective address of the operand is generated by adding a constant value to the contents of a register specified in the instructions. The register in this case is called the index register.

The operation is indicated as $X(R_i)$

Effective Address: $X+R_i$ where $X$ is the constant value (signed int) and $R_i$ is the index register.

e.g. `LOAD R2, 5(R1)` implies R2 <- [5+[R1]]

Here the value located at the address located 5 spaces after R1's value will be loaded into R2.

### 6. Base with Index Addressing Mode
The effective address of the operand is generated by adding 2 registers specified in the instruction.

The operation is indicated as $(R_i,\  R_j)$

Effective Address: $R_i+R_j$ where $R_i$ is used as the base register and $R_j$ is used to contain the offset.

e.g. `LOAD R2, (R1, R3)` implies R2 <- [[R1]+[R3]]

\<insert a picture of the summary here>
