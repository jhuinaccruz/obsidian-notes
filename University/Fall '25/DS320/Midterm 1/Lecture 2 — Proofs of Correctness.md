
__A full proper analysis of an algorithm addresses two key aspects__:
- Correctness (prove the algorithm produces correct solutions)
- Running time (prove the algorithm to be efficient)

>*In general, when you are solving problems in this course, you should prioritize correctness.*

__When analyzing runtime, break up the algorithm into__:
- Operations *outside* the loops
- Operations *within* the loops

__When analyzing correctness, analyze using__: Induction
- Base case
- Hypothesis
- Step

__Loop invariant__: Something that is true before and after ever iteration of a loop. A loop invariant is proven through
- Initialization: It is true prior to the first iteration of the loop
- Maintenance: It is true before an iteration of the loop, and remains true before the next iteration
- Termination: When the loop terminates, the invariant gives us a useful property that helps show that the algorithm is correct

## Comparison-Based Lower Bound via a Counting Argument
__Comparison Model__: A model, where the running time of an algorithm corresponds to the depth of the tree. When an algorithm operates under such model, it is written as a binary decision tree in which
- Vertices/nodes are labeled with a fixed comparison
- Computation proceeds as a root-leaf path down the tree
	- Left if the comparison is True
	- Right otherwise
- Leaves are labeled with the output of the algorithm