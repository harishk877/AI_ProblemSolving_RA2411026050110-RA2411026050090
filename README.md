# AI Problem Solving — GitHub Submission

> **Course:** Artificial Intelligence  
> **Problems Implemented:** Problem 1 (Tic-Tac-Toe AI) & Problem 8 (Smart Navigation System)  
> **Language:** HTML / JavaScript (runs entirely in browser — no install needed)

---

## 📁 Repository Structure

```
AI_ProblemSolving_<RegisterNumber>/
│
├── Problem1_TicTacToe/
│   └── problem1_tictactoe.html
│
├── Problem8_Navigation/
│   └── problem8_navigation.html
│
└── README.md
```

---

## Problem 1 — Interactive Game AI (Tic-Tac-Toe)

### Description
A web-based Tic-Tac-Toe game where the AI always plays optimally. Two algorithms are implemented and compared live: **Minimax** and **Alpha-Beta Pruning**.

### Algorithms Used

#### Minimax Algorithm
- The AI explores **all possible future game states** recursively.
- Assigns +10 to winning positions, -10 to losing positions, and 0 to draws.
- Always picks the move with the **maximum score**.
- Explores **every** node in the game tree — no pruning.

#### Alpha-Beta Pruning
- An **optimisation of Minimax** that skips branches that cannot affect the final decision.
- Maintains two values: `alpha` (best for maximiser) and `beta` (best for minimiser).
- If `beta ≤ alpha`, the branch is **pruned** (skipped).
- Produces the **same result** as Minimax but explores far fewer nodes.

### Comparison

| Metric | Minimax | Alpha-Beta |
|---|---|---|
| Nodes Explored | More (all states) | Fewer (pruned) |
| Execution Time | Slower | Faster |
| Result Quality | Optimal | Optimal (same) |
| Best Case Reduction | — | Up to 50% fewer nodes |

### How to Run
1. Open `problem1_tictactoe.html` in any modern web browser.
2. Select **Minimax** or **Alpha-Beta** algorithm from the top controls.
3. Choose whether you want to play as **X** or **O**.
4. Click cells to make your move. The AI responds instantly.
5. After each AI move, the **Algorithm Comparison panel** updates showing nodes explored and time taken for **both** algorithms side-by-side.

### Sample Output
```
You play:  X at row 2, col 2
AI (Minimax)  → nodes: 255, time: 0.41ms
AI (Alpha-Beta) → nodes: 87,  time: 0.12ms
Result: Draw (optimal play)
```

---

## Problem 8 — Smart Navigation System (BFS & DFS)

### Description
An interactive graph-based navigation system. Users can build custom graphs by adding nodes and edges, or load preset graphs (City, Tree, Grid). The system finds a path from a start node to a goal node using both **BFS** and **DFS**, then compares the results.

### Algorithms Used

#### Breadth-First Search (BFS)
- Uses a **queue** (FIFO) to explore nodes level by level.
- Visits all neighbours of a node before going deeper.
- **Guarantees the shortest path** in an unweighted graph.
- May explore more nodes when the goal is deep in the graph.

```
Algorithm:
1. Enqueue start node, mark visited
2. While queue not empty:
   a. Dequeue node
   b. If node == goal → return path
   c. Enqueue all unvisited neighbours
```

#### Depth-First Search (DFS)
- Uses **recursion** (implicit stack) to explore one path as deep as possible before backtracking.
- **Does NOT guarantee shortest path**.
- Can be faster when the goal is on the first explored branch.
- Uses less memory than BFS in wide graphs.

```
Algorithm:
1. Mark current node visited
2. If current == goal → return path
3. For each unvisited neighbour:
   a. Recurse into neighbour
   b. If path found → return it
4. Backtrack
```

### Comparison

| Metric | BFS | DFS |
|---|---|---|
| Path Optimality | ✅ Shortest path | ❌ Not guaranteed |
| Memory Usage | Higher (stores all levels) | Lower (one path at a time) |
| Best For | Shortest path problems | Maze solving, deep graphs |
| Time Complexity | O(V + E) | O(V + E) |

### How to Run
1. Open `problem8_navigation.html` in any modern web browser.
2. **Option A — Load Preset:** Click one of the sample graph buttons (City Network, Binary Tree, Grid Graph).
3. **Option B — Build Custom Graph:**
   - Type a letter (e.g. `A`) and click **+ Node**
   - Type an edge (e.g. `A-B`) and click **+ Edge**
4. Set **Start Node** and **Goal Node** in the input fields.
5. Click **▶ Run Search**.
6. The canvas highlights the BFS path (teal) and DFS path (orange).
7. Use **BFS Path / DFS Path / Show All** toolbar buttons to toggle views.
8. The comparison panel at the bottom explains the difference in results.

### Sample Output
```
Graph: City Network (A → E)

BFS Result:
  Path: A → B → H → E
  Path Length: 3 edges
  Nodes Explored: 6
  Shortest path: YES

DFS Result:
  Path: A → G → H → E
  Path Length: 3 edges
  Nodes Explored: 4
  Shortest path: NOT GUARANTEED
```

---

## Execution Steps (Both Problems)

```bash
# No installation required — pure HTML/JS
# Just open the file in a browser:

# Windows
start problem1_tictactoe.html
start problem8_navigation.html

# Mac
open problem1_tictactoe.html
open problem8_navigation.html

# Linux
xdg-open problem1_tictactoe.html
xdg-open problem8_navigation.html
```

Or simply **double-click** the `.html` file.

---

## Technologies Used
- HTML5 / CSS3
- Vanilla JavaScript (ES6+)
- HTML5 Canvas API (for graph rendering)
- Google Fonts (Orbitron, Space Mono, Syne)

---

## Team Members

| Name | Register Number |
|------|----------------|
| Member 1 | `<Register Number>` |
| Member 2 | `<Register Number>` |

---

*Submitted for AI Problem Solving Assignment — Deadline: 26th April 2026*
