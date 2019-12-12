---
title: 'What is Staking and How Much Does it Cost?' 
authors:
- richard
tags:
- Governance
- Proof of Stake
- PoS
categories:
- Blog
date: "2019-12-122T00:00:00Z"
lastmod: "2019-12-12T00:00:00Z"
featured: true
draft: false
toc: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Placement options: 1 = Full column width, 2 = Out-set, 3 = Screen-width
# Focal point options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
image:
  placement: 2
  caption: ''
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

This post considers "staking", the practice of using cryptographic coins or tokens to participate in some functional or governance role(s) within a decentralized (blockchain) production effort. The classic example is Proof of Stake (PoS) consensus, where token holders collectively perform the task of maintaining consensus and creating new blocks. This function is performed by Proof of Work miners in Bitcoin.

The term "staking" is now used much more broadly, including Delegated Proof of Stake systems and also hybrid forms. A number of companies now offer and promote "staking services" where they use custodied funds to participate in these processes and share some percentage of the rewards with their clients/depositors. Coinbase, Binance and Kraken all provide such services.

Staking means putting something of value at stake (like coins or tokens) as a kind of guarantee that one will participate in good faith and not try to abuse the system. As participants have skin in the game and would suffer from damage to the resource, they are incentivized to look after it - or at least the "tokenomics" have been designed this way.

The aim of this post is to characterize the type of "staking" that takes place in different projects by concisely answering a set of questions about it: 

* Does staking play a role in maintaining consensus?
* Does staking play a role in governance?
* Is staking incentivized?
* Can staking be delegated?
* What is the minimum requirement to participate in staking?

The project titles link to their crypto governance research profiles (where available), these profiles have more in depth information about the projects. 

## [EOS](/crypto-governance-research/overviews/eos)

DPoS smart contract platform

- Does staking play a role in maintaining consensus?

Indirectly, EOS uses Delegated Proof of Stake (DPoS). EOS holders vote to elect 21 [Block Producers](https://eosauthority.com/producers_rank) (BPs) and a number of standby BPs. These entities maintain consensus and produce new blocks.

- Does staking play a role in governance?

In principle, through [referendum polls](https://eosauthority.com/polls) which are intended to make decisions which should then be enacted by the BPs. EOS referendums have low turnout (< 3%) and most of the "approved" polls have yet to be put into practice by BPs.

Changing consensus rules requires the cooperation of 15 of the 21 active BPs. The active BPs have changed the rules in this way on a number of occasions

- Is staking incentivized?

Staking EOS to vote for BPs is not incentivized, but EOS can be staked to secure resources on the network.

The role of BP is incentivized with 1% annual inflation, with distribution weighted towards the active 21 BPs, although around 40 standby BPs also receive some rewards.

- Can staking be delegated?

Yes, EOS is a Delegated Proof of Stake system, so all of the voting power that elects BPs is delegated. Holders can delegate to themselves, but their EOS can vote for up to 21 BPs. Vote buying and trading between BPs was prohibited in the original EOS constitution, but this prohibition was lifted with the adoption of a "user agreement" which restricted itself to enforceable rules.

- What is the minimum requirement to participate in staking?

There is no minimum requirement to vote for BPs.

The minimum voting power required to be in the top 21 is **300,000 EOS votes (worth ~$1 million)**,
but the way voting power works means that it is much easier to rank highly with support from other BPs and holders. BPs that reach a certain threshold are paid at a lower rate as standby BPs, this is currently 
at **50,000 EOS votes ($180,000)**. 

BPs are required to maintain a powerful node that can handle a significant volume of traffic, this is enforced/checked for active BPs but not for standby BPs.

## TRON

DPoS smart contract platform

- *Does staking play a role in maintaining consensus?*

  Indirectly, TRON uses Delegated Proof of Stake (DPoS). TRX holders vote to elect representatives, there are 27 "[super representatives](https://developers.tron.network/docs/super-representatives-1)" and a further 100 "super partners".

- *Does staking play a role in governance?*

Governance does not involve TRX holders directly, it is the domain of super representatives.

- *Is staking incentivized?*

Yes, the super representatives and super partners are rewarded, it is [common](https://tronscan.org/#/sr/representatives) for them to share some of their rewards with delegators. 

- *Can staking be delegated?*

Yes, TRON is a Delegated Proof of Stake system, so all of the voting power that elects representatives is delegated. 

- *What is the minimum requirement to participate in staking?*

There is a fee of **9999 TRX ($140)** to register as a representative. The minimum voting power to be in the top 27 super representatives is **263k TRX ($3.7 million)**. The minimum voting power to be in the top 127 representatives is just **4,360 ($60)**, but these representatives will earn very little after redistributing ~80% of their rewards to their delegators. 

## [Tezos](/crypto-governance-research/overviews/tezos)

DPoS smart contract platform

- *Does staking play a role in maintaining consensus?*

Yes. XTZ holders with the minimum amount can participate in baking (block production), holders can also delegate their XTZ to a baker instead of participating directly.

- *Does staking play a role in governance?*

Yes. Bakers vote to decide which protocol upgrades are adopted.

- *Is staking incentivized?*

Yes. Bakers receive rewards from inflation, and most share some proportion with those who delegated XTZ to them.

- *Can staking be delegated?*

Yes. Most XTZ that participates in baking is delegated.

- *What is the minimum requirement to participate in staking?*

Minimum roll size to participate as an independent baker is **8,000 XTZ ($7,600)**. 

## Cosmos

DPoS connected blockchains

- *Does staking play a role in maintaining consensus?*

Indirectly. Cosmos uses Delegated Proof of Stake consensus and only the top 100 validators are active. 

- *Does staking play a role in governance?*

Yes. ATOM holders participate in voting on proposals, including signal voting on how to distribute a community fund and whether to adopt changes to consensus rules.

- *Is staking incentivized?*

Yes. Validators typically share rewards with their delegators (less a 2-20% commission).

- *Can staking be delegated?*

Yes.

- *What is the minimum requirement to participate in staking?*

The minimum number of ATOMs required to be one of the top 100 active validators is currently around **85,000 ($323,000)**. 

There is no minimum amount for delegation.

## [Maker](/crypto-governance-research/overviews/maker)

MKR tokens are ERC-20 tokens issued to holders by the Maker Foundation, holders use these tokens to govern the DAI/SAI stablecoins.

- *Does staking play a role in maintaining consensus?*

Not really. DAI lives on the Ethereum blockchain which is secured by Proof of Work consensus.

- *Does staking play a role in governance?*

MKR tokens vote to set the DAI/SAI stability fees and to implement other changes to the smart contracts that DAI/SAI run on. MKR tokens can also be used to participate in non-binding signalling polls. 

- *Is staking incentivized?*

No. When stability fees are paid they burn MKR tokens, reducing their supply, which MKR holders may expect to result in price appreciation.

- *Can staking be delegated?*

There is no formal method of delegating voting rights, and staking is not directly incentivized so there is little need for this. Coinbase allows its customers who hold MKR tokens to signal how they wish them to vote in executive polls. 

- *What is the minimum requirement to participate in staking?*

None

## [Dash](/crypto-governance-research/overviews/dash)

Proof of Service (Master Nodes) cryptocurrency. Although not Proof of Stake the collateral requirement to run master nodes is similar. 

- *Does staking play a role in maintaining consensus?*

Yes. As of July 2019, [Dash Chainlocks](https://www.dash.org/2019/07/02/dash-chainlocks-in-now-active/) give master nodes a role in maintaining consensus by locking in valid blocks as they are produced by Proof of Work miners and making reorg attacks more difficult.

- *Does staking play a role in governance?*

Yes. Master Nodes vote to decide which proposals will receive the Treasury's DASH, these votes occur monthly on chain. For consensus rules changing upgrades, Dash Master Nodes must upgrade their software to some threshold (specified by Dash Core Group) for the change to activate.

- *Is staking incentivized?*

Yes, Master Nodes share 45% of the block rewards, 45% go to PoW miners and 10% to the Treasury.

- *Can staking be delegated?*

Not without also granting custody of collateral funds to a "managed" master node provider. 

- *What is the minimum requirement to participate in staking?*

**1,000 DASH (~$60,000)** is required for collateral, and a server which is always online.

## [Decred](/crypto-governance-research/overviews/decred)

Hybrid PoW/PoS cryptocurrency.

- *Does staking play a role in maintaining consensus?*

Yes. DCR holders stake by time-locking their funds in exchange for [tickets](https://docs.decred.org/proof-of-stake/overview/). Every block [requires votes](https://docs.decred.org/governance/overview/#block-voting) from at least 3 of 5 pseudorandomly selected tickets. These votes determine whether the Proof of Work miner that produced the previous block receives their reward.

- *Does staking play a role in governance?*

Yes. Ticket holders vote to approve changes to the consensus rules on chain (75% supermajority requirement). Ticket holders also vote to decide how the project's Treasury funds should be spent, off chain on the Politeia [platform](https://proposals.decred.org/) (60% supermajority required).

- *Is staking incentivized?*

Yes. When tickets are called to vote on chain they share 30% of the reward for that block.

- *Can staking be delegated?*

Partially. Ticket-holders can delegate the act of making their vote to a voting service provider, which maintains voting infrastructure and relays votes from stakeholders. Ticket-holders specify how they want their tickets to vote on consensus rule change proposals, and even when using a VSP they vote directly on Politeia proposals from their wallet. 

- *What is the minimum requirement to participate in staking?*

The price for a single ticket is determined algorithmically, targeting a live ticket pool size of 40,960 tickets. The price for a ticket is currently around **130 DCR (~$2,600)**. Ticket-splitting software, which allows participation in a combined ticket purchase with others for a minimum **5 DCR ($100)** is in beta and being actively used by some community members. 

Stakeholders who do their own (solo) voting will incur some cost from maintaining online wallets, stakeholders who use a VSP pay a small fee (1-5% of the reward).

## Qtum

PoS based smart contract platform.

- *Does staking play a role in maintaining consensus?*

Yes. Qtum uses pure Proof of Stake consensus, specifically [version 3](https://blog.qtum.org/qtums-utxo-design-decision-d3cb415a3a6e) of a Proof of Stake implementation for UTXO based blockchains like Bitcoin.

- *Does staking play a role in governance?*

Minimally. PoS participants in Qtum vote to set parameters like maximum block size. Hard fork changes to the consensus rules are released in software updates with specified activation blocks, PoS nodes that do not update in time are forked off the network.

- *Is staking incentivized?*

Yes.

- *Can staking be delegated?*

No.

- *What is the minimum requirement to participate in staking?*

There is no technical minimum, but wallets with little QTUM will be selected very infrequently. Participation requires maintenance of an online wallet at all times, which has associated costs. This [resource](https://medium.com/coinmonks/getting-started-with-qtum-staking-for-advanced-users-qtumd-qtum-cli-node-wallet-b076a2ccfb64) puts the minimum to stake without making a loss at **160 QTUM ($368)**. 

## Algorand

Pure Proof of Stake (PPoS) smart contract platform

- *Does staking play a role in maintaining consensus?*

Yes, Algorand uses Proof of Stake consensus whereby participating nodes are selected probabilistically based on the number of "algos" they hold.

- *Does staking play a role in governance?*

Algorand governance is dominated by the [Algorand Foundation](https://algorand.foundation/governance), which also retains a sizeable share (25%) of the network's entirely [pre-mined supply of algos](https://algorand.foundation/token-dynamics), with another 30% of these being distributed over time in auctions (proceeds presumably going to the Foundation).

> The Algorand Public Blockchain seeks to have a constitution and long term governance structure designed with community involvement. More details on our constitutional assembly and governance policies/processes will be shared soon.
>
> At launch, governance of the network is assisted by the Algorand Foundation's Economic and Technical Advisory Committees, with committee members selected by our University & Non-Profit Program participants.

- *Is staking incentivized?*

Yes. 17.5% of the supply is reserved for rewarding participants in PoS consensus. A further 25% is reserved for rewarding "relay nodes" which do the work of processing transactions.

- *Can staking be delegated?*

No.

- *What is the minimum requirement to participate in staking?*

The minimum amount of algos required to register to [participate in staking](https://algorand.foundation/stakingrewards) was **25 ($5)** for the first round of registrations, but participants must register and **complete KYC/AML** processes before they can receive rewards. This means that participation in Algorand PPoS is not permissionless.

## Lisk

DPoS smart contract platform

- *Does staking play a role in maintaining consensus?*

Indirectly. LSK holders can vote to elect 101 delegates, these delegates maintain consensus and create new blocks. 

- *Does staking play a role in governance?*

Indirectly. Lisk's voting system has been notable for its dominance by cartels, and it is set to to be [upgraded](https://lisk.io/blog/research/3-new-dpos-lips-changing-voting-system-lisk). 

- *Is staking incentivized?*

Yes. The List [Elite](https://liskelite.com/) and [GDT](https://pool.liskgdt.net/#home2) [cartels](https://medium.com/coinmonks/lisk-the-mafia-blockchain-47248915ae2f) share a portion of their rewards with voters who delegate to all of their members.

- *Can staking be delegated?*

Yes all Lisk staking is delegated, in true DPoS fashion.

- *What is the minimum requirement to participate in staking?*

LSK holders [can vote](https://www.reddit.com/r/Lisk/comments/6wsb9x/voting_explained/) for up to 101 delegates, but **each vote costs 1 LSK (~$.070)** and only 33 delegates can be voted for each time, so to use **full voting power requires 4 votes costing 1 LSK each**. Every time votes are changed this costs another 1 LSK, so there is incentive to set and forget. Rewards shared are proportional to total holdings, so it may take a long time for small LSK holders to earn back the cost of their votes.