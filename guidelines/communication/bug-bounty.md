## Program Overview
The Bug Bounty Program is to find vulnerabilities in the ICON network. The greater the risk of the vulnerabilities, the greater the reward will be sent to those who discover the vulnerabilities. This will lead whitehats to report them to ICON, instead of taking advantage of the bug. It will start with ICON Mainnet and will expand to other applications.
Bug reporters can register bug reports in Immunefi 
https://immunefi.com/bounty/icon/

## Rewards by Threat Level
Rewards are distributed according to the impact of the vulnerability based on the Immunefi Vulnerability Severity Classification System V2.2, focusing on the impact of the vulnerability reported.

All High and Critical Blockchain/DLT and Smart Contract bug reports require a Proof of Concept (PoC) to be eligible for a reward. Explanations and statements are not accepted as PoC and code is required.

ICON requires KYC to be done for all bug bounty hunters submitting a report and wanting a reward. If the entity is an individual, the information needed are Name, Address, Nationality, Birthday, copy of ID card, copy of residence certificate, criminal records and personal relations with politicians. If the entity is a company, business start date, address, country the business base on, copy of business certificate. And some information about people who have over 20% of the company's share. The collection of this information will be done by the ICON project team.

Payouts are handled by the ICON team directly and are denominated in USD. However, payouts are done in ICX. If the reporter disagree with the KYC requirement or you are denied by the KYC process, payouts cannot be done.

Blockchain/DLT

| Severity | Payout       | PoC |
| --------- | -------------- | ----- |
|Critical | USD $100,000 | PoC Required |
|High     |USD $25,000   | PoC Required |
|Medium   |USD $5,000    |              |
|Low      |USD $1,000    |              |



## Impacts in scope
Only the following impacts are accepted within this bug bounty program. All other impacts are not considered as in-scope, even if they affect something in the assets in scope table.

Blockchain/DLT
| Critical |
| -------- |
|Network not being able to confirm new transactions (Total network shutdown)|
|Unintended permanent chain split requiring hard fork (Network partition requiring hard fork) |
|Direct loss of funds |
|Permanent freezing of funds (fix requires hardfork) |
|RPC API crash |
|Arbitrary transaction affecting ICON ledger |
|Change block data which is already finalised |
|Arbitrary smart contract (Score) call, updating or deleting Score without permission |
|Inconsistent data in partitioned blockchain |



| High |
| -------- |
|Unintended chain split (Network partition) |
|Transient consensus failures |
|Disability to make a new block(no consensus working) |
|Newly created block never comes to the finality |



| Medium |
| -------- |
|High compute consumption by validator/mining nodes |
|Attacks against thin clients |
|DoS of greater than 30% of validator or miner nodes and does not shut down the network |
|Attacking single node to shut down |
|Stopping a node from working properly |



| Low |
| -------- |
|DoS of greater than 10% but less than 30% of validator or miner nodes and does not shut down the network |
|Underpricing transaction fees relative to computation time | 
|Trivial minor bugs except the one related to consensus, safety, liveness, consistency |



