# Mobile Games A/B Testing with Cookie Cats

## Introduction
- Cookie Cats is a popular mobile puzzle game in which the player must connect tiles of the same color in order to clear the board and win the level. 
- As players progress through the game they will encounter gates that force them to wait some time before they can progress or make an in-app purchase.
- For this project, I will analyze the result, more specificly the impact on player _retention_, of an A/B test where the first gate in Cookie Cats was moved from level 30 to level 40.
- The definition of player _retention_ in this project is the player comes back and play the game after installing.

## Scope

### Problem
- By changing the first gate in Cookie Cats from level 30 to level 40, will the player retention rate increase or decrease? 

### Goal
- Identify the association between versions and retention rates for one day and for seven days.
    - association will be based on significance threshold 5%
- Decide if the game should set up the first gate at level 30 or at level 40.
- (Further research needed) Create user segmentations where different groups of users have the first gate set up at different levels.

### Action
1. Pick two groups of users randomly, each with the same number of users. The control group will install the gate_30 version where the first gate appears at level 30, and the experimental group will install the gate_40 version where the first gate appears at level 40.
2. Count the number of rounds each group of users play during the first 14 days after install.
3. See if the user come back and play the game again the next day and the seventh day after installing.
4. Use Chi Sqaure contingency test to calculate the association between the two versions and retention_1 and retention_7.

### Data
- I will use 'cookie_cats.csv' dateset. It contains five columns:
    1. userid: a unique number that identifies the player
    2. version: whether the user is in the control group (gate_30, the first gate appears at level 30) or in the experimental group (gate_40, the first gate appears at level 40)
    3. sum_gamerounds: the number of game rounds played by the player during the first 14 days after install.
    4. retention_1: whether the player comes back and plays 1 day after installing.
    5. retention_7: whether the player comes back and plays 7 days after installing.

### Types Analysis Done
- Description
- Optimization
- Behavior Change

## Conclusion
- There is no significant association between the two versions of game and the retention in one day; however, there is a significant association between the two version and the retention in seven days, which means that the change of the gate in the game will impact on users' retention in the longer term, although seven days is still too short to judge the overall impact.
- The experimental group's retention is lower than the control group, meaning users are more likely to come back after seven days if the gate appears at level 30. However, it can be considered that a gate set up at a lower level will increase retention, since currently 50% of players play 16 times or fewer.
