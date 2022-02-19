# Rule Based Expert System

## Intro
**Knowledge** theoritical or practical understanding of subject or a domain.


Most experts are capable of expressing their knowledge in the form of rules of problem solving. i.e. 

IF the 'traffic light' is green 
THEN go

IF the 'traffic light' is red
THEN stop

**Rule** can be defined as multiple IF-THEN structure that relates given information or facts.
- IF part = antecedent (premise or condition)
- THEN part = consequent (conclusion or action)
The rule can have multiple antecendents and joined by AND or OR.

Rules can represent relations, recommendation, directive, and heuristics
- Relation
```
IF 		the 'fuel tank' is empty
THEN 	the car is dead
```

- Recommendation
```
IF		the season is autumn
AND		the sky is cloudy
AND		the forecast is drizzle
THEN	the advice is 'take an umberella'
```

- Directive
```
IF 		the car is dead
AND		the 'fuel tank' is empty
THEN	the action is 'refuel the car'
```
you can distinct between directive and recommendation by looking the antecedent part. The directive is more mandatory than the recommendation.

- Strategy
```
IF		the car is dead
THEN	the action is 'check the fuel tank';
		step1 is complete
		
IF		step1 is complete
AND		the 'fuel tank' is full
THEN	the action is 'check the battery';
		step2 is complete
```

- Heuristic
```
IF		the spill is liquid
AND		the 'spill pH' < 6
AND		the 'spill smell' is vinegar
THEN	the 'spill material' is 'acetic acid'
```

## Players in the Development Team
![](attachments/Pasted%20image%2020210920084601.png)
1. **Domain expert** someone that has deep knowledge in certain domain.
2. **Knowledge engineer** designing, building, and testing expert system. He then chooses some development software/programming language
3. **Programmer** to program and describe the domain knowledge in terms that a computer can understand.
4. **Project manager** leader of the expert system development team.
5. **End-user** the user

## Structure
![](attachments/Pasted%20image%2020210920085418.png)
1. Production rules stored in long-term memory.
2. Problem-specific information or facts stored in short-term memory.
3. Reasoning/inference
![](attachments/Pasted%20image%2020210920085541.png)

The expert system is similar to human's decision making process

**Knowledge base** contains knowledge useful for problem solving. In rule-based expert system, the knowledge is represented as a set of rules. 

**Database** set of facts used to match against the IF parts of rules stored in the knowledge base.

**Inference engine** carries out the reasoning whereby the expert system reaches a solution.

**Explanation facilities** enable the user to ask the expert system how a particular conclusion is reached and why specific fact is needed.

**User interface** communication between a suer seeking a solution to the problem and an expert system.

![](attachments/Pasted%20image%2020210920090050.png)

## Forward Chaining and Backward Chaining
Inference chain
![](attachments/Pasted%20image%2020210920121143.png)

**Forward chaining** data-driven reasoning. The reasoning starts from the known data and proceeds forward with that data. 
- Each time only the topmost rule is executed. 
- When fired, the rule adds a new facts in the database. 
- Any rule can be executed only once. 
- The match-fire cycle stops when no further rules can be fired.

![](attachments/Pasted%20image%2020210920121501.png)

About forward chaining:
- Forward chaining is a technique for gathering information and then inferring from it whatever can be inferred.
- However, in forward chaining, many rules may be executed that have nothing to do with the established goal.
- Therefore, if our goal is to infer only one particular fact, the forward chaining inference technique would not be efficient.

**Backward chaining** goal-driven reasoning. Inbackward chaining, an expert system has the goal (a hypothetical solution) and the inference engine attempts to find the evidence to prove it.
- The knowledge base is searched to find rules that might have the desired solution.
- Such rules must have the goal in their THEN action parts.
- If such a rule is found and its IF condition part matches data in the database, then the rule is fired and the goal is proved.
- However this is rarely the case.

![](attachments/Pasted%20image%2020210920122404.png)

How do we choose between forward and backward chaining?
- If an expert first needs to gather some information and then tries to infer from it whatever can be inferred, choose the forward chaining inference engine.
- However, if your expert begins with a hypothetical solution, and then attempts to find facts to prove it, choose the backward chaining inference engine.

## Conflict Resolution
Rule 1
```
IF		the 'traffic light' is green
THEN	the action is go
```

Rule 2
```
IF 		the 'traffic light' is red
THEN	the action is stop
```

Rule 3
```
IF		the 'traffic light' is red
THEN	the action is go
```

There is no right and wrong in expert system, Methods used for conflict resolution: 
- Highest priority number. Usually works well for expert systems with around 100 rules/
- Most specific rule (longest matching strategy, highest number of parent rule). Based on assumption, specific rules process more information than a general one.
- Most  recently entered. This method relies on timestamp attached to each fact in the database.

## Metaknowledge
Knowledge about the use and control of domain knowledge in an expert system. In rule-based expert systems, metaknowledge is represented by metarules.

**Metarule** determines a strategy for the use of task-specific rules in the expert system. Example
1. Rules supplied by experts have higher priorities than rules supplied by novices.
2. Rules governing the rescue oi human lives have higher priorities than rules concerned with clearing overloads on power system equipment.

## Advantages of Rule-Based Expert Systems
- Natural knowledge representation, problem solving technique based on procedure that is created by human expert.
- Uniform structure (IF-THEN structure), it enables to self-document
- Knowledge is separated from process, possible to develop different applications using the same expert system shell.
- Dealing with incomplete and uncertain knowledge., it includes reason.

## Disadvantage of Rule-based Expert Systems
- Opaque relations between rules, difficult to observe how individual rules serve the overall strategy.
- Ineffective search strategy, can be slow and unsuitable for real-time applications.
- Inability to learn, unlike human expert, who knows when to "break the rules",





