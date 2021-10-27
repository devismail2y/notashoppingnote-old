# CLIPS Programming Tool

- It is a forward chaining system: starting from the facts, a solution is developed
- Its inference engine internally uses the Rete Algorithm for pattern-matching: find fitting rules and facts.

![](attachments/Pasted%20image%2020211011065228.png)

## Components
- **Fact base**, fact list that represents the initial state of the problem. This is the data from which inferences are derived.
- **Rule base**, knowledge base (KB) contains a set or rules which can transform the problem state into a solution.
- **Inference engine**, controls overall execution. It matches the facts against the rules to see what rules are applicable using recognize-act cycle:
	- match the facts against the rules
	- choose which rules instantiation to fire
	- execute the actions associated with the winning rule

## Basic Commands
To launch these command, place inside a parenthesis.
i.e. (exit), (run), etc
```clips
exit - exit from clips
clear - clear environments from facts, rules
reset - set fact base to its initial state (perform it before each program run)
run - executes a program currently loaded into the CLIPS interpreter against currently defined rule-bases and fact-bases

load "filename.clp" - load a CLIPS proram into the interpreter, also does syntax check and makes constructs
facts - display fact base
rules - display rule base
agenda - display all potential matches of active facts for all rules
```

![](attachments/Pasted%20image%2020211011072510.png)

## Data Types
![](attachments/Pasted%20image%2020211011072540.png)

## Comments
![](attachments/Pasted%20image%2020211011072612.png)
![](attachments/Pasted%20image%2020211011072629.png)

## Examples
![](attachments/Pasted%20image%2020211011075809.png)
![](attachments/Pasted%20image%2020211011075747.png)

## Fields
![](attachments/Pasted%20image%2020211011081752.png)
![](attachments/Pasted%20image%2020211011081812.png)
![](attachments/Pasted%20image%2020211011081905.png)
![](attachments/Pasted%20image%2020211011081922.png)

## Facts
![](attachments/Pasted%20image%2020211011082330.png)
command:
``` clips
assert - (assert (emergency fire))
list - (facts)
retract - (retract 0)

in the file
define group of facts - deffeacts

(deffacts Expert Systems "Class List"
 (person (name "Mike") (age 18))
 (person (name "John") (age 20))
)
```
 By default, identical facts are not allowed by using (asert)
 Identical facts can be defined in deffacts, but only one of them is put on working memory.
 
 To allow duplicate fact, you can use (set-fact-duplication TRUE) in the terminal
 
 Load and save facts from separate file
 ![](attachments/Pasted%20image%2020211011083718.png)
 
 