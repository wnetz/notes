# 4-Implementation
![[MIPS Machine (with Controls).png]]
## MIPS Organization
![[MIPS Organization.png]]
8 bits = 1 byte
32 bits = 4 bytes =  1 word
width of address bus determines the **32 or 16** processor 


## Fetching Instructions
![[Fetching Instructions.png]]
*instructions address must be dividable by 4*


## Decoding Instructions
![[Decoding Instructions.png]]

## R-Type
![[Executing R Format Operations.png]]
#R-Type [op, rs, rt, rd, shamt, funct]
R-type is an arithmetic  instruction
perform op on rs and rt then store in rd [[register]]

## I-Type
#I-Type [op, rs, rt, address offset]
I-Type is a load or store instruction
address offset must be expanded form 16 to 32 bits
### Executing Load and Store
![[Executing Load and Store.png]]
location is rs + offset
### Executing Branch Operations
![[Executing Branch Operations.png]]
the base register is the [[PC]]




## J-Type
![[Executing Jump Operations.png]]
#J_Type [op, jump target address]
J-Type is a jump instruction
