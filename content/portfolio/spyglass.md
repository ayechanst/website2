+++
title = 'Spyglass Labs'
date = 2023-09-08T13:10:53-07:00
+++

[Spyglass Labs](https://soulbound.xyz) is a web3 startup that I intered at. The platform is a no-code data
analytics platform similar to something like Dune Analytics.

# Goals 
1. Gather data to demonstrate the functionality of the platform
2. Write tests to ensure the UI and UX works smoothly as new features are implemented

# Tools
Javascript, Python, Cypress, Selenium, Infura 

# Data gathering execution for Ethereum mainnet and Near
The data my intern colleague and I collected were the names and ABI's of the 100 most transacted on smart 
contracts. The data was used to populate sample subgraphs so users could have a better idea of what Spyglass
was capable of. The idea was that people could see Spyglass in action with some of the most popular decentralized
apps. For mainnet, we used infura to connect to the etherscan API, then we wrote scripts in JS to filter through the data so
that we were left with the top 100 contracts.  

The problem was that etherscan obscured the transation count beyond 10,000 transactions, so we were left with
much more than 100 contracts post filtering. We got around this by writing Python scripts in Selenium to scrape 
the most popular smart contracts for their real transation count. After doing so we suspected the contracts we
aquired were not the right ones because their transation counts were much lower than the expected number for 
such popular contracts.  

After that failed, my colleague and I divided the labor and he would find a work around for the mainnet problem,
and I would scrape the Near blockchain to populate a JSON file with the required fields. The co-founders who 
assigned us this task recommended instead of data collecting based on transaction count, we should collect data
on the basis of popularity. I found a Near website that listed the current most popular smart contracts within 
the past month and manually filled out the JSON file to completion. The mainnet file was also completed and sent.  

In summary this job was comprised of writing scripts that worked in terms of getting us data, but not the correct
data. The problems were overcome by brute forcing our results which in hindsight took a lot less time than
automating the process.  

# Test execution 
The start of the testing began with familiarizing ourselves with the Cypress testing frame work. After reading 
documentation and watching videos, we began writing a few simple tests. After those first few tests work, we spent
time discussing and planning who was going to write which test for what. The tests I wrote ensured that the flow 
of the UX was smooth from the initial login to the viewing of the completed subgraph.  

The main challenge was implementing an asycronous loop in Cypress so that tests that followed the same steps 
could be looped over instead of written several times. The challenge was over come with a lot of trail and error
but the tests were completed.  
