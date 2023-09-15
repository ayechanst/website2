+++
title = 'Decentralized Gaming'
date = 2023-09-08T13:23:58-07:00
+++

[Block Paper Scissors](https://block-paper-scissors.vercel.app/) is a game that uses 
a commit reveal scheme to make cheating impossible.

# Goals
1. Allow a player to host a game
2. Allow a different player to join that same game
3. Have the players commit an answer with salt
4. Have the players reveal their answer at the same time
5. Compare the answers and determine a winner

# Tools
TypeScript, Solidity, Hardhat, Scaffold-eth 2, Ethers.js, Daisy-ui

# Hosting and joining a game
Player 1 creates a game by putting in the wallet address of their opponent.
There is an enum that changes from join phase, commit phase, reveal phase, 
and results phase. While the player 1 waits for player 2 to join, the game 
stays in the join phase which is the default phase. When player 2 joins, the 
game moves on to the commit phase.

# Commit phase & problems
Both players choose either rock, paper, or scissors, along with a salt, or
random data to mix up into their answer, so that their opponent cannot check
to see what that player picked. Originally the game had a function in the 
smart contract that took in two arguments from the front end, which was the
players choice and the players salt. This was a big security problem because
etherscan and other websites that monitor the blockchain can read the argument
values. Because of this, players choices and salt were on public display. This
problem was fixed when I use the ether.js library to hash player's answers in
the React component, instead of in the contract. 

# Reveal phase
Once both players commit and salt their answers, the game state enum moves to 
the reveal phase were players re-input their salt, so that the reveal function
can decrypt the hashed commit and compare the two players results.

# Results phase
This phase just displays who won. 

# Potential future updates
1. It would be cool to add a betting mechanism since this game is so secure
