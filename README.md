# Lab 3: n-Puzzle

Solve the sliding tile puzzle, also known as n-puzzle.

## A star search

This search method ensures a optimal solution by using a combination of the actual cost to reach a node (g) and the estimated, heuristic, cost to the goal (h).

## Greedy Best First

This search method is used to quickly find a solution by always exploring the node heuristically closest to the goal.

## Heuristics

All the used algorithms are informed, so they need an admissible heuristic.
Three heuristics have been considered:

- Number of misplaced tiles (hamming distance)
- Total manhattan distance
- Total manhattan distance with linear conflict penalty

The more complex, but the more stringent, is the last one.
To obtain it we compute the manhattan distance of each tile from its goal (excluding the blank tile) and then we add a penalty for each conflict in row or columns (two tiles have the goal in the same line but now they are swapped).

N.B: the more stringent the heuristic the faster the convergence of the algorithms.

## Results

The path is returned as a sequence of states.

The optimal path can be found for N=2,3.

An approximatated path can be computed for N up to 7.
