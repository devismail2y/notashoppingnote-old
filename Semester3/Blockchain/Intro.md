Hash function, can be any size but reasonable to compute.

For the security
- Collision resistance
- Hiding = Hide the real data
- Puzzle friendliness

Collision do exist $2^130$ randomly chosen inputs, 99.8% chance that two of them will collide. This works no matter what H is, but it takes too long and too much to matter (not feasible).

## Commitment API
(com, key) := commit(msg)  
match := verify(com, key, msg)  

**To seal msg in envelope**  
(com, key) := commit(msg) -- then publish  

**To open envelope**  
publish key, msg  
anyone can use verify() to check validity  

**Security properties**  
Hiding: Given com, infeasible to find msg  
Binding: infeasible to find msg != msg' such that  
	verify(commit(msg), msg') == true  


## Puzzle Friendly
(for mining) for every possible output value y, if k is chosen from a distribution with high non-entropy.

Blockchain tidak pasti desentralisasi. Namun, desentralisasi adalah validator dari blockchain (berdasarkan konsensus).
