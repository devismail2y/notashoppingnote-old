# Evolutionary Computation
Intelligence can be defined as the capability of a system to adapt its behavior to changing environment 

i.e. optimization algorithm.

Evolutionary computation = evolutionary approach based on computational models of natural selection and genetics. This is an umbrella term that combines
1. Genetic algorithms
2. Evolution strategies
3. Genetic programming

## Evolutionary Fitness
- Evolution can be seen as a process leading to the maintenance of a population's ability to survive and reproduce in a specific environment.
- Measure of the organism's ability to anticipate changes in its environment.
- Quantitative measure of the ability to predict environmental changes and respond adequately, can also be considered as the quality that is optimized in natural life.

Example:
Rabbits that are faster than others possess superior fitness, because they have a greater chance of avoiding foxes, surviving, and then breeding. The child may have ability to run even faster than the parents.

## Genetic Algorithm (GA)

Makes computers do what nature does by manipulating strings of binary digits.
Each artificial chromosomes consists of number of genes, and each gene is represented by 0 or 1.
![](attachments/Pasted%20image%2020211010104417.png)

GA uses a measure of fitness of individual chromosomes to carry out reproduction. As reproduction takes place, the **crossover** operator exchanges parts of two single chromosomes, and the **mutation** operator changes the gene value in some randomly chosen location of the chromosome.

GA has two mechanisms to solve problems:
- Encoding
- Evaluation

The Algorithm
Step 1: Represent the problem variable domain as a chromosome of a fixed length, choose the size of a chromosome population N, the crossover probability (pc) and the mutation probability (pm).

Step 2: Define a fitness function to measure the performance or fitness of an individual chromosome in the problem domain. The fitness function establishes the basis for selecting chromosomes that will be mated during reproduction.

Step 3: Randomly generate an initial population of chromosomes of size N:
x1, x2, ..., xn

Step 4: Calculate the fitness of each individual chromosomes
f(x1), f(x2), ..., f(xn)

Step 5: Select a pair of chromosomes for mating from the current population. Parent chromosomes are selected with a probability related to their fitness.

Step 6: Create a pair of offspring chromosomes by applying the genetic operators - crossover (kawin) and mutation.

Step 7: Place the created offspring (keturunan) chromosomes in the new population

Step 8: Repeat step 5 until the size of the new chromosome population becomes equal to the size of the initial population, N.

Step 9: Replace the initial (parent) chromosome population with the new (offspring) population. 

Step 10: Go to step 4, and repeat the process until the termination criterion is satisfied.

**So**
GA represents an iterative process, each iteration is called a **generation**. A typical number of generations for a simple GA can range from 50 to over 500. The entire set of generations is called a **run**.

GA uses stochastic search method, the fitness of a population may remain stable for a number of generations before a superior chromosome appears.

A common practice is to terminate a GA after a specified number of generations and then examine the best chromosomes in population. If no satisfactory solution is found, the GA is restarted.

**Case study**
![](attachments/Pasted%20image%2020211010120414.png)
![](attachments/Pasted%20image%2020211010121000.png)
![](attachments/Pasted%20image%2020211010121117.png)
- In natural selection, only the fittest species can survive, breed, and thereby pass their genes on to the next generation. GAs use a similiar approach, however the size of the chromosome population remains unchanged from one generation to the next.
- The last column in the table shows the ratio of the individual chromosome's fitness to the population's total fitness. This ration determines the chromosome's average fitness improves from one generation to the next.

![](attachments/Pasted%20image%2020211010121627.png)
- In the example, we have an initial population of 6 chromosomes. Thus, to establish the same population in the next generation, the roulette wheel would be spun six times.
- Once a pair of parent chromosomes is selected, the **crossover** operator is applied.
- X6 and X5 has the bigger chance to be selected among others. Even it may be possible to have a generation from genes X5 and X6 only.

Crossover Operator
- First, the crossover operator randomly chooses a crossover point where two parent chromosomes break;  and then exchanges the chromosome parts after that point. As a result, two new offspring are created
- If a pair of chromosomes does not cross over, then the chromosome cloning takes place, and the offspring are created as exact copies of each parent.
![](attachments/Pasted%20image%2020211010122753.png)
offspring1 = 1000
offspring2 = 0101
and so on

Mutation Operator
- Mutation represents a change in the gene
- Mutation is background operator. Its role is to provide a guarantee that the search algorithm is not trapped on a local optimum.
- The mutation operator flips a randomly selected gene in a chromosome
- The mutation probability is quite small in nature, and so for GA, typically in the range between 0.001 and 0.01
![](attachments/Pasted%20image%2020211010130300.png)

GA cycle
![](attachments/Pasted%20image%2020211010130319.png)


### Case Study 2
![](attachments/Pasted%20image%2020211010132057.png)
concatenate x and y into one chunk of chromosome.
euler's number = ![](attachments/Pasted%20image%2020211010134245.png)
![](attachments/Pasted%20image%2020211010134519.png)
![](attachments/Pasted%20image%2020211010134749.png)

![](attachments/Pasted%20image%2020211010132302.png)
![](attachments/Pasted%20image%2020211010133009.png)
6 is total lompatan antara -3 sampai 3
![](attachments/Pasted%20image%2020211010135518.png)
discrete value = 0.235284

- Using decimal values of x and y as inputs in the mathematical functuon, the GA calculate the fitness of each chromosome.
- To find the maximum of the peak function, we will use crossover with probability equal to 0.7 and mutation with the probability equal to 0.001.
- Common practice in GA is to specify the number of generations are 100, the GA will create 100 generations of 6 chromosomes (population) before stopping.

![](attachments/Pasted%20image%2020211010144053.png)
optimum value = red
local optimum = the second highest peak (it may be trapped there without mutation)

First generation, the values move to local optimum.
![](attachments/Pasted%20image%2020211010144223.png)

Trapped in local optimum
![](attachments/Pasted%20image%2020211010144332.png)

After more generations (application of mutation), it reaches the global maximum.
![](attachments/Pasted%20image%2020211010144434.png)

**Graph**
Local maximum
![](attachments/Pasted%20image%2020211010144451.png)

Result (global maximum)
![](attachments/Pasted%20image%2020211010144520.png)

**How about using 60 chromosomes?**
Higher computation, but easier to escape local maximum.
![](attachments/Pasted%20image%2020211010144559.png)


## Case Study: Maintenance Scheduling
- Maintenance scheduling problems are usually solved using a combination of search techniques and heuristics. These problems are complex and difficult to solve.
- They are NP-complete and cannot be solved by combinatorial search techniques.
- Scheduling involves competition for limited resources and is comlicated by a great number of badly formalized constraint.


Steps
- Specify the problems, define constraints and optimum criteria
- Represent the problem domain as a chromosome
- Define a fitness function to evaluate the chromosome performance.
- Construct the genetic operators
- Run the GA and tune its parameters.

Problem constraints:
- The maximum loads expected during four intervals are 80, 90, 65 m and 70 MW
- Maintenance of any units starts at the beginning of an interfal and finishes at the end of the same or adjacent interval. The maintenance cannot be aborted or finished earlier than scheduled.
- The net reserve of the poer system must be greater or equal  to zero at any interval.

Optimum criterion is the maximum of the net reserve at any maintenance period.
![](attachments/Pasted%20image%2020211010150445.png)

![](attachments/Pasted%20image%2020211010150510.png)

![](attachments/Pasted%20image%2020211010153725.png)

![](attachments/Pasted%20image%2020211010153738.png)

![](attachments/Pasted%20image%2020211010153752.png)

![](attachments/Pasted%20image%2020211010153807.png)

![](attachments/Pasted%20image%2020211010153823.png)

![](attachments/Pasted%20image%2020211010153836.png)
