# Content
1.  [What is Searching?](#what-is-searching)
2. [Uninformed Search](#uninformed-search)
3. [Informed Search](#informed-search)

---
# What is Searching?

In AI, searching means finding a sequence of steps or actions to reach a goal from a starting point.

An AI system searches through different possible solutions to find the best or correct one.

In AI searching is used when:

- The solution is not directly known
- AI must explore possibilities

The AI checks different states and paths until it finds the goal.

### Why searching is important
Searching is the core of many AI systems because AI often needs to:

- Make decisions
- Find optimal solutions
- Plan actions

Without searching, many intelligent behaviors are impossible.


### Real-world examples
| Application      | What AI searches for |
| ---------------- | -------------------- |
| Google Maps      | Best route           |
| Chess AI         | Best move            |
| Robot navigation | Safe path            |
| Puzzle solving   | Correct solution     |

### Types of search in AI

1. **Uninformed Search**

    AI has no extra knowledge.

    Examples:

    - BFS (Breadth First Search)
    - DFS (Depth First Search)
2. **Informed Search**

    AI uses hints or heuristics.

    Example:

    - A* Algorithm

    Used for faster and smarter searching.




[Go To Top](#content)

---
# Uninformed Search
Uninformed Search (also called Blind Search) is a search technique in AI where the algorithm has no extra knowledge about which path is better.

It only knows:

- Initial state
- Goal state
- Possible actions

It does not know:

- Which direction is closer to the goal
- Which path is optimal beforehand

### Why called “uninformed”?

Because the algorithm has:

- No guidance   
- No estimate of goal distance
- No intelligence about better paths

It simply searches mechanically.

### Main types of uninformed search
| Algorithm                  | Working                            |
| -------------------------- | ---------------------------------- |
| Breadth First Search (BFS) | Explores level by level            |
| Depth First Search (DFS)   | Goes deep first                    |
| Uniform Cost Search        | Chooses lowest-cost path           |
| Depth Limited Search       | DFS with depth limit               |
| Iterative Deepening DFS    | Repeated DFS with increasing depth |

### 1. Breadth First Search (BFS)
Explores all nearby nodes first.

Example:
```
A
├── B
├── C
└── D
```
BFS checks:

- B, C, D first
- Then deeper levels

**Advantage**\
Finds shortest path (if costs are equal)

**Disadvantage**\
Uses lots of memory

### 2. Depth First Search (DFS)
Goes as deep as possible before backtracking.

Example path:
```
A → B → E → H
```

**Advantage**\
Less memory usage

**Disadvantage**\
May get stuck in deep wrong paths

### Difference between BFS and DFS
| Feature        | BFS        | DFS            |
| -------------- | ---------- | -------------- |
| Strategy       | Level-wise | Deep first     |
| Memory         | High       | Low            |
| Shortest path  | Yes        | Not guaranteed |
| Data structure | Queue      | Stack          |



[Go To Top](#content)

---
# Informed Search
Informed Search (also called Heuristic Search) is a search technique in AI where the algorithm uses extra knowledge or hints to find the goal faster.

Instead of searching blindly, it estimates: “Which path is more likely to reach the goal?”

### Heuristic Function

A heuristic is a rule or estimate that tells how close a state is to the goal.

Usually written as:

$$h(n)$$

Where:

- n = current node/state
- h(n) = estimated cost to reach goal

Lower heuristic value means:
- Closer to goal

### Characteristics

Informed search:
- Uses heuristics
- Faster than uninformed search
- Explores fewer nodes
- More efficient

But:
- Quality depends on heuristic accuracy

### Main types of informed search
| Algorithm                | Idea                         |
| ------------------------ | ---------------------------- |
| Greedy Best First Search | Chooses node closest to goal |
| A* Search                | Uses path cost + heuristic   |

### 1. Greedy Best First Search
Chooses the node with smallest heuristic value.

> Meaning: “Go where goal seems closest.”

**Problem**\
Can choose wrong shortcut sometimes.

### 2. A* Search
Most important informed search algorithm.

Uses:

$$f(n) = g(n) + h(n)$$

Where:

- g(n) = actual cost from start
- h(n) = estimated cost to goal
- f(n) = total estimated cost

[Go To Top](#content)

---