## 实验目的

加深对深度优先、广度优先、代价一致搜索、A*搜索等搜索算法的理解，能独立实现这些算法完成Pacman中的任务

## 实验介绍

Pac-Man（吃豆人）是1980推出的迷宫动作视频游戏，加州大学伯克利分校借鉴该游戏开发了开源的人工智能实验项目Pacman，通过编写AI策略引导Agent（智能体）走出迷宫，项目地址：[https://inst.eecs.berkeley.edu/~cs188/fa23/projects/proj1/](https://inst.eecs.berkeley.edu/~cs188/fa23/projects/proj1/)。该实验项目要求编写吃豆人搜索策略解决：找到一个指定位置的豆子、到达四个角落、吃掉所有豆子三大类问题。

## 运行代码

###  Q1：应用dfs找到一个特定的位置的豆

`python pacman.py -l mediumMaze -p SearchAgent`

`python pacman.py -l bigMaze -z .5 -p SearchAgent`

### Q2：应用bfs找到一个特定的位置的豆

`python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs`

`python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5`

### Q3：应用代价一致算法找到一个特定的位置的豆

`python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs`

### Q4：应用A* 算法找到一个特定的位置的豆子

`python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic`

### Q5：找到所有的角落——基于BFS的角落问题（完成CornersProblem）

`python pacman.py -l tinyCorners -p SearchAgent -a fn=bfs,prob=CornersProblem`

 `python pacman.py -l mediumCorners -p SearchAgent -a fn=bfs,prob=CornersProblem`


### Q6：找到所有的角落——基于A*的角落问题（构建启发函数）

`python pacman.py -l mediumCorners -p AStarCornersAgent -z 0.5`

### Q7：吃掉所有的豆子——食物搜索问题（A*算法，构造启发函数）

`python pacman.py -l trickySearch -p AStarFoodSearchAgent`

### Q8：次最优搜索——任意食物搜索问题（优先吃最近的豆子加快搜索）

`python pacman.py -l trickySearch -p ClosestDotSearchAgent`

`python pacman.py -l bigSearch -p ClosestDotSearchAgent -z .5`

### 评分

`python autograder.py`

or

`python autograder.py -q q8` 

## 详细介绍

见[指导书](lab1-pacman实验指导书.pdf)