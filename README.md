# Ex No:
# Date:

# MDP REPRESENTATION

## AIM:
To represent any one real-world problem in MDP form.

## PROBLEM STATEMENT:
To develop a AI agent which controls the level of fluoride percentage in water.

### State Space
{A,B,C} -> {0,1,2}

where,

A->LOWER than required

B->CORRECT amount

C->HIGHER than required

### Sample State
A->0-lower than required

### Action Space
{H,L} -> {0,1}

where,

H -> higher the fluoride percent

L ->  higher the fluoride percent

### Sample Action
H -> 0

which means we have to increase the fluoride percent in water

### Reward Function
```
R = { +1 , for correct amount of fluoride
       0 , otherwise
```
### Graphical Representation
![image](https://github.com/Saibandhavi75/mdp-representation/assets/94208895/2a5d6936-b432-4efb-9f8d-d5c7b441b600)


## PYTHON REPRESENTATION:
```
Developed By: S. Sanjna Priya
Reg No: 212220230043
```
```
P = {
    0 : {
        0 : [(1.0, 1, 1.0, True)],
        1 : [(1.0, 0, 0.0, False)]
    },
    1 : {
        0 : [(1.0, 2, 0.0, False)],
        1 : [(1.0, 0, 0.0, False)]
    },
    2 : {
        0 : [(1.0, 2, 0.0, False)],
        1 : [(1.0, 1, 1.0, True)]
    }
}

P
```

## OUTPUT:
![image](https://github.com/Saibandhavi75/mdp-representation/assets/94208895/aed4bc06-883c-4cfe-87e3-fcdb294d2b52)


## RESULT:
Thus the given real world problem is successfully represented in a MDP form .
