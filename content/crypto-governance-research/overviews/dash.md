---
title: Dash
linktitle: Dash
toc: true
type: docs
date: "2019-09-24T00:00:00+01:00"
draft: false
menu:
  overviews:
    parent: Governance Overviews
    weight: 1

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---
## Where does the governance happen?

Treasury governance happens on chain, with monthly superblock votes to determine which proposals receive that month's funding. [Dash Central](https://www.dashcentral.org/) is a well established place to view and discuss proposals. [Dash Nexus](https://app.dashnexus.org/proposals/leaderboard) and [Dash Ninja](https://www.dashninja.pl/) also show proposal voting data (along with a variety of other information about the network).

Decisions about the consensus rules and the network's core functionality are made internally at Dash Core Group. DCG is given considerable freedom to propose upgrades. The master node operators have a degree of control over DCG through a legal entity and control of funding, but so far have yet to challenge any decisions made by DCG.

# Blockchain Governance

## Consensus

Making changes to Dash's consensus rules is governed in a similar way to Bitcoin and pure PoW currencies. It is an ad hoc process in which some arbitrary signalling criteria are set (i.e. % of miners and masternodes upgrade/signal) and this initiates a lock-in process. A recent (Feb 2019) example of this is the adoption of [DIP0003](https://github.com/dashpay/dips/blob/master/dip-0003.md), where the signalling threshold of v0.13.0 was relaxed after one month by a new release (v0.13.1), because the it was proving [too difficult](https://blog.dash.org/dash-core-v0-13-1-release-5d6e06031ba3) to meet the original threshold.

Masternodes have held signalling votes to approve changes to the consensus rules ([example](https://www.dashcentral.org/p/2mb-blocksize), block size increase vote) but the mechanism through which upgrades are adopted relies on consensus among both miners and masternodes.

## Blockchain Governance

* *Does the project have its own blockchain or is it a token on another chain? (many questions are not relevant for tokens)*

Dash's blockchain mainnet launched in January 2014 as [Xcoin](https://dashpay.atlassian.net/wiki/spaces/OC/pages/19759164/Dash+Instamine+Issue+Clarification), it was soon [re-branded](https://bitcoinmagazine.com/articles/battle-privacycoins-why-dash-not-really-private/) to Darkcoin and then again to Dash in early 2015. 

* *What is the mechanism for ensuring consensus about the state of the blockchain?*

Dash's consensus mechanism has a role for Proof of Work miners (HASH) and also Master Nodes (termed "Proof of Service"). 

* *Which entities interact with the blockchain? What role does each entity play? How are the "block producers" selected?*

Proof of Work miners compete to find the solution to an arbitrary problem that can only be found by guessing (hashing). Dash uses the [X11 hash algorithm](https://docs.dash.org/en/stable/introduction/features.html#x11-hash-algorithm). When a PoW miner finds a valid solution they create a block and broadcast it to the network.

Master Nodes are nodes which must meet certain requirements. Master Nodes must have 1)1000 Dash and 2) a server meeting certain specifications.

In July 2019 the way that master nodes and PoW miners interact to produce the blockchain changed significantly, with the introduction of [Long Living Masternode Quorums (LLMQs) and ChainLocks](https://blog.dash.org/mitigating-51-attacks-with-llmq-based-chainlocks-7266aa648ec9). 



[Role of masternodes](https://docs.dash.org/en/stable/masternodes/understanding.html#masternodes-vs-mining):

> The masternode system is referred to as Proof of Service (PoSe), since the masternodes provide crucial services to the network. In fact, the entire network is overseen by the masternodes, which have the power to reject improperly formed blocks from miners. If a miner tried to take the entire block reward for themselves or tried to run an old version of the Dash software, the masternode network would orphan that block, and it would not be added to the blockchain.

> Masternode payments in Dash version 0.13.0 are entirely deterministic and based on a simple list sort algorithm. 

> InstantSend transactions in Dash version 0.13.0 are secured using a consensus of deterministically selected masternodes. This set of masternodes is informally termed a quorum and must be in a majority agreement, at least six out of ten, for a successful lock of the transaction inputs. Multiple quorums are self-selected for each input in an InstantSend transaction using the mathematical distance between the hash of each input and of the set of masternode funding transactions.

Once a pending new version (v0.13.1) has been adopted [widely enough](https://blog.dash.org/dash-core-v0-13-1-release-5d6e06031ba3) to activate, MN quorums  will be selected deterministically through an on-chain mechanism.  https://github.com/dashpay/dips/blob/master/dip-0003.md

Chainlocks coming some time: https://blog.dash.org/mitigating-51-attacks-with-llmq-based-chainlocks-7266aa648ec9

PoW Miners make blocks, one MN is selected (deterministically) in each block approve it and insert instantsend and privatesend transactions

* *How were/are coins distributed? Was there an ICO? Is there inflation now? Is there a fixed supply?*

Dash block rewards are divided between Miners (45%), Masternodes (45%) and a Treasury (10%).

There is a controversy in Dash's history around an "instamine bug" which allowed large quantities of DASH to be mined in the first days of the network - likely mined largely by the developers. There are many relevant sources for this, here are two that represent each "side":

* [bitcointalk post from 2015 where the launch was discussed in detail](https://bitcointalk.org/index.php?topic=1043923.0)
* ["official reponse" to the instamine from Dash Core Group](https://dashpay.atlassian.net/wiki/spaces/OC/pages/19759164/Dash+Instamine+Issue+Clarification)

All parties agree that: much more DASH was mined in the first 48 hours after the chain launched than was intended - 2 million DASH were minted during this time, around 10% of the total supply that will ever be issued. 

## Funding

A key aspect of Dash's governance, deciding which proposals are funded by the Treasury, happens [on-chain](https://docs.dash.org/en/stable/governance/understanding.html). Treasury DASH is distributed in monthly superblocks which occur every 16616 blocks or approximately 30.29 days. Masternodes can each vote Yes or No on each proposal. There is a fee of 5 

For a proposal to be funded it must satisfy the condition: `(YES votes - NO votes) > (Total Number of Masternodes / 10)`, but as there is a limited amount of DASH available in each superblock the ranking of proposals (by net Yes - No votes) is more important. When the superblock occurs, proposals that satisfy the criteria are paid out in order of their score, once the available DASH has been paid out remaining proposals will not be funded. In a scenario where there is a surplus of DASH in a superblock (the proposals which meet the voting criteria collectively requested less than the available amount), the remaining DASH is burned or not created. 

The footprint of a Dash proposal on the blockchain is pretty minimal (short title, wallet address of owner, proposal amount and duration), but this is supported by a number of off-chain sites which present further information. 

[Dash Central](https://www.dashcentral.org/) is probably the main site for discussing proposals, and it has tools which support proposal submission and voting by masternodes.

[Dash Nexus](https://app.dashnexus.org/proposals/leaderboard) provides a list of current proposals and some information about how Treasury funds are being spent. 

[Dash Ninja](https://www.dashninja.pl/) provides masternode monitoring and analytics. 

dashvotetracker used to be the go to resource for proposal voting data, but it has been replaced by Dash Nexus. Dash Nexus does not provide a historical list of proposals, but that information can still be found on [dashvotetracker](http://dashvotetracker.com/past.php).

Prospective proposal submitters are encouraged to submit a pre-proposal on the Dash [Forum](https://www.dash.org/forum/topic/pre-budget-proposal-discussions.93/), and discuss it on their Discord. 

[Dashboost](https://www.dashboost.org/proposals) is an initiative for funding small-budget proposals, with its own DASH-voting system to choose what gets funded.



- *What is the reference node implementation?*

[Dash](https://github.com/dashpay/dash) 

- *Any other full node implementations?*

No

Block reward - Dash Core Group is a corporation which has been funded by Treasury superblocks since September 2015.

![Dash core funding over time](/img/dash-core-funding-over-time.png )

Image above taken from this article, looking at the proportion of Treasury DASH going to proposals from Dash Core Group. In the depressed market conditions of 2018, Dash Core Group's share of the overall Treasury budget has increased significantly. For March 2019 Core Group is requesting 60% of the superblock Dash, for core team [compensation](https://app.dashnexus.org/proposals/1d944a8a-d033-4825-ad9c-50a9815f073f/overview) and [business development](https://app.dashnexus.org/proposals/de7250ad-7047-4ea6-a371-b500a64678cf/overview).

**What other software does the entity(ies) which funds the reference node produce?** 

Dash Core Group has been working on "[Dash Evolution](https://www.dash.org/evolution/)" for quite some time. This is planned to be a comprehensive advance in the usability of Dash.

Through the Treasury, a wide range of integrations and other smaller-scale projects have also been funded.

**What else do the entities which develop or fund the reference node do? (not software)**

![Dash core funding over time](/img/dash-treasury-funding-by-category.png )

This chart shows a categorical breakdown of what Treasury Dash (and in USD equivalent) had been spent on up until January 2018 (from this [article](https://medium.com/@richardred/observations-of-the-dash-treasury-dao-c94231b2b5c4)). During times when the DASH price was high, significant DASH was spent on marketing activities like advertisements and sponsorships.

## Proposals and Voting

![Dash treasury proposals participation](/img/dash-proposals-participation.png)

For the first 758 Treasury proposals (August 2015 - April 2019) mean master node participation in voting [was around 19%](https://github.com/RichardRed0x/crypto-governance-research/tree/master/governance-proposals).

### Further reading

Docs - https://docs.dash.org/en/stable/

IOHK published a [paper](https://iohk.io/research/papers/#dash-governance-system-analysis-and-suggestions-for-improvement) about Dash's governance system in 2016

Richard Red has written two articles about aspects of Dash's Treasury governance:

* [Observations of the Dash Treasury DAO](https://medium.com/@richardred/observations-of-the-dash-treasury-dao-c94231b2b5c4)
* [Decentralized autonomous funding of blockchain projects](https://medium.com/@richardred/decentralized-autonomous-funding-of-blockchain-projects-3c0c233ae4ad)

### Related projects

Dash software was originally forked from Bitcoin Core v0.12

Dash has itself been forked many times, and the masternode concept has been extensively [copied](https://masternodes.online/). One notable fork of Dash is PIVX, which replaces PoW with PoS.

### Significant Entities

[Dash Core Group](https://www.dash.org/team/), a for-profit entity which is responsible for core development 

From [March budget proposal](https://app.dashnexus.org/proposals/1d944a8a-d033-4825-ad9c-50a9815f073f/overview):

> In March, DCG will have 43 staff associated with the project.  The breakdown of the number of staff we have working in each unit will be as follows:
> **Development and Operations:**
> Full-time: 26
> Part-time: 6
>
> **Admin / business development / marketing / customer service:**
> Full-time: 10
> Part-time: 1
>
> \*  Full-time defined as contracts permitting staff to bill up to 40 hours a week
> ** Part-time defined as contracts permitting staff to bill less than 40 hours a week
>
> Our run-rate in March will be $250,000 after taking into account voluntary pay reductions, recent resignations and the non-renewal or cancellation of certain contracts.

Dash Core Group is now [owned](https://dashnews.org/dash-core-group-becomes-first-legally-dao-owned-entity/) by the masternodes DAO entity.

[The Dash DAO Irrevocable Trust](https://www.dash.org/2018/08/02/legal.html) : a Trust established in New Zealand which owns all shares in Dash Core Group and has the responsibility to step in and fix things if the masternodes de-fund Dash Core Group.

> The initial trust protectors are a subset of the DCG board, as we needed an initial body to establish the trust. This is temporary and will no longer be the case after the first proper election early next year. The initial trust protectors are Philipp Engelhorn, Andy Freer, Fernando Gutierrez, Holger Schinzel, Ryan Taylor, and Robert Wieko.

[Dash Labs](https://www.dash.org/2017/07/05/Dash-Labs.html): Evan Duffield, Dash founder, stepped away from the Core team in early 2017 to pursue research on masternode hardware. This organization is self-funded by Duffield.

[Dash Force](https://dashnews.org/about-the-dash-force/): The first dash force [proposal](https://www.dashcentral.org/p/Dash_Force_Reloaded) was funded in January 2017. To start with it was geared towards boosting social media engagement, but since then it has expanded to run the [Dash News](https://dashnews.org/) website. 

# Significant Events

### Feb 2019

Dash v0.13.1 was released on Feb 8 to "accelerate adoption of the Dash Core v0.13". Dash Core [v0.13](https://blog.dash.org/dash-core-v0-13-on-mainnet-dc9609b0f6f9) was intended to activate [DIP3](https://github.com/dashpay/dips/blob/master/dip-0003.md) but it had an activation threshold of 80% blocks signalling support from the PoW miners and masternodes in a 7 day window before activation would begin. After failing to meet these criteria for around 24 days, it was decided that the criteria are too stringent and that the requirement for masternodes to signal could be dropped. When enough PoW miners have adopted v0.13.1 the change will activate one week later, any masternodes who fail to upgrade by then will cease to receive rewards. 

### Mar 2019

Dash held an [election](https://blog.dash.org/announcing-the-dash-dao-irrevocable-trust-election-results-bfe134c113b0) for Trust Protectors, people who will oversee the operation of a legal trust that has been [set up](https://blog.dash.org/dash-network-elected-trust-protectors-closing-the-governance-loop-4f07b46da03e) to own and control Dash Core Group.

Dash also [finished](https://blog.dash.org/deterministic-masternode-list-and-automatic-instantsend-now-live-f2028d833388) the deployment of the Deterministic Masternode List, enabling automatic instant payments for transactions with fewer than 4 inputs.

Dash Core Group further [tightened](https://www.theblockcrypto.com/2019/03/04/corporation-behind-dash-lays-off-senior-staff-as-bear-market-grip-tightens/) its budget with layoffs and salary freezes.

### Apr 2019

The Dash sporking upgrade process [completed](https://blog.dash.org/product-update-april-5-2019-71344591a5e1) to enable Deterministic Masternode List (which is a requirement for chain locks that will deter PoW majority attacks) and Auto InstantSend. The activation of this spork caused Treasury proposal votes to be reset, and for most of the month it looked as though only a few proposals would reach the required level of votes to be funded. When superblock voting closed on Apr 29 voter participation rates were back to within their normal range and 15 proposals met the requirement. 660 DASH remained to be spent in the superblock, and is now lost to the Dash Treasury, but this level of underspend is not particularly uncommon. Among the [proposals](https://github.com/RichardRed0x/crypto-governance-research/blob/master/governance-proposals/dash-proposals.csv) were two from rival PR firms, Wachsman and Shift; until this point Dash Core Group had arranged such services directly at their discretion, and had been retaining the services of Wachsman. The Shift proposal, costing $10K per month as a retainer, passed with 536 Yes votes (90% Yes, but only 52 votes over the quorum requirement), while the Wachsman proposal was rejected with a score of -206 (more No votes than Yes votes).

### May 2019

Dash [Ventures](https://blog.dash.org/introducing-the-dash-investment-foundation-370cafcc48ee) investment foundation is nearing completion, and Dash will be holding an election to select a set of supervisors to oversee its operation. The Dash Investment Foundation will be able to take ownership of equity or other assets in consideration for network funding. The election to fill the remaining 4 of 6 supervisor seats [started](https://blog.dash.org/details-on-the-election-for-dash-investment-foundation-supervisors-25766c55a1f) on May 30, and will be followed by budgetary proposals to fund the foundation's administrative costs and allocate some capital for it to invest.

### Jul 2019

Dash [completed](https://blog.dash.org/the-dash-investment-foundation-supervisor-election-results-96a28309744b) the first annual elections for positions as supervisors of the Dash Investment Foundation, using some software custom [made](https://blog.dash.org/trust-protector-election-software-93ed67c7455b) for this purpose.

### Aug 2019

A CoinDesk [article](https://www.coindesk.com/despite-ceo-claims-dash-isnt-really-the-most-used-crypto-in-venezuela) explored the reality of Dash adoption in Venezuela, suggesting that it was not being used as widely as claimed by some Dash representatives, and that some of the programs to promote adoption among merchants were ineffective.

