# TicTacToe-RL-Self-Play
## Description : Teaching an ai to play tictactoe using q-learning

# Q Learning for 2 player Games 

Who to play against? 
- Random
- Bruteforce minimax
- against yourself!
You typicaly want an enemy that's always trying to match ur current skills , and levels up with you , so You are playing against your own policy.
Problems : 
- Overfitting stratigies
- Unstable Learning

# How to try to reduce these problems 
Solution : we don't play vs out current policy but we keep a buffer with latest n policies and pick one as our enemy.
![image](https://user-images.githubusercontent.com/64399795/177513987-74787ac5-8fb9-490b-a305-4463652e99b9.png)
![image](https://user-images.githubusercontent.com/64399795/177514033-105fc7c7-ee9e-45e0-9c04-4d14e0af82d5.png)

The length of the policy buffer is usually ranges from 5 to 30.
every 10k+ steps we update the buffer throwing the oldest policy and adding the current.
![image](https://user-images.githubusercontent.com/64399795/177514334-64e7207d-4011-4e2b-9e6e-f6279dc043c8.png)

Saving Different Policies :
- Saves Range of skills to play against
![image](https://user-images.githubusercontent.com/64399795/177514621-c374ccf3-148c-4fe4-b1ff-bed7d0ba5be7.png)

# Results
![image](https://user-images.githubusercontent.com/64399795/177515088-f52a5a69-654b-4c8e-81e2-eda744dce1da.png)
