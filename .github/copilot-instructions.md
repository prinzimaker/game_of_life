# Copilot Instructions for Game of Life

## Project Overview
This repository contains an implementation of Conway's Game of Life, originally developed for the MAC LC in the early 1980s.

## About Conway's Game of Life
Conway's Game of Life is a cellular automaton devised by the British mathematician John Horton Conway in 1970. It is a zero-player game, meaning that its evolution is determined by its initial state, requiring no further input.

The universe of the Game of Life is an infinite, two-dimensional orthogonal grid of square cells, each of which is in one of two possible states: live or dead. Every cell interacts with its eight neighbors, which are the cells that are horizontally, vertically, or diagonally adjacent.

### Rules
At each step in time, the following transitions occur:
1. Any live cell with fewer than two live neighbors dies (underpopulation)
2. Any live cell with two or three live neighbors lives on to the next generation
3. Any live cell with more than three live neighbors dies (overpopulation)
4. Any dead cell with exactly three live neighbors becomes a live cell (reproduction)

## Development Guidelines

### Code Style
- Follow clean code principles
- Use descriptive variable and function names
- Add comments for complex logic
- Keep functions small and focused on a single responsibility

### Testing
- Write tests for core game logic
- Test edge cases and boundary conditions
- Ensure patterns behave correctly according to the rules

### Common Patterns
When working with Game of Life implementations, be aware of common patterns:
- **Still lifes**: Patterns that don't change (e.g., block, beehive, loaf)
- **Oscillators**: Patterns that return to their initial state after a finite number of generations (e.g., blinker, toad, beacon)
- **Spaceships**: Patterns that translate themselves across the grid (e.g., glider, lightweight spaceship)

### Performance Considerations
- Consider efficient algorithms for computing the next generation
- Optimize neighbor counting operations
- Handle infinite grid implementations efficiently

## When Making Changes
- Ensure the core game rules are preserved
- Maintain backward compatibility where possible
- Document any new features or pattern implementations
- Consider the historical context of the original MAC LC implementation
