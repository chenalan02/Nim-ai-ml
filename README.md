# Nim-ai-ml
Using a q-learning algorithm to teach an ai to play Nim. Nim is a game where there are piles of objects from 4 piles and each player takes turns taking a non zero number of objects out of a chosen pile. The person who ends the game by taking the last tile(s) loses the game. Compile play.py to play against the ai

## Logic
The ai is trained to play the game by repetetively playing against itself by initially choosing random actions. If the ai makes an action in a state and either wins or loses, that action-state pair is given a positive or negative reward respectively. Tthe q value of that action-state pair is then changed by a non zero value. If the ai is in the same state in the future, it will be more likely/unlikely to choose that action depending on the reward. The magnitude of the change in q value given a reward is also affcted by the predicted future rewards. In a specific state, if the ai knows that it has the potential to gain a positive rewards through any one of its actions, it will be inscentivised to reach that state if it is in a previous state. This causes a trickle down effect to all possible states. The ai is also encouraged to explore rather than just perform actions it knows will be beneficial. This way, it has the potential to find pathways it had previously not found that may be more beneficial. I have programed it to randomly choose an action with a 10% chance.

## Template
This was an assignment in which I built upon a template from the Harvard CS50 online course. It can be found at https://cs50.harvard.edu/ai/2020/projects/4/nim/

![Nim](https://github.com/chenalan02/Nim-ai-ml-Harvard-cs50ai/blob/master/Nim.JPG)
