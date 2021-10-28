# Register Scoreboarding
ALU is not unified
## Data Hazards
### RAW
caused by data dependencies
![[RAW.png]]

### WAR
called an "ant-dependence"
![[WAR.png]]
cant happen in MIPS 5 stage pipeline because
- all instructions take 5 stages
- reads are always on stage 2
- writes are always on stage 5

### WAW
called an output dependence
![[WAW.png]]
cant happen in MIPS 5 stage pipeline because
- all instructions take 5 stages
- writes are always on stage 5

## Out of Order Execution
instructions fetched and commit in order, but execute out of order

### Register Scoreboarding
WAR Solution
- stall writeback until registers have been read
- read registers only during read operation

WAW Solution
- detect hazard and stall issue of new instruction until other instruction completes

keeps track of dependencies between instructions that have been issued
![[Register Scoreboarding pipeline.png]]

functional unit status
- Busy: Indicates whether the unit is busy or not
- Op: Operation to perform in the unit (e.g., + or –)  
- Fi: Destination register
- Fj,Fk: Source-register numbers
- Qj,Qk: Functional units producing source registers Fj, Fk  
- Rj,Rk: Flags indicating when Fj, Fk are ready