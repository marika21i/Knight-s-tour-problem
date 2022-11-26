#KNIGHT'S TOUR PROBLEM

The solution consist of finding a sequence of knight's moves on the chessboard such that the knight, given the starting position which can be any cell, visits every square on the board exactly once. The allowed moves are the ones which follow the Knight's rules of chess game.

The problem can involve chessboards of different size, also rectangular ones, but in our project we will only deal with squared boards and we decided to put the size $n$ as an attribute of the class. A theorem, proved by Cull and Conrad, guarantees us the existence of a solution for $n\ge 5$.

One way to find an open knight's tour is the heuristic method which follows **Warnsdorff's rule**. It suggests to choose the next position at each step, among the free ones, in such a way that the knight has the lowest number of available moves from that cell at the next step.
It follows that he visits the squares around the edges of the board first. This ensures that the knight will visit the hard-to-reach corners early and can use the middle squares to hop across the board only when it is necessary.
We decided to implement Warnsdorff's solution in two different ways:
*  using lists
*  using graphs.

Another way to solve the problem is through **Backtracking** and again we decided to implement the solution using both lists and graphs. Backtracking is an algorithmic paradigm that tries different solutions until a solution that *does the job* is found. Each step of the algorithm can be described as follows:
* starting from any cell, choose a move from all the available moves;
* check if this move will lead us to the solution or not: if not, we choose a different move. 
