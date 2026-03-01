# Dynamic Pathfinding Agent

A real-time, grid-based pathfinding visualizer built with Python and Pygame. This project implements Informed Search Algorithms (A* and Greedy Best-First Search) capable of navigating dynamic environments where obstacles appear while the agent is in motion.

## 🚀 Features
* **Search Algorithms:** Toggle between **A* Search** ($f(n) = g(n) + h(n)$) and **Greedy Best-First Search** ($f(n) = h(n)$).
* **Heuristics:** Supports **Manhattan** and **Euclidean** distance calculations.
* **Dynamic Re-planning:** Real-time obstacle spawning and automated path recalculation if the current route is obstructed.
* **Interactive Editor:** Manually place/remove walls or generate a random maze with 30% obstacle density.
* **Real-Time Metrics:** Dashboard tracking Nodes Visited, Path Cost, and Execution Time (ms).

## 🛠️ Installation & Setup

### Prerequisites
* Python 3.8 or higher
* Anaconda (Optional, but recommended)

### Dependencies
Install the required library using pip:
Bash
pip install pygame

Navigate to the directory and run the main script:
Bash
python main.py
(Note: If using Jupyter Notebook, open the .ipynb file and run all cells.)

🎮 How to Use
Left Click: Set Start Node (Orange), Goal Node (Purple), and place Walls (Black).

Right Click: Remove a node/wall.

'R' Key: Generate a Random map (30% density).

'A' Key: Select A Search* algorithm.

'G' Key: Select Greedy Best-First Search.

'M' Key: Use Manhattan Heuristic.

'E' Key: Use Euclidean Heuristic.

'D' Key: Toggle Dynamic Mode (Spawns walls during transit).

'SPACE': Run the search/simulation.

'C' Key: Clear the entire grid.

📊 Visual Legend
Yellow: Frontier (Nodes currently in the priority queue).

Red: Visited Nodes (Explored/Expanded).

Green: Final calculated optimal path.

Cyan: The Agent's current position during transit.

🧠 Implementation Logic
The agent utilizes a Priority Queue for node expansion. In Dynamic Mode, the agent monitors the final_path array. If a newly spawned obstacle's coordinates match any coordinate in the remaining path, a collision is detected, and the search algorithm is immediately triggered from the agent's current cell to the fixed goal.
