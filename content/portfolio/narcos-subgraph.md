+++
title = 'Narcos Substreams Powered Subgraph'
date = 2023-10-08T13:27:22-07:00
+++

A Subgraph is an open-source and decetralized API with high data correctness that people can 
query from. A Substreams are a way of indexing blockchain data in a parallelizable way to
query blockchain data very quickly. Subgraphs powered by Substreams allows for ready to use 
blockchain data without worrying about using a querying language. The specific goal of this 
project was to filter through mintings of a NFT project called Narcos. From all the mintings,
I wanted to identify which of the Narcos had a particular trait called "cocaine eyes".

# Goals
1. Make a Substreams
2. Filter the blockchain data
3. Make a Subgraph
4. Connect the Subgraph to the Substreams

# Tools
Rust, Substreams Rust Library, Subgraphs, Protobufs, Directed Acyclic Graph (DAG)

# Making a Substreams
Substreams are composed of Rust modules. I learned Rust with the intention of building 
substreams, and learning about the structure of Substreams as well as Substreams Rust Library
was challenging. 

# Map Transfers
The first module in my Substreams was in charge of listening to all blocks and filtering out 
Narco NFT transfers. From these transfers, all the NFTs that had a from address of 0 
(indicating that the transfer was a mint) were filtered so the remaining data to work with 
was every Narcos minted.

# Graph Out
The last module takes the output of the map_transfers module and loads the data into a
subgraph that was made on the Edge and Node website.

# Problems
The main problem in accomplishing the goal is that subgraphs do not have access to data on 
IPFS (Interplanetary File System) which is where NFT metadata is typically stored. The only 
way to find the "cocaine eyes" trait was to look at the metadata on IPFS which was not
possible, so the final Subgraph just contains to mintings of the Narcos NFT.

# Overcoming Problems
If I were to do this project again, I would load my data into a subgraph, and instead load it
into a database where I could use scripts to further filter the NFTs to be left with the ones
with the cocaine eyes trait.
