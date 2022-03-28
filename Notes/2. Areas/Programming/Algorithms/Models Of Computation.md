### Models Of Computation
> Notes Handwritten: [[Handwritten-Models-Computation.pdf]]
> Resources (PDF): [[Models-Computation.pdf]]

#### What is an algorithm?
- Mathematical abstraction of computer program
- Computational procedure to solve a problem
![[Algorithm.png]]

> Read [[Algorithms]], for more..

**History**: "Father of algebra" [Al-Khw¯arizm¯ı “al-kha-raz-mi” (c. 780-850)](https://en.wikipedia.org/wiki/Muhammad_ibn_Musa_al-Khwarizmi) and his book ["The compendious Book on Calculation by Completion & Balancing"](https://en.wikipedia.org/wiki/The_Compendious_Book_on_Calculation_by_Completion_and_Balancing)

__Model of computation__ specifies:
- what operations an algorithm is allowed
- cost (time, space, ... ) of each operation
- cost of algorithm = sum of operation costs
#### Random Access Machine (RAM)
![[RAM.png]]
#### Pointer Machine
- dynamically allocated objects (namedtuple)
- object has 0(1) fields
- field = word(e.g., int) or pointer to object/null (a.k.a reference)

![[DocDist.png]]

#### Python Model
Read about python model in the PDF source: [[Models-Computation.pdf]]

#### Document Distance Algorithm
1. split each document into words
2. count word frecuencies (document vectors)
3. compute dot product (& divide)

![[Pasted image 20220325111804.png]]

**Code Example:**
1. 228.1 seconds to solve.
2. 164.7 seconds to solve.
3. 123.1 seconds to solve. 
4. 71.7 seconds to solve. 
5. 11.5 seconds to solve. 
6. 11.5 seconds to solve.
7. 1.8 seconds to solve. 
8. 0.2 seconds to solve. [[Docdist]]

#### Aditional Sources:
[MIT Class](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-006-introduction-to-algorithms-fall-2011/lecture-videos/lecture-2-models-of-computation-document-distance/)
