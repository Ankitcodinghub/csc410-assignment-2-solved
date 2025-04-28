# csc410-assignment-2-solved
**TO GET THIS SOLUTION VISIT:** [CSC410 Assignment 2 Solved](https://www.ankitcodinghub.com/product/csc410-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;120301&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSC410 Assignment 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Assignment 2• This is a group assignment, designed for groups of 3 students. From this point on in the semester, you are permitted to work in groups of 2 if you wish. You cannot submit individually.

• Each group should submit three files named q1.py, q2.py and q3.py. Note that Markus has been setup to accept exactly those 3 files. All the necessary helper functions should be included in each file for each problem. You should not change any of the names or signatures of the functions already provided in the files, and you are not allowed to import any other package than the ones already imported.

• Your problems (1) and (3) encodings can only use boolean variables. You should not solve the problems algorithmically, which means that the solution of the problem can always be deduced only from the solution given by the solver.

Note that your assignment will be automatically graded. Your functions will be called from another script. If you mess with the signature, the call will fail and the autograder will give you a 0 mark.

Instructions about Z3 and Python

• You have to use the Python API of Z3 to produce the encoding and call the solver. All functions necessary to complete the assignment have been presented in Tutorial 2.

• You are not allowed to import any other package than the ones already imported in your python files.

• For problems (1) and (3), you should only use Bool literals in the encoding. More precisely, you can use any variable type in your Python program, but you should only pass variables created via Bool() to the solver. This means that you will be using Z3 as a SAT-solver and not in its more expressive capacity as an SMT solver. For problem (2), on the other hand, you should provide a different SMT encoding.

Word of Advice

The goal of this assignment is to use constraint solvers to solve problems. The interface to the solver is minimal and you will need to use only a few functions. The difficulty is not in using the solver, in the sense that you need to know how to do fancy things with it. The main effort goes into devising a correct encoding of each problem in SAT or SMT.

Problem 1 (30 points)

In this problem, you will experiment with giving two different encodings to the same problem, and comparing their performance. The learning objective is to gain an understanding that there are many ways to encode a problem as a constraint solving problem, and some are better than others.

The At-most-k constraint on n (n &gt; k) variables (X1,…,Xn) is noted ≤k (X1,…,Xn) and satisfied iff at most k of the X1,…,Xn variables are true.

Naive encoding Devise a simple encoding for the At-most-k constraint, and implement it in the naive(literals, k) function.

• The function should return all the clauses of the encoding that ensures at most k literals in the list literals can be true.

• You are not allowed to create any new variables for the encoding in this function.

Encoding using a sequential counter Sinz [?] introduced an encoding for the At-most-k constraint by encoding a sequential counter that counts the number of Xi that are true. For more details on why this encoding works, you can read the original paper, but this is not required for the assignment.

To encode ≤k (X1,…,Xn), this encoding introduces (n−1)∗k new variables {Ri,j |1 ≤ i &lt; n,1 ≤ j ≤ k}.

Below is the conjunctive normal form of the encoding:

¬X1 ∨R11

Vkj=2 ¬R1,j

Vin=2−1 ((¬Xi ∨Ri,1)∧(¬Ri−1,1 ∨Ri,1))

Vni=2−1 Vkj=2(¬Xi ∨¬Ri−1,j−1 ∨Ri,j)∧(¬Ri−1,j ∨Ri,j)

Vni=2−1(¬Xi ∨¬Ri−1,k)

∧(¬Xn ∨¬Rn−1,k)

1. Implement this encoding in the sequential_counter(literals,k) function in q1.py. The function should return all the clauses of the encoding that ensure at most k literals in the list literals are true.

2. Compare the performance of the two encodings and write a short paragraph in the comments in q1.py to explain which encoding performs better depending on n and k, if there is one.

To help you, a small test function has been implemented in q1.py. You can execute the script q1.py with three arguments: E is 0 to use your encoding, 1 to use the sequential encoding. N is the number of variables and K is the number of variables that have to be set to true (0 &lt; K &lt; N).

python q1.py E N K

If your encoding is correct, the response should be PASSED in (-)s, where the “- ” will be replaced with the running time (in seconds) of the solver to solve the encoded constraints.

Note that the test function encodes the constraint ensuring exactly k variables are true, not the weaker constraint at-most-k. To do so, it calls your implementation of at-most-k twice, with different arguments.

Note that the goal of the test function is to encode the constraint that exactly k variables are true. It achieves this by reducing the goal to a combination of results from two calls to your implementation of at-most-k.

Problem 2 (30 points)

https://en.wikipedia.org/wiki/Hidato

Input format The partially completed grid is provided to you with – standing for each blank cell to be filled with a number, and * for blocked cells (that are not to be filled with a number). Each symbol two symbols is separated by a single space. Each line of the puzzle is written in a separate line of the input file. For example, the input file:

* * 7 6 – * *

* * 5 – – * *

31 – – 4 – – 18

– 33 2 12 15 19 –

29 28 1 14 – – –

* * – 24 22 * *

* * 25 – – * *

Has the following solution, represented in the same format:

* * 7 6 9 * *

* * 5 8 10 * *

31 32 3 4 11 16 18

30 33 2 12 15 19 17

29 28 1 14 13 21 20

* * 27 24 22 * *

* * 25 26 23 * *

The function parsing the input grid is provided in q2.py.

Task

Given a partially completed grid, is it possible to complete the grid obeying the rules of Hidato?

If the answer is no, then simply output None. If the answer is yes, then you need to output the completed grid.

You are not allowed to use more variables for z3 (using Int() or Bool()) than there are cells on the grid.

Problem 3 (40 points)

The goal of this problem is to solve Hidato again, but this time without the power of SMT. For this instance, we want to limit ourselves to a SAT solver only. The encoding will naturally be less high level and less intuitive in this case.

The specification of the output is precisely the same as stated in Problem 2, but you will complete the function solve(grid) in q3.py this time which only permits you to use Boolean variables.

Problem 2 vs Problem 3

You are asked to redo the same problem in two different encodings, precisely so that you get a sense how different the solutions (encodings) can be. The constraints put in place in each case are there to make sure that you do not recycle an idea from one solution to the other, but rather rethink and resolve the problem given the context.

In class, we discussed how a computation model can be built around a SAT/SMT oracle. In both instances of Hidato, your wrapper code should have polynomial time complexity on the input size to produce the encoding (which itself should also be polynomial on the input size). Considering that Hidato is known to be NP-Complete, this effectively forces you to use the solver properly since any algorithmic solution to Hidato without the SAT/SMT oracle must have super-polynomial complexity.
