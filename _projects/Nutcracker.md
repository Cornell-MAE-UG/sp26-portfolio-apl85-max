Problem Statement: 
Find the necissary dimensions of a nutcracker when the nutcracker is about to crack. 

Constraints and Input parameters: 
From the literature provided in the assignment, the average load required to crack a nut is 222.18 kg. 
The average grip stregnth for a man is 50 kg and a woman 30 kg so the average value of 40 kg will be applied here. 
The size of a nut is between 1 and 3 cm so 2 cm is a good approximation. 

Problem Approach 
In order to implement finding the design parameters needed, a free body diagram will first be constructred. 
A moment balence will be completed at a chosen origin of analysis then the ratio of legnths and height will be determined to get the final values.

Using the joint as the origin, 

$\sum \mathbf{M} = \mathbf{l}_1 \times \mathbf{F}_i - \mathbf{l}_2 \times \mathbf{F}_n = 0$

(assume static equilibrium) 

$$
\frac{|\mathbf{l}_1|}{|\mathbf{l}_2|} = \frac{|\mathbf{F}_n|}{|\mathbf{F}_i|}
$$
= 228.18 kg/40 kg = 5.55

This is the cooresponding similar triangle ration

H1 = 5.55H2
H1 = 5.55(2 cm) 
H1 = 11.11 cm

Since the nut is 2 cm, let the legnth l2 be 4cm so l1 is 4 cm (5.55) = 22.22 cm


Diagram: ![Image of Nutcracker FBD](/assets/images/NutFBD.png)


Discussion: 
The nutcracker will therefore be 11 cm tall and 22 cm long in the open position. This system is HUGE and would be hard for the user to be able to use. 
Therefore future disucssion would likeley require smaller parameters in order to create an effective nutcracker. 
