# Trains a Machine Learning Model
Inductive inferring with ideal y value of 44.1. Let's take looks for value of x1:x6 that gives the most identical value to 44.1.

![](attachments/Pasted%20image%2020211010154247.png)

Solution 1
![](attachments/Pasted%20image%2020211010154303.png)

Solution 2
![](attachments/Pasted%20image%2020211010154319.png)

Solution 3
![](attachments/Pasted%20image%2020211010154336.png)

Difficulty
![](attachments/Pasted%20image%2020211010154353.png)

## Genetic Algorithm for Optimization
Genes
![](attachments/Pasted%20image%2020211010154741.png)

Define the population size
![](attachments/Pasted%20image%2020211010154808.png)

Fitness value (the lower error, the higher fitness value)
![](attachments/Pasted%20image%2020211010154925.png)

Calculating initial value
![](attachments/Pasted%20image%2020211010154945.png)
![](attachments/Pasted%20image%2020211010155003.png)
and so on

Select 3 best individuals as parents for mating to generate new individuals.
![](attachments/Pasted%20image%2020210913131734.png)

**Crossover**
![](attachments/Pasted%20image%2020210913131816.png)


**Mutation**, you can choose which gene/genes got the mutation. In this example we define 5th gene of the children will get mutated by dividing by 2.
![](attachments/Pasted%20image%2020210913131851.png)


Parents (old individuals) and children (new individuals)
![](attachments/Pasted%20image%2020211010170000.png)

**Generation 1**
![](attachments/Pasted%20image%2020210913132228.png)

Do the same thing to create generation 2
![](attachments/Pasted%20image%2020211010170052.png)
![](attachments/Pasted%20image%2020211010170031.png)

**Generation 2**
![](attachments/Pasted%20image%2020210913132658.png)

So, if you want to get the best result, you run the algorithm again and again.
It still use decimal number not binary number.
It is challenging to use Genetic Algorithm for real time application.

If the value is still not satisfy you enough, rerun the process, create another crossover, i.e. chromosome number 5 to chromosome number 3, etc. 

