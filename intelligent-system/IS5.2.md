# Evolution Strategies and Genetic Programming
## Evolution Strategies
(1+1)-evolution strategy, one parent generates one offspring per generation by applying normally distributed mutation.

Unlike GAs, evolution strategies only a mutation operator.

Steps
- Choose the number of parameters N to represent the problem and then determine a feasible range for each parameter.
![](attachments/Pasted%20image%2020211010171110.png)

- Randomly select an initial value for each parameter form respective feasible range. The set of these parameters will constitute the initial population of parent parameters
![](attachments/Pasted%20image%2020211010171208.png)

- Calculate the solution associated with the parent parameters
![](attachments/Pasted%20image%2020211010171235.png)

- Step 4. Create a new (offspring) parameter by adding a normally distributed randomm variable a with mean zero and pre-selected deviation to each parent parameter.
![](attachments/Pasted%20image%2020211010171952.png)
Normally distributed mutations with mean zero reflect the natural process of evolution (smaller changes occur more frequently than larger ones).

- Calculate the solution associated with offspring parameters
![](attachments/Pasted%20image%2020211010172119.png)

- Compare the solution associated with the offspring parameters with the one associated with the parent parameters. If the solution for the offspring is better than that for the parents, replace the parent population with the offspring population. Otherwise, keep the parent parameters.

- Go to Step 4, and repeat the process until a satisfactory solution is reached or a specified number of generations is considered.

## Genetic Programming
Extension of the conventional genetic algorithm, It evolves the computer code that solves the problem, not just a bit-string representation. 
LISP was chosen as the main language for genetic programming

### LISP
symbol-oriented structure. ITs basic data structures are atoms and lists. Integer, variable, and string are examples of LISP atoms. Object that is composed of atoms or other lists called a list (it is written as an ordered collection of items inside a pair of parentheses).

List example
(-(\*AB\*)c) , it is the same as calculation (A\*B)-C

![](attachments/Pasted%20image%2020211010230823.png)

Both atoms and lists are called symbolic expressions or S-expressions. In LISP, all data and all programs are S-expressions. This gives LISP the ability to operate on programs as if they were data (can modify themselves or write other LISP programs).

Before applying genetic programming to a problem:
1. Determine the set of terminals
2. Select the set of primitive function.
3. Define the fitness function.
4. Decide on the parameters for controlling the run.
5. Choose the method for designating a result of the run.

**Illustration**
![](attachments/Pasted%20image%2020211010231049.png)
![](attachments/Pasted%20image%2020211010231134.png)

1. Determine the set of terminals, correspond to the inputs of the computer program to be discovered. It takes two inputs, a and b
2. Select the set of primitive functions, using four standard arithmetic operations (+, -, \*, and /) plus sqrt.
3. Define fitness function, fitness function can be measured by the error between the actual result produced by the program and the correct result given by the fitness case.Typically, the error is not measured over just one fitness case, but calculated as a sum of the absolute errors over a number of fitness cases, The closer this sum is to zero, the better the computer program
4. Decide on the parameters for controlling the run, for this, genetic programming uses the same primary parameters as those used for GAs.
5. Choose the method for designating a result of the run, designate the best so far generated program as the result of a run.

![](attachments/Pasted%20image%2020211010231944.png)
![](attachments/Pasted%20image%2020211010231959.png)

**Mutation** can randomly change any function or any terminal in the LISP S-expression. A function can only be replaced by a function and a terminal can only be replaced by a terminal.
![](attachments/Pasted%20image%2020211010232206.png)

**Steps**
1. Assign the maximum number of generations to be run and probabilities for cloning, crossover, and mutation. Note that the sum of the probability of cloning, the probability of crossover and the probability of mutation must be equal one.
2. Generate an initial population of computer programs of size N by combining randomly selected functions and terminals.
3. Execute each computer program in the population and calculate its fitness. Designate the best-so-far individual as the result of the run.
4. With assigned probabilities, select a genetic operator to perform cloning, crossover or mutation.
5. If the cloning operator is chosen, select one computer program from the current population of programs and copy it into a new population.
  - If the crossover operator is chosen, select a pair of computer programs from the current population, create a pair of offspring programs and place them into the new population.
  - If the mutation operator is chosen, select one computer program from current population, perform mutation and place the mutant into the new population.
6. Repeat step 4 until the size of the new population of computer programs becomes equal to the size of the initial population, N
7. Replace the current (patent) population with the new (offspring) population
8. Go to step 3 and repeat the process until the termination criterion is satisfied.

![](attachments/Pasted%20image%2020211011063933.png)

**Benefits of genetic programming vs genetic algorithms**
- Applies the same evolutionary approach, however, genetic programming does not breed bit strings but complete computer programs.
- The fundamental difficulty of GAs lies in the problem representation (fixed-length coding). A poor representation limits the power of GA or may lead to false solution.
- Fixed-length coding is rather artificial, it cannot provide a dynamic variability in length, such a coding often causes redundancy and reduces the efficiency of genetic search. In contrast, genetic programming uses high-level building blocks of variable length. Their size and complexity can change during breeding.
- Genetic programming works well in a large number of different cases and has many potential applications.


