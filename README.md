# TicTactToe

(Assuming that the reader is familiar with the rules of the game) - This project's objective is about training a machine agent to play against a human player. The following steps were followed to achieve this objective:
1. A simple program to play Tic Tac Toe was created - where the machine agent makes random moves.
2. The machine agent was trained to learn - to play the game intelligently - 
3. A set of game features based on board positions were created. Initial uniform weights corresponding to all these features (and including one bias weight) were initialized to 0.5. 
4. The agent which was to learn would pick the board position based on the highest sum product of the features and corresponding weights. 
5. Likewise, it picks each move till the game is over. The other machine agent is just making random moves. At the end of the game, the weights of the learning agent is updated. 
6. For the weight update - a preceding step is required - that of finding the Target and actual values. The actual values are the values of the sum product of the features and weights. The target values for the final board state are 100 if the learning agent wins the game, 0 if the game ends in a tie and -100 if the learning agent loses the game against the other agent. The target values of the previous board states are slightly tricky - they are the actual values of the successor board state. For instance, the target value of the penultimate board state would be the actual value of the last board state.
7. The weight update is done by the simple perceptron weight update formula Wnew = Wold + Learning rate * (Target - Actual values) * Input Feature
8. Both the agents played for 1000 times and at the end of each game, the weights were updated.
9. Finally, the trained agent was pitted against a human player. The agent would use its final set of weights. It does manage to remain unbeaten.
10. But there are scenarios - where instead of capitalizing on clear winning positions, it gets into a defensive mode. Need to figure out how this can be corrected.

I was inspired to do this project by the first chapter in Tom Mitchell's book on Machine learning. I also benefited in equal measure by this blog https://chrismaclellan.com/blog.html.

It was definitely a valuable learning experience - both in terms of coding an end - to - end project as well as understanding the basic blocks of machine learning.

Disclaimer: Code quality has lots of scope for improvement.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Rajivh/TicTactToe/master)
