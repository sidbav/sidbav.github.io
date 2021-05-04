---
layout: post
title: "Part 2: What is The Lightning Network?"
subtitle: "A followup to my previous post"
date: 2021-04-02
modified_date: 2021-04-10
---

Update (April 10): If you want to learn more about the Lightning Network, you can refer to this [guide](https://docs.lightning.engineering/conceptual-overview/overview-overview). This goes into a lot of detail, you will be able to learn a lot from it!

Okay, so it have been a couple days since I wrote my first [post](https://sidbav.github.io/2021/03/31/Lightning-Network.html) about the Bitcoin Lightning Network. Go check it out if you have not read that post.

The morning after I wrote that post I realized that I barely scratched the surface of the second Layer of Bitcoin. I thought it was pretty cool that you are able to setup a payment channel between two parties, but I did not even consider the Network part of the Lightning Network.

Continuing from the previous post, let say that you and the coffee shop have a payment channel, and you and one of your other friends Bob set up a payment channel as well. Bob goes to the coffee shop, and wants to pay them in Bitcoin. He owes them 0.005 BTC.

There are three options here:
1. Bob can send the bitcoin "On-Chain" to the coffee shop. The problem with this is that he will have pay the cost of transaction fees, which will probably cost even more than the coffee. Also, this is quite slow given that a new block is only formed every ten minutes.
2. Can set up a direct payment channel between the coffee shop between himself and the coffee shop. But this has the same problems as Option 1, since On-chain transactions must take place in order to set up the payment channel.
3. The payment goes through yourself. First Bob sends you the payment, and then you send the payment to the coffee shop. A visual depiction of this option helps make is more clear.

So here is the initial setup: Bob and yourself have a payment channel, and you each have deposited 0.05 BTC. You and the coffee shop also have a payment channel.
{% include image.html url="/img/posts/payment1.png" description="The initial setup" %}

So now Bob will send you the payment of 0.05 BTC through yours and his payment channel. Here is the updated balance sheet between you and Bob:
{% include image.html url="/img/posts/payment2.png" description="Updated Balance sheet after Bob sends you BTC" %}

After Bob sends you BTC, you will send the coffee shop through the coffee shop's and yours payment channel. Here is the updated balance sheet after that: 
{% include image.html url="/img/posts/payment3.png" description="Completed Transaction" %}

At the end, Bob paid 0.05 BTC, you have the same balance of BTC from the start (0.095 BTC), and the coffee shop gained 0.05 BTC, and now has a total balance of 0.02 BTC.

Obiviously, this is just a really small example, but imagine that there are hundreds of nodes on this graph. You will be able to send Bitcoin to literally anyone on the Lightning Network as long as there is path between the sender and receiver. And yes, I know you are able to send a payment to anyone on the Bitcoin network, however, on the Lightning Network, the transactions are instant and cost little to nothing.

This is just one of the many applications of The Lightning Network. After listening to [BTC019: BITCOIN’S LAYER 2 LIGHTNING NETWORK WITH RYAN GENTRY](https://www.theinvestorspodcast.com/bitcoin-fundamentals/btc019-bitcoins-layer-2-lightning-network-w-ryan-gentry/) I was completely blown away. There are literally so many different applications that exist for the Lightning Network. (If you want to learn more about bitcoin, I would definitely recommending taking a look at Preston Pysh's Podcast [Bitcoin Fundamentals](https://www.theinvestorspodcast.com/bitcoin-fundamentals/). It is one of my favourite resources to learn even more about Bitcoin).

Here is a list of a few: 
- Messaging Apps: [Sphinx](https://sphinx.chat/)
- Stream Podcasts to a private RSS feed, and pay per second listening [Sphinx](https://sphinx.chat/)
- Purchasing Gift Cards
- Paid Reddit: [Y'alls](https://yalls.org/)
- Lightning Layer 3 (I was sooo shocked by Layer 2 applications, and so was Preston, that I do not even think they covered and Layer 3 Applications)
- Many many more

This podcast episode made me realize how little I actually know about Bitcoin, and the various different applications that are being built on top of it. It also makes me really excited about Bitcoin, I think it would be really cool to work on Layer 2 Bitcoin, or any other applications.
