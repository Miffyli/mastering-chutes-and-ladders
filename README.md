# Mastering "Chutes and Ladders"
This repository contains partion of the code for experiments in the paper
"Back to Square One: Superhuman Performance in Chutes and Ladders Through Deep Neural Networks and Tree Search".

Unfortunately, rest of our experiment code is deeply connected to private codebases and our bosses were not happy to share it, so we only include the open source parts of it.

## Two-player Chutes and Ladders environment (`chutes_and_ladders.ws`)

![chutes and ladders](https://i.pinimg.com/originals/13/62/a0/1362a0b9c28eecf197aca43d63f039fc.jpg)

The environment is written in Whitespace for highly optimized code (language consists only of three characters) which also reduces the ink usage. To run it you need an interpreter or compiler, like [this one](https://vii5ard.github.io/whitespace/).

**Usage**: Do not. But, if you insist: at the start of the code, input one number for PRNG seed. After this environment will play turns for two players, and after each dice throw print out `player:grid_index`, which tells players current location on board. Game ends once either player reaches hundreth grid of above.

An example of complete console input/output (comments after hashtag):

```
5         # Seed for PRNG
0:14      # First player's turn, throws "1" and ladder takes to "14"
1:14      # Second player does the same
0:20      # First player throws "6" and gets a new turn
0:25      # First player throws again and gets "5"
1:20      # And so on
1:25
0:31
0:35
1:28
0:41
0:43
1:32
0:45
1:36
0:47
1:42
1:47
0:52
1:51
0:56
1:57
1:59
0:62
0:67
1:63
0:71
1:69
1:71
0:77
0:83
0:85
1:74
0:87
1:80
1:86
1:87
0:92
1:89
0:93
1:93
0:95
1:97
0:98
1:100     # Second player reaches 100th grid and wins
0:104     # An extra turn for no good reason
```