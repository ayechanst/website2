+++
title = 'House DAO'
date = 2024-02-06T11:30:06-07:00
+++

This is a prototype of a full-blown decentralized application. It is called Domus DAO
as Domus means home in Roman and I thought an epic app should have an epic name. The
gist of the project is that people living in a communal living space can all join a
DAO. In the DAO members are able to suggest tasks to be done around the house, and
assign members to do the task.
After submitting the "task proposal", members vote on if the task should be vetoed or
approved. If the task is approved then someone becomes the task manager for a period
of time. The time period has not been implemented yet, but when the manager is done,
each member gives the manager a grade. When the task is graded, the "cycle manager"
button is clicked and the next task member is assigned as the task manager.

Projet link: [House DAO](https://nextjs-ji39vo07f-ayechanst.vercel.app/)

# Features

1. Add new members
2. Add new tasks
3. Grade members on the quality of their completed task
4. Cycle the task manager if they are done
5. View a current member's overall reputation

# Tools

Solidity, Next.js, TypeScript, Daisy UI, Scaffold-Eth 2.0, Hardhat

# Adding Members

As this is a prototype, there is no identity verification or crytpo wallet connecting.
The new members are just a string and are added to an array of members.

# Adding Tasks

The tasks are structs in solidity, and have a name, the array of members assigned to
the task, and other meta-data for logic purposes.

# Voting on a Task

Once the new task is proposed, it goes into a voting que where members vote yes or no.
Again, since this is a prototype there is no voting verification of any sort, the user
just clicks yes or no until the votes add up to the amount of members in the DAO, and
the votes are divided by 2 to determine if the task is approved or not.

# Grading the Manager

In the same manner as voting, there is no verification of anything but the user just
gives a grade (should be between 0-10) and the grades are averaged out and assigned to
the task manager.

# Checking Member's Reputation

There is a read function in the smart contract that takes all of a member's grades, adds
the grades up, and divides by the number of tasks they have completed over the course of
being in the DAO. This number is what their reputation is and is what is displayed when
clicked on a member's name in the "Click for Reputation" section.

# Future Features

1. Tasks will be NFTs instead of structs
2. There will be wallet connection and identitiy verification for every step
3. The UI will look amazing
4. There will not be one House DAO, but rather many which can be created on the fly
   to keep different DAO members separated
