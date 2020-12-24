# Entry 10: The Halting Problem
The halting problem is a problem that proposes the question of "if given a computer program and an input, will the program terminate or go forever?" This problem is infamous for being undecidable as it was proven that there is no machine capable of solving the halting problem. In 1936, Alan Turing proved that the halting problem was undecidable for Turing machines using the following logic:

Suppose there is a Turing machine A that decides the halting problem. Now consider a Turing machine B that takes an input p and runs A on input (p, p) and halts if and only if A doesn't halt. The outcomes of this machine are either "yes, p on input p halts" and the program loops forever or "no, p on input p doesn't halt" and it terminates. A paradox is introduced when B is fed into itself as an input. The following two cases emerge: 
1. A halts and so does B on input B. This is impossible by the definition of B because B can only halt if A does not. 
2. A doesn't halt and neither does B on input B. This is also impossible because B will halt if A doesn't.

This proof derived by Turing illustrates exactly why the halting problem may never be solved by a machine and is thus undecidable.
