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

[*These guys at Upfolio*](https://www.upfolio.com/ultimate-bitcoin-guide) will do a much better job than I ever will at explaining bitcoin and how it works for dummies.
___
<br />

#### The goal... ₿
Bitcoin is pseudo-anonymous, not anonymous; hence it is relatively simple to find patterns in on-chain data. One transaction can take you to the next one and so on forever. The Blockchain is what Bitcoin uses to prevent the '[*double spend problem*](https://river.com/learn/what-is-the-double-spend-problem/)' from ever happening. 

Once a bitcoin changes hands, the transaction becomes an official Blockchain entry that’s automatically and permanently recorded, so the money can’t be spent twice. **(Huge)** Problem solved!

**This small project aims** to connect one address to another just like [*bitcoin's explorers*](https://blockstream.info) do but showing the whole history in string format and visually, so the inexperienced user won't have to deal with the in/outs of the most needed blockchain explorers.
<br />

*Here's how the output in string format looks like in raw.*
<img src="https://github.com/CommanderPoe/bitcoin_forensics/blob/main/presentation/vids/output.png"> 

*Here's how the output looks visually after using [*gephi*](https://gephi.org).
<img src="https://github.com/CommanderPoe/bitcoin_forensics/blob/main/presentation/vids/tx_visualization.png">*
___
<br />

#### The process... ₿
1. [Notebook #1](https://github.com/CommanderPoe/bitcoin_forensics/blob/main/notebooks/01_Querying%20the%20data.ipynb)
   Query data from the Bitcoin blockchain to extract a few on-chain insights. To do so, I used [Google's BigQuery Bitcoin Database](https://cloud.google.com/blog/topics/public-datasets/bitcoin-in-bigquery-blockchain-analytics-on-public-data).

    Since each query was massive (**~1.5 TB**) and google's monthly quota is only 5TB, I ran into much trouble getting the proper amount of data to achieve my goal.

    For this reason, I ended up only with just a few hundred blocks (**449**) which translates into three days of data and **~900.000** transactions. These couple of days of tx size in memory was around 4GB.
<br />

2. [Notebook #2](https://github.com/CommanderPoe/bitcoin_forensics/blob/main/notebooks/02_Bitcoinabuse%20Webscraping.ipynb)
    For this step, I decided to scrape [bitcoinabuse.com](https://www.bitcoinabuse.com), which tracks bitcoin addresses used by ransomware, blackmailers, fraudsters, etc.

    I scraped the whole website and ended up with almost three years of abused addresses. 
<br />

3. [Notebook #3](https://github.com/CommanderPoe/bitcoin_forensics/blob/main/notebooks/03_Data%20Cleaning%20%26%20EDA.ipynb)
    Now that I had interesting addresses to explore I started cleaning the data and doing some exploratory analysis. I was so focused on building a final product that I missed some really cool insights about daily tx regarding fees, amount sent/received, # of inputs/outputs ect...
 <br />

4. [Notebook #4](http://localhost:8888/notebooks/Desktop/IRONHACK%20BOOTCAMP/Final%20Project/bitcoin-forensics/notebooks/04_Minimun%20Viable%20Product%20.ipynb)
    Final script was developed in this step and combined with several libraries to graph/map the conection between the adresses in-situ called `graphviz` and once it was all working I started using a 3rd party software called **Gephi** which is the leading visualization and exploration software for all kinds of graphs and networks. Gephi is open-source and free. Steps to follow for the user:
    - Inputs the address or tx id to be checked.
    - The system checks if the given input (address) matches any of the outputs column (addresses).
    - If it finds any, it will go back to the inputs column and repeat the process again and again till there’s no more connection btween the given address and the outputs.
___
<br />

#### Video of the MVP... ₿

https://user-images.githubusercontent.com/33594578/120248096-18076780-c276-11eb-9fef-cf1a3eb9054e.mp4


<br />

#### Things to improve... ₿
- [ ] Better way to represent the data (output) in string format.
- [ ] Improve skills of gephi, software offers unlimited posibilities for this project.
- [ ] Try to extract the data (transaction history) from own node using the python API instead of using Google's BigQuery.
- [ ] Explore and scrape several websites for 'abused addresses' and create a small database of all malicious transactions.
- [ ] Use more data.
- [ ] TODO a deeper exploratory analysis on the bitcoin's blockchain, there's a world to be discovered there inside.
- [ ] Give the user to input not only an address but also a tx id or a hash.

