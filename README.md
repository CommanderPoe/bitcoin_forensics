### Bitcoin_Forensics

##### Tracing malicious (or any kind of) transactions on the bitcoin's blockchain and vizualise them.
___

<!---![bitcoin is a massive honeypot](https://github.com/CommanderPoe/bitcoin_forensics/blob/main/presentation/vids/iu-2.jpeg) --->
<img src="https://github.com/CommanderPoe/bitcoin_forensics/blob/main/presentation/vids/iu-2.jpeg">  
<!--- width=50% height=50%--->
<br />

#### What is Bitcoin and how it works... ₿

Bitcoin is a peer-to-peer electronic cash system that allows you to send money anywhere in the world without anyone stopping you.

No amount is too small or too large. Apart from this, it is a very scarce asset. It is also the most robust and unique fundamentally decentralized settlement layer/protocol ever created for money that has worked unstoppably for over ten years.

[*These guys at Upfolio*](https://www.upfolio.com/ultimate-bitcoin-guide) will do a much better job than I ever will explaining what is bitcoin and how it works for dummies.
___
<br />

#### The goal... ₿
Bitcoin is pseudo-anonymous, not anonymous; hence it is relatively simple to find patterns in on-chain data. One transaction can take you to the next one and so on forever. The Blockchain is what Bitcoin uses to prevent the '[*double spend problem*](https://river.com/learn/what-is-the-double-spend-problem/)' from ever happening. 

Once a bitcoin changes hands, the transaction becomes an official Blockchain entry that’s automatically and permanently recorded, so the money can’t be spent twice. **(Huge)** Problem solved!

**The goal** of this small project is to connect one address to another just like [*bitcoin's explorers*](https://blockstream.info) do but showing the whole history in string format but also visually, so the unexperience user wont have to deal with the in/outs of the most needed blockchain explorers.
<br />

*Here's how the output in string format looks like in raw.*
<img src="https://github.com/CommanderPoe/bitcoin_forensics/blob/main/presentation/vids/output.png"> 

*Here's how the output looks visually after using [*gephi*](https://gephi.org).
<img src="https://github.com/CommanderPoe/bitcoin_forensics/blob/main/presentation/vids/tx_visualization.png">.*
<br />

#### The process... ₿


#### Video of the MVP... ₿


#### Things to improve... ₿
- [ ] Better way to represent the data (output) in string format.
- [ ] Improve skills of gephi, software offers unlimited posibilities for this project.
- [ ] Try to extract the data (transaction history) from own node using the python API instead of using Google's BigQuery.
- [ ] Explore and scrape several websites for 'abused addresses' and create a small database of all malicious transactions.
- [ ] Use more data.

