
### Maxime Legarde : AI for Chess

# Running the program

Feel free to create an environment of your own and then run the command : pip install -r requirements.txt

# Interface

The interface where you play is made using **pygame** 2.1.2 and **numpy** 1.22.4.

All the rules of Chess are implemented. There are still a few buggs.

# AI

The AI is a Neural Network built using **tensorflow** 2.9.1. 

It is constituted of a first input layer of shape (14,8,8) which represents the position of each piece in the board separately from the others.
This means that there are 12 inputs attributed to the board for each type of piece. The two left are dedicated to the position of all pieces and to the pieces being attacked based on which player has to play.

After the input layer there are 4 Conv2D layers activated using the 'relu' function. After there is a Flatten and a Dense 64 activated with a 'relu' and finally a Dense 1 to know the evaluation of the position by our network.

The AI has been trained in a database of more than 10^6 millions of positions evaluated by stockfish_15 which has won the 11, 12, 13 and 14th season of the **Top Chess Engine Championship**.

# Playing Moves

The AI is having difficulties playing moves involving tactics as it only searches one move ahead. This needs further improvements.
