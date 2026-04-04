---
title: Quick Start
slug: 2a05bab0c2cc811c895ac488d3baece9
sidebar_position: 1
---


# Quick Start

# Overview

Cryptocurrency withdrawal refers to the process of transferring cryptocurrency (such as BTC, ETH, USDT, etc.) from a personal digital wallet or trading platform account to another address (including other wallets or other trading platform accounts). If conversion to fiat currency is required, the client must first complete a sell transaction on a trading platform before withdrawing the corresponding fiat amount to a bank account. This guide focuses on the direct cryptocurrency transfer scenario.

<b>Operation process: </b>The client initiates a withdrawal through the app by entering the recipient address and transfer amount. Once the request has passed platform review (including WBO work order approval) and received the required number of blockchain confirmations, the asset transfer is complete.

# Quick Start

## Prerequisite

Operators must obtain the following permissions before they can use the system functions properly.

## Cryptocurrency Service Fee Reserve on HashKey

When initiating a cryptocurrency withdrawal operation on the HashKey platform, operators must be aware of the service fee deduction rules and account fund reserve requirements, as detailed below:

1. <b>Service fee deduction accounts</b>

The blockchain network service fee (e.g., miner fee) incurred during a cryptocurrency withdrawal is deducted from the main account, while the withdrawal principal is deducted from the tenant's sub-account. These two deductions are independent of each other. If the sub-account holds sufficient principal but the main account has no available balance to cover the service fee, the withdrawal will fail.

1. <b>Main account fund reserve requirements</b>

To ensure that withdrawals are processed successfully, the tenant must maintain a reserve of the relevant cryptocurrency in the main account before initiating a withdrawal (for example, a small amount of BTC for a BTC withdrawal, or USDT for a USDT withdrawal). The reserve must be sufficient to cover the estimated service fee for the transaction, which can be viewed on the withdrawal page in real time.

1. <b>Common issues</b>

If a "Main account service fee insufficient" error appears during a withdrawal, the client should either deposit the relevant cryptocurrency into the main account, or transfer a small amount from the sub-account to the main account as a service fee reserve. The withdrawal application can then be resubmitted.

<img src="/assets/TyC0wfeVwhvjqMbX1YojKi5Vpoe-board.jpeg"/>

## Cryptocurrency Configuration

Operators should configure cryptocurrency settings for withdrawals before processing client withdrawals.

<img src="/assets/XCWZbBM2ioDNPTxN9DVjQSXLpQh.png" src-width="2474" src-height="1188" align="center"/>

# Client Wallet Address

To ensure asset security, wallet address verification must be completed before a withdrawal is processed. This is a critical prerequisite step.

<img src="/assets/MsepbKsJKo7Dsjx9Fhbjvs0dpLr.png" src-width="2440" src-height="1164" align="center"/>

## Processing Withdrawal Applications

If the client has submitted a withdrawal application in the app, the record will be automatically displayed on this page.

Withdrawal applications submitted by clients are automatically linked to the WBO work order system (work order ID: atm.va.coin_withdraw_apply). The system will conduct the approval process based on the pre-configured approval workflow.

<img src="/assets/NmyObhgk1ohCjPx8oH5jCTlUpcb.png" src-width="2468" src-height="602" align="center"/>

