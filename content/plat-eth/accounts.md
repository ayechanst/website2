+++
title = 'Accounts'
date = 2024-02-19T12:05:12-07:00
+++

Lets start with a short story to get you situated. After the story we will go into the specifics and purposes of the **items**. Things in bold are the focus point of the lesson, here they are before the story so you know what to look out for:

1. Train Station
2. Address
3. Public Key
4. Private Key
5. Balance
6. Nonce

# A Little Lonely Station

> Walking through rolling hills of short grass, you stumble accross a very old and decrepid **train station**.

> As you approach the station with great curiosity, you walk pasts a tiny mailbox. It looks like there's something on it, so you pull out your magnifying glass and place it up to the shrinking mailbox. On the side of it, you see an **address**.

> On the other side of the mailbox, there is a shiny hook upon which hangs a **public key**. You don't think much of it aside from the ridicously small size of it all, put away your magnifying glass, and procceed on a stone path leading to the station.

> The door of the station has a huge chain around it with a massive lock swinging in the breeze. Despite the station's age, no one is getting in here without a key. But you hear a click in the lock and the door magically creaks open. You step inside and cough at the dust. On the left side of the room there is a weird object covering the whole table. Its a wax stamp with a handle, but the handle is also a key. Etched on the key in beautiful cursive is written "**private key**". You see red wax oozing and dripping from the stamp side of the key.

> On the other side of the room you see a balance surrounded by a pile of coins. The coins are being counted by a small flying robot with a number displayed on its back screen. The screen says, "**balance**: 101 coins".

> The back wall of the station has a door leading to the platforms. Next to the door is a poster that says "**Nonce**: 3". You take a seat on the floor and consider everything you just saw.

# Accounts in Ethereum

Read [this](https://ethereum.org/developers/docs/accounts#types-of-account) short article about accounts after
reading this paragraph. In the article they mention **contract accounts**, pay no special attention to those, we will cover them later. Just
remember the key differences under **externally-owned**, and the **externally-owned accounts and key pairs** section. And the visual demo
videos by Austin are a must watch for a solid understanding of how key pairs work all analogies aside.

# Recap of the story

Answer the following questions in your head:

1. In the rolling hills of grass, what did you stumble accross?
2. What two **items** were on that tiny mail box that you couldn't see without a magnifying glass?
3. In side the building, what huge **item** was on the desk?
4. What was on the other side of the room? What was displayed on the flying robots back?
5. Next to the door leading to the train platform, what was the name of that number on the poster?

# Accounts are train stations

Why? Accounts are a pair of keys called the **public key** and **private key**. They are owned by someone, the same way a train station is
owned by, or operated by someone, or something. Think of externally owned accounts (EOA)s as train stations. They are externally owned
because they have keys that belong to someone. EOA are also like train stations because they are the only type of account that can inititate
transactions as the the [article](https://ethereum.org/developers/docs/accounts#types-of-account) mentions. A transaction is like a train but
that's not until a later article.

# Addresses and public keys are on a mailbox

Everyone can see your address on your mailbox, and it works the same in Ethereum. Addresses are public, and so are public keys. How are the
keys and addresses related? A private key is randomly generated. From the private key a public key is generated using elliptic-curve
cryptography. Then an **address** is generated from the public key. The three things are **not** the same.

# The private key is a key and a stamp?

What's with the stamp you might be asking. A private key is needed to get into the account, so it can be seen as a key. But the private key
is also used to sign transations. In medival times, letters were stamped with a wax seal to confirm who it came from and if it the letter had
been opened yet. So the private key is used to access accounts, and also used to sign transactions.

# The account balance

Accounts hold money plain and simple. So inside the train station locked behind the door is money. Accounts have a balance like any old bank
account. There can be all sorts of money in there but this account just has one type for simplicity. Of course the money cannot be accessed
without a private key which is why its locked inside the train station.

# Nonce

This is not too important at the moment, but the nonce is a number that keeps track of the amount of transctions sent by a certain account.
This is why the **nonce poster** is set right next to the train platform door. It keeps track of how many trains have been sent. We keep
track of the nonce to prevent re-entrancy attacks which you can read about [here](https://blog.daisie.com/cryptographic-nonce-a-practical-understanding-guide/).
