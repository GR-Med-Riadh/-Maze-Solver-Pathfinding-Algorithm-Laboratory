# 🧩 Maze Solver: Pathfinding Algorithm Laboratory

This project is a visual and analytical tool designed to compare four distinct pathfinding strategies. It allows you to visualize how algorithms "think" when navigating a grid and provides a platform to test which method is the most efficient for different maze layouts.

## 🔬 The Algorithms Explained

### 1. Breadth-First Search (BFS)
* **Strategy:** Explores all neighbors at the current depth before moving to the next level.
* **Best for:** Finding the **shortest path** in unweighted grids.
* **Behavior:** It radiates outward from the start like a ripple in water.

### 2. Depth-First Search (DFS)
* **Strategy:** Dives as deep as possible into one branch before backtracking.
* **Best for:** Memory efficiency (in some cases) or simply finding *any* path.
* **Behavior:** Often results in long, winding paths.

### 3. A* Search (Heuristic-Based)
* **Strategy:** Uses a "Best-First" approach by calculating the cost function:
    $$f(n) = g(n) + h(n)$$
    Where $g(n)$ is the cost from the start and $h(n)$ is the estimated distance (heuristic) to the exit.
* **Best for:** Finding the shortest path with the **least amount of exploration**.
* **Behavior:** Highly targeted; it "aims" for the exit.

### 4. Wall Follower (Right/Left-Hand Rule)
* **Strategy:** Always keeps a hand on the wall to the side.
* **Best for:** Simple, non-looping mazes.
* **Behavior:** It doesn't "know" where it's going; it just follows the physical structure of the maze.

---

## 🛠️ Instructional: How to Import Your Own Maze

This tool is designed for experimentation. You can easily test a custom layout by modifying the `maze` variable in the script:

```python
# 'S' = Start, 'E' = End, 1 = Wall, 0 = Walkable Path
maze = [
    [1, 1, 1, 1, 1, 1],
    [1, 'S', 0, 0, 1, 1],
    [1, 0, 1, 0, 0, 1],
    [1, 0, 0, 0, 'E', 1],
    [1, 1, 1, 1, 1, 1]
]
