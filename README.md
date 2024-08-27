# Ex01-MDP REPRESENTATION

## AIM:
To represent a Stochastic MDP (Markov Decision Process) problem in the following ways.
  1. Text representation
  2. Graphical representation
  3. Python - Dictonary representation

## PROBLEM STATEMENT:

### Problem Description
An agent, represented as a boy/girl character, has to move in an environment to avoid getting lost on his way to school. Within this environment, there are several paths, some leading to the school and some taking the agent further away from the goal. At every step, the agent aims to make correct decisions that help him to remain on the paths leading toward the goal. Finally, when the agent reaches school, this step is rewarded; otherwise, it is not rewarded. The task positions learning how to identify the correct path and follow it as analogous to a real-world task: reach the goal, without deviation.

### State Space
{0,1,2,3}

### Sample State
* 0 -> Starting point(S)
* 1 -> Relaxing point(R)
* 2 -> Goal point(G)
* 3 -> Restricted point(D)

### Action Space
{1,2}


### Sample Action
{1} Moving up
{2} Moving down

### Reward Function
*  If the goal is reached -> reward=+1
*  Else -> reward=0

### Graphical Representation
<img src="https://github.com/user-attachments/assets/00ff1d27-791b-497d-80e7-6461360e0249" width=50%>

## PYTHON REPRESENTATION:
```python
solved_mdp = {
    # Start Point State(S) -> 0
    0 : {
        # Action: up -> 0, down -> 1
        0: [(0.65, 1, 0, False), (0.35, 0, 0, False)],
        1: [(0.70, 0, 0, False), (0.30, 1, 0, False)]
    },
    # Relaxing point state(R) -> 1
    1: {
        # Action: up -> 0, down -> 1
        0: [(0.90, 2, 0, False), (0.10, 0, 0, False)],
        1: [(0.75, 0, 0, False), (0.25, 2, 0, False)]
    },
    # Goal point state(G) -> 2
    2: {
        # Action: up -> 0, down -> 1
        0: [(0.85, 3, 1, True), (0.15, 1, 0, False)],
        1: [(0.92, 1, 0, False), (0.08, 3, 1, True)]
    },
    # Restricted point(R) -> 3
    3: {
        # Action: up -> 0, down -> 1
        0: [(0.80, 3, 0, True), (0.20, 2, 0, False)],
        1: [(0.85, 2, 0, False), (0.15, 3, 0, True)]
    }
}
solved_mdp
```

## OUTPUT:
<img src="https://github.com/user-attachments/assets/34d79098-c7d4-45da-80a5-03b72eea4a67">

## RESULT:
Thus a real world problem is represented as Markov Decision Problem in the following ways
successfully:
- Text Representation
- Graphical Representation
- Python Representation
