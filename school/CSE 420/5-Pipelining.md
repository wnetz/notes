# 5-Pipelining
![[The Promise of Pipelining.png]]
![[The “new look” dataflow.png]]
- pipelining is  parallelism
- has a theoretical linear speed up
- #J-Type and #I-Type  are done in decode section
- operates best when length of stages are balanced

## hazards
- structural hazard
	- happens when a resource is needed in multiple segments
	- ![[Structural Hazard.png]]
	- ![[Structural Hazard Solution.png]]
- data hazard
	- happens when an instruction needs data produced by an earlier instruction
	- ![[Data Hazard.png]]
	- ![[Data Hazard Solution.png]]
- control hazard