**Artificial Intelligence – Assessment 3**

**Title**

**Implementation of A Search and Minimax with Alpha-Beta Pruning for Intelligent Problem Solving and Decision Making***

**Objective**

To study and implement advanced Artificial Intelligence search and decision-making algorithms such as A* Search Algorithm and Minimax Algorithm with Alpha-Beta Pruning using Python programming. The objective is to analyze optimal path finding, heuristic-based searching, and intelligent decision-making techniques used in real-world AI applications.

**Software Used**

Python 3.13

**Tools Used**

Python IDLE

**AI Techniques / Algorithms Used**
A* Search Algorithm
Heuristic Search
Cost Function Evaluation
Open List and Closed List Management
Minimax Algorithm
Alpha-Beta Pruning
Game Tree Search
Intelligent Decision Making
Problems Implemented

**1. Optimal Path Finding using A Search Algorithm***

Implemented A* Search Algorithm to find the shortest path between a starting node and a goal node in a weighted graph. The algorithm uses heuristic values and path costs to calculate the best route using:

f(n)=g(n)+h(n)

where:

g(n) represents the actual cost from the start node.
h(n) represents the estimated cost to reach the goal.
f(n) represents the total estimated cost.

The algorithm maintains Open List and Closed List to select the most efficient path.

**Optimal Path Obtained:**

A → B → E → D → G

**Total Path Cost**:

8

**2. Strategic Game Decision Making using Minimax with Alpha-Beta Pruning**

Implemented Minimax Algorithm with Alpha-Beta Pruning to determine the best possible move in a game tree.

**The algorithm evaluates:**

MAX player decisions.
MIN player decisions.
Alpha (α) value.
Beta (β) value.

Alpha-Beta Pruning removes unnecessary branches to reduce computation time while maintaining the correct decision.

**Final Minimax Value**:

3

**Best Move:**

Left MIN Branch

**Pruned Node:**

Node 2

**Result**

The Artificial Intelligence algorithms were successfully implemented and tested using Python. The A* Search Algorithm successfully found the optimal path by evaluating heuristic and path costs, while the Minimax Algorithm with Alpha-Beta Pruning successfully performed intelligent decision-making by analyzing game states and reducing unnecessary searches.
The implementation improved the understanding of heuristic search, optimal path planning, game tree evaluation, and AI-based problem-solving techniques.
