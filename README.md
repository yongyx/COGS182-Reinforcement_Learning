# COGS182-Reinforcement_Learning

The source code provided contains the SnakesAndLadders class and Agent classes. The SnakesAndLadders class is responsible for creating the environment while the Agent class is responsible for being the player that interacts with the environment. 

In-built Libraries Used:
- numpy as np
- matplotlib.pyplot as plt
- tqdm as tqdm

SnakesAndLadders Methods:
- __init__ : initializes the board and other variables
- reset: resets the board for multiple runs
- step: steps through the environment (board) given an action, returns subsequent state, reward and whether the program is terminal or not.
- showBoard: shows the board and how many times the agent has landed in each state
- getCurrent: returns the current state
- setCurrent: sets the current state

Agent Methods:
- __init__: initializes the Agent with a Q-value array and alpha, gamma and epsilon.
- reset: resets the actions of the Agent
- roll_dice: rolls an unfair dice and returns the resulting diceRoll.
- ep_greedy: chooses an action based on an epsilon-greedy policy given a state, returns an action.
- updateQ: does an update on the Q values given the state, action, state' and reward.
- getQValues: returns the Qvalues.
- getActions: returns a list of actions that the agent took.
- resetQ: resets the Qvalues to an empty array of zeros.

Test Methods:
- testSAndL: tests the whole game once and shows the board.
- testStep: tests the step method of the SnakesAndLadders class and prints the input state, dice roll, next state and reward.
- testRollDice: tests the roll_dice method of the agent and prints the frequency of each number on the dice.

Plotting Methods:
- plot_heatmap_max_val: generates the heatmap showing the maximum value at each state. Recevies environment, value function, title of algorithm, and axis as input, returns im.
- plot_actionNum_vs_episodes: receives the number of episodes, the list of actions, the algorithm title and the axis as input and plots the number of actions taken vs the number of episodes.

QLearning:
A method that receives the number of episodes, the environment and agent, and conducts Q-learning, returns a list of actions taken by the agent for each episode.

DynaQ:
A method which receives the environment, agent, model, max_steps, n_planning_steps and conducts the Dyna-Q, returns the model and steps taken per episode.

__NOTE:__
- All cells are placed in order in the Jupyter Notebook and should be compiled and ran from top to bottom. tqdm has been put in certain loops to ensure that the program is running effectively and not stuck in an infinite loop due to the large number of episodes.
