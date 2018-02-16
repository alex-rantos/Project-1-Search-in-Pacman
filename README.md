Project : http://ai.berkeley.edu/search.html

#### Provisional grades
------------------

Question q1: 3/3

Question q2: 3/3

Question q3: 3/3

Question q4: 3/3

Question q5: 3/3

Question q6: 3/3

Question q7: 2/4

Question q8: 3/3

------------------
Total: 23/25

### BFS,DFS,UCS,A*
The above algorithms are implemented so they pass the autograder.py.

So the idea is to check the node if has been visited before.Then you push it to
visited list and check if we reached goalState - if not expand children based on algorithm.

**Code is fully explained in comments.**


### Problem 5
I changed my first-implementation of BFS to the one I used for ucs/a* so I can calculate the
number of corners I have visited.

### Problem 6
In this problem the function of manhattanDistance() from util.py has been used.
First @cornersHeuristic we check which corners are left to visit and then we calculate
the currentpoint to each corner respectively - all written efficiently and cleanly in a 
single line of code :: 
*min([(util.manhattanDistance(curPoint, corner), corner) for corner in cornersLeftToVisit])*

### Problem 7
There are 2 implementations.

First one is an oneliner that gets 2/4 on autograder and returns the length of the foodGrid.In that way
each food-node gets an additional cost of how many foods are left. *12517 nodes in ~9sec*

Second and faster implementation uses manhattanDistance to calculate the distance between each food
and pacman distance.(This one fails autograder.py) *6126 nodes in 3sec*
### Problem 8
Worked as problem 6.There is no difference between bfs,ucs,astar as far as path cost is concerned.
######NOTE : The old DFS gave a path cost of 514 but the new one that passes the autograder gives a very expensive path of 5324 cost. 



