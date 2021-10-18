# 6-Control Hazards
they are less common that data hazards, but harder to resolve
## How Bad are Branches
getting target address
![[Get target address.png]]
resolving conditions
![[Resolve conditions.png]]

## Solutions
### Branch Delay Slot
after the branch instruction insert an instruction that is not dependent on the branch to allow time for calculation
searching for an independent instruction can be expensive and sometimes impossible
if there are no independent instructions fill the slot with a NOP
penalty = 0
![[Before Branch.png]]
penalty = 1 to T
![[After Branch.png]]
assuming R7 contains the older value of R9
penalty = T
![[In Branch.png]]

### Predication
converts control dependencies into data dependencies
when it works its great, but when it fails it is significantly worse
![[Branch Predication.png]]