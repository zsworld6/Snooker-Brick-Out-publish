# Brick Out Simulator

### About the `Game` Class

The `Game` class stores the game map and runtime information. By default, it reads the initial map information from the `map.in` file located in the same directory as `game.h` during initialization. To prevent stack overflow, it is recommended to create the `game` object using the `new` operator.

The `game` class provides several public functions for use.

##### `int play(char)`

This function accepts a char parameter as the provided instruction. The class will automatically run until the next instruction is needed, and returns the reward value obtained during this process. (Hint: you can also modify the return value according to your needs.)

##### `Game::Save *save(void)`

Saves the current game state and returns a save pointer.

##### `void load(Game::Save *save)`

This function accepts a save pointer and loads the game state to the corresponding saved state.

##### `void erase(Game::Save *save)`

This function accepts a save pointer and deletes the corresponding save.

##### `int bricksTotal()`

Returns the initial total number of bricks in the map.

##### `int bricksHit()`

Returns the number of bricks that have been hit in the map.

##### `int bricksRemaining()`

Returns the number of bricks remaining in the map.

##### Note

Each save creation and load operation takes $O(n^2)$ time. To avoid TLE (Time Limit Exceeded), we do not recommend excessive save/load operations.

Correctness is not guaranteed when the number of valid saves exceeds $1e4$.
