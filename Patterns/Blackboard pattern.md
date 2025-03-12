[[Architecture Patterns Index]] #Decoupling #Microservices
# Blackboard pattern

This is a problem solving approach that uses a modular and decentralised framework.

It is used for complex problems that lack a single well defined algorithm or pre-determined architecture.

Often it is used as a transitional architecture early in a project and then as things become clearer you switch to a more appropriate architecture.

"The architecture is based on how people work together around a blackboard – each person would sit around the board and a problem would be written on it. When a person can solve the problem, they would go to the board and add the partial solution they know how to do. This process is repeated until a collective solution is found."

"The blackboard pattern describes the overall flow of information and control within the blackboard architecture. It typically involves the following steps:

1. ****Initialization:**** The blackboard is set up with the initial problem statement and any available input data.
2. ****Activation:**** The controller selects and activates one or more knowledge sources based on the current state of the problem and the available data on the blackboard.
3. ****Execution:**** The activated knowledge sources independently analyze the problem, apply their specialized algorithms or techniques, and produce partial solutions or hypotheses.
4. ****Conflict resolution:**** If multiple knowledge sources generate conflicting or overlapping solutions, a conflict resolution mechanism is employed to reconcile the differences and select the most appropriate solution(s).
5. ****Update:**** The knowledge sources update the blackboard with their outputs, such as new constraints, proposed solutions, or intermediate results.
6. ****Iteration:**** The controller repeats the activation and execution steps until a satisfactory solution is reached, convergence criteria are met, or a predefined time limit is exceeded."

![[Pasted image 20240904075003.png]]

![[Pasted image 20240904075535.png]]

This sequence diagram shows a Control node, three knowledge sources and a Blackboard node:
![[Pasted image 20240904075243.png]]