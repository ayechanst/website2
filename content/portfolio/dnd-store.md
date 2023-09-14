+++
title = 'Dungeons and Dragons Store'
date = 2023-09-08T13:27:22-07:00
+++

As a dungeon master for my pary adventuring through Icewind Dale, I wanted to build
a tool that would make my job easier. Players visiting shops was a problem for me
because shops have hundreds of items and sometimes shops don't exactly have what
players are looking for. So I turned to the internet to generate random stores for
me, but none of them were satisfactory to my standards. So I started to create my own.  

Project link: [Dungeons and Dragons Store](https://dungeons-and-dragons-store.vercel.app/)

# Goals
1. Generate a store
2. Add new items to the store

# Tools
React, TypeScript, Next.js 13, Daisy UI, Firebase

# Store Generation
In earlier prototypes of this application, there was a local database of items that would
be randomly chosen depending on the desired size of the store. Bigger stores would have a
wider range of items. In this working version the app reads all items from the data base
so there is no randomness. 

# Adding items
Adding items works like it did in the prototype, there is a form, and you can input the
item with a description and price. The category of item will add it to one of three 
possible stores. 

# Future updates
Dungeons and Dragons is a big hobby of mine and this project is close to my heart. These
are some basic features I would like to implement when I can make the time.
1. Items in the database are chosen at random
2. More stores and categories (apothecary, magic store, stables, mercenaries)
3. Removable items
4. Better UI
5. Chat-GPT implementation for item descriptions
