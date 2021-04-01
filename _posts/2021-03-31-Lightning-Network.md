---
layout: post
title: "What is The Lightning Network?"
subtitle: "The Second Layer of Bitcoin"
date: 2021-03-31
background: '/img/posts/bitcoin-lightning.jpg'
---

Recently, I have been hearing a lot about the Lightning Layer of Bitcoin.

I do not really know much about it, other than it should make transactions quicker and cheaper (I’m not even sure if that is correct), So I am writing this article/blog post explaining what the Lightning Network is.

# The Basics
In order to understand what the Lightning Network does, you need to understand what Bitcoin is, and the basics of how it works. If you do not know much about Bitcoin, I suggest that you take you read this article to learn about Bitcoin.

The Bitcoin Blockchain can currently handle about 7 transactions per second, whereas if you look at Visa or MasterCard, they handle about 4000 transactions per second. Comparing Visa and Bitcoin, we can see that Bitcoin is unable to handle a large number of transactions. Additionally, each bitcoin transaction must be sent to the blockchain in order to be verified. It does not matter if you are sending $1 or $1 million dollars, your bitcoin transaction fee will remain the same. New Blocks are added to the Bitcoin Blockchain every ten minutes as well.

# The Problem
Well, so there are two problems here: 
  1) Bitcoin is unable to handle a large number of transactions.
  2) Transactions are not instant.
  3) Every transaction must be stored onto the blockchain transaction -> have to pay fees for each transaction.

# The Solution
This is where The Lightning Network, also known as the second layer of Bitcoin, comes in. The community behind the Lightning Network believes that small, everyday transactions do not have to be stored on the Bitcoin blockchain. It is easier to explain how the Lightning Network works by providing an example.

Imagine that on your way to school or work (before COVID), that you go to your local coffee shop and buy a coffee and a bagel every day. If you were to pay in bitcoin, you would likely end up spending more money on the transaction fee then your coffee and donuts, and it quite slow to verify your transaction.

So, what the Lightning Network proposes to do is to setup a Payment Channel between yourself and the coffee shop. Through this payment channel you will be able to send each other Bitcoin “Off-Chain” (without sending it to the Bitcoin blockchain).

To do this, both yourself, and the coffee shop will deposit bitcoin into a multigeniture wallet. You can think of multisignature wallet as a vault which to store the bitcoin and needs multiple keys in order to open. In this case, you need both your and the coffee shop’s private key to unlock (We will come back to this concept in a second) the vault.

Assume you deposit 0.05 bitcoin, and the coffee shop deposits 0.01 bitcoin; the “vault” now contains 0.06 bitcoin. These transactions of sending your bitcoin to the wallet occur on the blockchain. The Lightning Network will keep track that how much bitcoin each party owns. So now when you buy a coffee for 0.005 bitcoin, you can subtract 0.005 bitcoin from your balance (0.05 - 0.005 = 0.495 BTC) and add 0.005 bitcoin the coffee shop’s balance (0.01 + 0.005 = 0.015 BTC). Both you are the coffee shop verify that this transaction is correct, by signing the transaction with your private keys. You and the coffee shop can have thousands of transactions on the payment channel, and they can be verified almost instantly.

Okay, now that’s great, but what do you do when you want your bitcoin back? Both you and the coffee shop can close the payment channel by broadcasting your final balance sheet to the bitcoin network. Keep in mind here, BOTH parties must agree to close the payment channel, to unlock the “vault”. If the bitcoin network verifies your both of your balance sheets, the vault will be unlocked, and each party will receive their respective bitcoin balances.

# My Thoughts
I think the Lightning Network as a whole is fantastic. However, practically speaking though, would I want to actally make everyday payments with bitcoin? Absolutlety not! The reason for that is the bitcoin price is always changing! I do not want to end up like Laszlo Hanyecz who ended up spending [about $600 million on two pizzas](https://www.businessinsider.com/bitcoin-surge-means-laszlo-hanyecz-paid-316-million-two-pizzas-2021-3#:~:text=The%20programmer%20Laszlo%20Hanyecz%20has,as%20%22Bitcoin%20Pizza%20Day.%22) when he bought them using Bitcoin.

Personally, although I think the Lightning Network is great, I do not think I will be making use of it anything soon.

