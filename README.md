## Compiler Construction Assignment - 1
### Problem Statement : 
(Refer to ```Assignment-1.pdf``` and ```q2.pdf```)
1. Program that takes a parenthesized regular expression r and a string w as an input and output the sequences of valid tokens, as per LEX tool i.e by finding
the longest matching prefix of the string.
2. Given n regular expressions r1, r2, . . . , rn and a string w, the LEX tool finds the longest prefix w1 (say w1 as a valid token) of the input w that can be generated by a regular expression
(RE) in {r1, r2, . . . , rn}. If the longest prefix w1 can be generated by more than one regular expression, consider that it is generated by the lower indexed regular expression among the REs
that can generate w1.


#### Base Functions : 
1. Concatenation of two NFA's : </br> 
Epsilon transitions added from final states of NFA1 to start state of NFA2 and a dummy start state created with epsilon transitions to start state of NFA1 </br>
![graph](https://user-images.githubusercontent.com/98446038/229279251-e3c0dbb6-d642-430f-8573-f287d424149d.png)
2. Star Operator : </br>
Start state is made the final state and epsilon transitions from final to start </br>
![graph (2)](https://user-images.githubusercontent.com/98446038/229279432-21478f50-2344-4e1d-a985-42308cce52eb.png)
3. Plus Operator : </br>
Epsilon transitions from final to start state </br>
![graph (1)](https://user-images.githubusercontent.com/98446038/229279455-c54f13ce-e680-4c1d-92ed-c43efbd34ef7.png)
4. Or Operator : </br>
Dummy start state with epsilon transitions to start state of NFA1 and NFA2 and epsilon transitions from final state of both NFA to a dummy final state </br>
![graph (3)](https://user-images.githubusercontent.com/98446038/229279481-f8d81ba1-df6a-41a4-9151-52572f9cf132.png)
