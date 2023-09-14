+++
title = 'Decentralized Gaming'
date = 2023-09-08T13:23:58-07:00
+++

The goal of this project was to get hands on experience building a decentralized app
from start to finish. The app allows two different users to 
play rock paper scissors against each other without the risk of either player cheating. 

- **Game Flow**   
The host player can begin a game session by inputting their opponent's wallet address.
Once the session is live, the address or join code of the session is displayed. The
opponent can now join the game session with the join code. Both players choose rock,
paper, or scissors, along with a secret phrase to "salt" their answer. When both 
players are done, the game moves to the reveal phase where both players input thier
salt, and the winner if determined shortly after.

- **Commit Reveal**   
The commit reveal scheme is implemented through a Solidity data structure called an 
emum. The enum goes through a cycle of four game phases, which change once conditions
on the part of both players are met, such as joining, commiting, revealing, and seeing
the results.
