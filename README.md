# Knight-Min_Steps

Problem Statement:
Given a square chessboard of N x N size, the position of Knight and position of a target is given.  We need to find out the minimum steps a Knight will take to reach the target position.
 
 
Examples: 
In above diagram Knight takes 3 step to reach 
from (4, 5) to (1, 1) 
(4, 5) -> (5, 3) -> (3, 2) -> (1, 1) 


Approach:
This problem is similar to finding the shortest path in an unweighted graph. As a result, we employ BFS to overcome this issue. 
We try all 8 spots a Knight can reach from its current position. 
If a reachable position hasn't been visited yet and is located within the board, we add it to the queue with a distance of one more than its parent state. 
Finally, when the target position is popped out of the queue, we return its distance.
The code below uses BFS to search across cells, where each cell has its own coordinate and distance from the starting node. 
In the worst-case scenario, the code below accesses all of the board's cells, resulting in an O(N^2) time complexity.
