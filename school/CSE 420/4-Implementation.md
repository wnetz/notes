# 4-Implementation
![[MIPS Machine (with Controls).png]]
## MIPS Organization
![[MIPS Organization.png]]
- 8 bits = 1 byte
- 32 bits = 4 bytes =  1 word
- width of address bus determines the **32 or 16** processor 
- MIPS memory is split into 16 segment each has 2^28 bytes

## Fetching Instructions
![[Fetching Instructions.png]]
*instructions address must be dividable by 4*

## Decoding Instructions
![[Decoding Instructions.png]]

## R-Type
![[Executing R Format Operations.png]]
#R-Type [op, rs, rt, rd, shamt, funct]
- R-type is an arithmetic  instruction
	- op and funct are 6 bits
	- rs, rt, rd, and shamt are 5 bits
- perform op on rs and rt then store in rd [[register]]

## I-Type
#I-Type [op, rs, rt, address offset]
- I-Type is a load or store instruction
	- op is 6 bits
	- rs and rt are 5 bits
	- address offset is 16 bits
- address offset must be expanded form 16 to 32 bits

sign extend keeps the sign wile also changing number to a 32 bit number for the [[ALU]]. this is done so that you can go both forward and backward in memory.

### Executing Load and Store
![[Executing Load and Store.png]]
- location is rs + offset

### Executing Branch Operations
![[Executing Branch Operations.png]]
- the base register is the [[PC]]
- branch instructions branch relative to the next instruction
- branch instruction can be move between memory segments because it is [[PC]]  relative

## J-Type
![[Executing Jump Operations.png]]
#J_Type [op, jump target address]
- J-Type is a jump instruction
	- op is 6 bits
	- jump target address is 26 bits
- jump instructions cant jump from one memory segment to another unless you are on the last instruction of the segment
