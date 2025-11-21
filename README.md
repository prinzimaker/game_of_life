# game_of_life

Conway's game of life, developed for MAC LC early '80s

## About Conway's Game of Life

Conway's Game of Life is a cellular automaton devised by British mathematician John Conway in 1970. It is a zero-player game, meaning that its evolution is determined by its initial state, requiring no further input from humans. The Game of Life takes place on a two-dimensional grid of cells, where each cell can be in one of two states: alive or dead.

## The Rules

The game operates on a simple set of rules that determine the state of each cell in the next generation based on its current state and the states of its eight neighboring cells:

1. **Underpopulation**: Any live cell with fewer than two live neighbors dies, as if by underpopulation.
2. **Survival**: Any live cell with two or three live neighbors lives on to the next generation.
3. **Overpopulation**: Any live cell with more than three live neighbors dies, as if by overpopulation.
4. **Reproduction**: Any dead cell with exactly three live neighbors becomes a live cell, as if by reproduction.

## How It Works

The game begins with an initial configuration of live and dead cells on the grid. As the simulation runs, each generation (or "tick") applies the rules simultaneously to every cell, creating the next state of the grid. Different initial configurations lead to different evolving patterns - some patterns stabilize, some oscillate, and some continue to grow and change indefinitely.

The fascinating aspect of the Game of Life is that these simple rules produce complex, unpredictable, and often beautiful patterns. Certain configurations, like "gliders" and "spaceships," move across the grid, while others, like "blinkers" and "toads," oscillate in place.

## Emergent Behavior

Despite the simplicity of its rules, Conway's Game of Life demonstrates how complex behavior can emerge from simple local interactions. It has been shown to be Turing complete, meaning it can simulate any computation that can be performed by a computer. This makes it not just a game, but a powerful demonstration of how complexity and life-like behavior can arise from simple mathematical rules.
