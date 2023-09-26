## MDP REPRESENTATION 
## AIM:
The aim of this MDP representation is to model the interaction between the agent "Staff" and the environment "Students" in a classroom setting where the agent can take actions like "Teaching" and "Monitoring" in different states.

## PROBLEM STATEMENT
The problem is to define an MDP that represents the agent's decision-making process in managing students who can be in states of "sitting," "listening," or "talking."

### State Space
- "sitting"
- "listening"
- "talking"

### Sample State
A sample state can be "sitting," where the students are sitting quietly.

### Action Space
- "Teaching"
- "Monitoring"

### Sample Action
A sample action can be "Teaching," where the agent engages in teaching activities.

### Reward Function
The reward function is not explicitly defined in the provided information, but it assigns rewards to state-action pairs based on the agent's goals. It should encourage actions that lead to desired outcomes and discourage unwanted behaviors.

### Graphical Representation
![WhatsApp Image 2023-09-20 at 16 14 27](https://github.com/arunraj2002/mdp-representation/assets/75235747/b7e6c164-71f2-4e60-8cc5-72b6f33a3942)

## PYTHON REPRESENTATION
```python
# Define the states
states = ["sitting", "listening", "talking"]
# Define the actions
actions = ["Teaching", "Monitoring"]
# Define the MDP as a dictionary of dictionaries for transition probabilities and rewards
MDP = {
    "sitting": {
        "Teaching": [(0.8, "sitting", 0.0, True), (0.2, "listening", 0.0, False)],
        "Monitoring": [(0.8, "listening", 0.0, False), (0.2, "sitting", 0.0, True)]
    },
    "listening": {
        "Teaching": [(0.8, "sitting", 0.0, True), (0.2, "talking", 1.0, True)],
        "Monitoring": [(0.8, "talking", 1.0, True), (0.2, "sitting", 0.0, True)]
    },
    "talking": {
        "Teaching": [(0.8, "listening", 0.0, False), (0.2, "talking", 0.0, True)],
        "Monitoring": [(0.8, "talking", 0.0, True), (0.2, "listening", 0.0, False)]
    }
}
```
## OUTPUT:
![Screenshot 2023-09-19 144424](https://github.com/arunraj2002/mdp-representation/assets/75235747/0ac5d5ef-9e58-48ae-bfa7-437fc8c08b8a)
## RESULT:
The result will be the optimized policy that the agent "Staff" should follow to maximize its expected rewards while managing the students in different states and taking appropriate actions.
