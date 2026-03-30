---
title: System Introduction
slug: T15Awmt9Vi8QbCk5nJcjUpXRp9c
sidebar_position: 1
---


# | 原文 | 英文翻译 |
|---:|---|
| 系統介紹 | System Introduction |

# System Introduction

The Activity System is the core marketing campaign management component provided by the Whale OPA operations system. It enables broker tenants to manage various marketing campaigns, offering configuration and management capabilities for multiple campaign elements. The system currently supports the following campaign type groups:

- Standard campaign types: invitation campaigns, basic campaigns, team campaigns, etc.
- Non-standard campaign management: provides customizable campaign elements to facilitate the arrangement of bespoke campaigns.

Manage a variety of marketing campaigns through convenient campaign templates to achieve digital marketing.

<img src="/assets/KVmEbr0nzoboJbxDspxjer1spDh.jpeg" src-width="1276" src-height="920" align="center"/>

## 1. Features

### 1.1 Campaign System Architecture

<img src="/assets/LOlEbPocioJV6Px4q6ZjQ9zFplr.jpeg" src-width="806" src-height="492" align="center"/>

### 1.2 Task Types for Campaign Qualification and Descriptions

### 1.3 Campaign Reward Types

When creating a campaign, three reward types may be configured: physical goods, vouchers, and cash.

Refer to the Benefits System documentation for physical goods and voucher creation.

### 1.4 Campaign Configuration Workflow

Applicable users: Operations personnel. The campaign system involves the following entities:

- Campaign System: Operations personnel are responsible for configuring and managing online campaigns.
- User Segmentation: Defines target users and retrieves asset-related data during the campaign.
- Benefits System: Associates relevant campaign rewards.

<img src="/assets/KGNobb5VTo588TxQ6sRjOTM8pMf.jpeg" src-width="2190" src-height="894" align="center"/>

## 2. Standard Campaign Management

Navigation: Operations System &gt; Campaign System &gt; Standard Campaign Management

This function maintains and manages standard campaigns.

Upper layer: choose a campaign template to create a campaign.

Lower layer: query and manage records of created campaigns.

<img src="/assets/GEuEbUP6doZaW9x3edTj90eMpTe.jpeg" src-width="3766" src-height="1562" align="center"/>

Campaign management list field descriptions

### 2.1 Invitation Campaigns

#### 2.1.1 Invitation Campaign Business Logic

If any campaign page enables the share feature, then new user registrations resulting from user sharing will bind invitation relationships.

Invitation campaigns award based on these binding relationships.

<img src="/assets/QNvgbgICXoN40VxSyLsjvdqfpLU.jpeg" src-width="1474" src-height="494" align="center"/>

Invitation campaigns support two reward types: fixed rewards and tiered rewards.

Fixed reward: For each invited new user who completes the task, the inviter receives a fixed reward.

Tiered reward: Divide the number of invitees into ranges. For invite counts within a given range, the inviter receives the reward corresponding to that range for each successful invitation. Upon reaching the next range, the inviter can receive an additional bonus. Typically, the more invites, the larger the rewards.

#### 2.1.2 Invitation Campaign Configuration

Operations System &gt; Campaign System &gt; Standard Campaign

To create a new invitation campaign, click the "New" button under the Invitation Campaign module.

<img src="/assets/QbwdbiotxoliMpxV4D9jSRfrpRd.jpeg" src-width="1280" src-height="199" align="center"/>

The invitation campaign creation page is as follows:

<img src="/assets/YN2Ubte3Lotvh9x6EZujssqCpDc.jpeg" src-width="2108" src-height="1941" align="center"/>

Configure template fields according to the following rules:

Reward Rules

Click "Add Reward Rule". The fields vary by reward type and campaign attribute:

Fixed Reward

<img src="/assets/TXPRbFcHVode9yxOWXbjriPQpdh.jpeg" src-width="1280" src-height="980" align="center"/>

Tiered Reward

<img src="/assets/JTjZbCqSfoJQ5FxkEyQjwXYgpeg.jpeg" src-width="1280" src-height="958" align="center"/>

Prize Settings

Click "New Prize Rule" to reveal configuration items:

Set limits on how many times a user can receive specific prizes under the reward rules.

<img src="/assets/W8HxbPV4VoMTxqxahI7jZoP5pgc.jpeg" src-width="2040" src-height="386" align="center"/>

#### 2.1.3 Invitation Campaign Reward Data Query

Data is available only while the campaign is running and rewards are being distributed.

Click the details button for the relevant campaign, then open the "Winners" tab to access the following page:

<img src="/assets/Gnnwb4GYOoRPLTx1YCJjtYr4pkh.jpeg" src-width="3280" src-height="852" align="center"/>

Data Status Definitions

- Pending Submission: Reward records for which distribution requests have not yet been submitted.
- Distributing: Reward records currently being distributed.
- Distributed: Reward records successfully distributed.
- Failed: Reward records where distribution failed.
- Distribution Canceled: Reward records for which distribution has been canceled.
- Locked: If the campaign task requires locking, this indicates reward records currently under lock.
- All: All reward records for the campaign.

### 2.2 Basic Campaigns

#### 2.2.1 Basic Campaign Business Logic

<img src="/assets/OuSLbJt9foU6XTx7yEZjbpgopPf.jpeg" src-width="1394" src-height="494" align="center"/>

#### 2.2.2 Basic Campaign Configuration

Operations System &gt; Campaign System &gt; Standard Campaign

Click the "New" button under the Invitation Campaign module.

<img src="/assets/DsJubiStvoj7SLxRrnHjAi2Ppjb.jpeg" src-width="1280" src-height="203" align="center"/>

Open the following page:

<img src="/assets/RsKJbHGEFosEShxlqvTjPmc7p9b.jpeg" src-width="2058" src-height="1480" align="center"/>

Configure template fields according to the following rules:

Reward Rules

<img src="/assets/CRrObFfJqoW2kKxxJxJjjJm3puI.jpeg" src-width="1280" src-height="989" align="center"/>

- The calculation logic for rewards varies depending on the reward generation timing rules.
- For trading or asset-based qualification tasks, if you want multiple tiers and corresponding multiple rewards, add multiple reward rules.

Example: The following shows four reward rules in the same campaign, where the net deposit task is divided into three tiers. If "Real-time Generation" is selected, each time a user meets a tier they generate a reward record.

<img src="/assets/Qoq4bYjkZohzmxxi9wzjzkIApIg.jpeg" src-width="3144" src-height="548" align="center"/>

#### 2.2.3 Basic Campaign Reward Data Query

Reward data is available only while the campaign is running and rewards are being distributed.

Click the details button for the relevant campaign, then open the "Winners" tab to access the following page:

<img src="/assets/GQY0bAl4towBVSxvUZaj84XIpeP.jpeg" src-width="2712" src-height="1132" align="center"/>

Data Status Definitions

- Pending Submission: Reward records for which distribution requests have not yet been submitted.
- Distributing: Reward records currently being distributed.
- Distributed: Reward records successfully distributed.
- Failed: Reward records where distribution failed.
- Distribution Canceled: Reward records for which distribution has been canceled.
- Locked: If the campaign task requires locking, this indicates reward records currently under lock.
- All: All reward records for the campaign.

### 2.3 Team Campaigns

#### 2.3.1 Team Campaign Business Flow

<img src="/assets/ABwlbDfrFoHZLUxyek7jRKv2pHd.jpeg" src-width="2274" src-height="434" align="center"/>

#### 2.3.2 Team Campaign Configuration

Operations System &gt; Campaign System &gt; Standard Campaign

Click the "New" button under the Team Campaign module.

<img src="/assets/BXxVboksioes5ExkTTUjmjxmp0f.jpeg" src-width="1280" src-height="201" align="center"/>

Open the following page:

<img src="/assets/PfH5bZiTCoJFTUxbVTpjxS3Npvb.jpeg" src-width="1886" src-height="1648" align="center"/>

Configure template fields according to the following rules:

#### 2.3.3 Team Campaign Reward Data Query

Data is available only while the campaign is running and rewards are being distributed.

Click the details button for the relevant campaign, then open the "Winners" tab to access the following page:

<img src="/assets/DVrJbh8k1oJz0lxILKXjq98hpac.jpeg" src-width="2730" src-height="818" align="center"/>

Data Status Definitions

- Pending Submission: Reward records for which distribution requests have not yet been submitted.
- Distributing: Reward records currently being distributed.
- Distributed: Reward records successfully distributed.
- Failed: Reward records where distribution failed.
- Distribution Canceled: Reward records for which distribution has been canceled.
- Locked: Not applicable to the current assistance-style team campaign; ignore.
- All: All reward records for the campaign.

#### 2.3.4 Team Information Viewing

In assistance campaigns, the initiator invites assistants to form a team; team information can therefore be viewed.

Data is available only while the campaign is running and rewards are being distributed.

Click the details button for the relevant campaign, then open the "Team Information" tab to access the following page:

<img src="/assets/JrhxbXekZobKdixFZiUjqDvKpZj.jpeg" src-width="2716" src-height="838" align="center"/>

Data Statistics

- In Progress: Number of teams initiated and still below the preset assistant count during the campaign.
- Team Success: Number of teams that reached the preset assistant count.
- Team Failure: Number of teams that failed to reach the preset assistant count by campaign end.
- All: Total number of teams initiated in the campaign.

<img src="/assets/VCpwbyFMPofDW0xSZprjPBZjpag.jpeg" src-width="1062" src-height="650" align="center"/>

## 3. Non-standard Campaign Management

Users: Operations

Use case: Offline reward distribution, e.g., corporate client appreciation events with no explicit campaign rules—used solely to issue rewards to users.

Primary function: Create a campaign to obtain a campaign code. Then, in the Benefits System &gt; Rewards Center, associate the campaign code to distribute rewards.

Navigation: Operations System &gt; Campaign System &gt; Non-standard Campaign Management

You can query and manage created campaign records here (the current design archives standard campaigns into this list as well; therefore this list contains both standard campaigns and non-standard campaigns, serving as a comprehensive campaign query repository).

<img src="/assets/OQAubTCgLoTS2LxkSVjj3gnvpof.jpeg" src-width="2720" src-height="1216" align="center"/>

Campaign management list field descriptions

<img src="/assets/QcBsbup4coXxv3x4OdUjVtxEpyb.jpeg" src-width="944" src-height="334" align="center"/>

### 3.1 Non-standard Campaign Configuration

Click the "New" button at the top of the page to open the following page:

<img src="/assets/GhA4bD37CoYjeTxGybVj6FV1p7c.jpeg" src-width="1742" src-height="1612" align="center"/>

Because non-standard campaigns do not have explicit rules, creating them is primarily to obtain a campaign code for later association with the Rewards Center. Therefore, optional fields on the creation page may be left blank.

Below are explanations for important fields:

## 4. Invitation Relationship Management

[Not Support block type: Diagram/21]

As illustrated: a user will generate a unique invitation code within a given App. The user shares this code with friends who can then fill it in to bind. After binding, it is updated in the invitation relationship list.

Invitation relationships bound through invitation campaigns can be queried here, and manual bindings can also be performed.

Navigation: Operations System &gt; Campaign System &gt; Invitation Relationship Management

<img src="/assets/RSiWbdrHJo9AQzxeTSKjE6gOpDb.jpeg" src-width="2730" src-height="1010" align="center"/>

Primary functions:

- Query: By switching the top tabs, you can query registration invitations, account-opening invitations, and deposit invitations.
- Add: Bind invitation relationships for users directly from the back office.
- Details: View specific user information for a binding, including binding channel, binding time, and modify bindings.

(Completed action nodes cannot have their corresponding invitee bound; for incomplete nodes, you may bind or change the inviter.)

### 4.1 Adding Invitation Relationships

#### 4.1.1 Add Registration Invitation

Click the "New" button on the Invitation Relationship Management page to open the following dialog:

<img src="/assets/CabybyqTYoai7axEKXkjSOH8pNg.jpeg" src-width="1280" src-height="183" align="center"/>

<img src="/assets/W6Hebszq5oB9ujxl8k4j17vPpkc.jpeg" src-width="936" src-height="708" align="center"/>

Enter the invitee's and inviter's customer IDs to complete the binding.

#### 4.1.2 Add Account-opening or Deposit Inviter

First, locate the invitee for whom you want to bind an inviter by filtering the list, then click the user's details to view:

<img src="/assets/CmUabn2i4oddJJx0mfMjFS7kplf.jpeg" src-width="2698" src-height="392" align="center"/>

The details page displays the user's registration inviter and allows binding of account-opening and deposit inviters.

<img src="/assets/CMwsblvGso2Y4PxQYQWj4nwXppf.jpeg" src-width="2712" src-height="1710" align="center"/>

In the dialog that appears, enter the inviter's user ID to complete the binding for the invitee's account-opening/deposit inviter.

If the user has not completed a node, you may change the bound inviter for that node using the same procedure—enter the new inviter's user ID to update the binding.

## Common Questions for Campaign Operations

Q: A user reports not receiving a reward. How should operations investigate?

Navigation: Operations System &gt; Campaign System &gt; Standard Campaign Management

First verify that the campaign configuration is correct. Click the details button for the relevant campaign and review the campaign rules and reward configuration to confirm accuracy.

<img src="/assets/OAhgbH8IsoWvKSxGHzajrC56pPf.jpeg" src-width="1280" src-height="595" align="center"/>

<img src="/assets/DpOdbs7ApoXGPLxTIq6jgXkdpwh.jpeg" src-width="1280" src-height="636" align="center"/>

If the configuration is correct, check the Winners list to confirm whether a reward record was generated and to inspect the reward record status.

<img src="/assets/K4tdbv5IhoH2bXxlqsbjTO1Dp1b.jpeg" src-width="1280" src-height="443" align="center"/>

If the status is "Distributing" the system is still processing the distribution. If the status is "Pending Submission," operations must click "Submit" to initiate distribution.

Q: How to verify whether a user’s invitation binding succeeded?

Navigation: Operations System &gt; Campaign System &gt; Invitation Relationship Management

<img src="/assets/JLorb2hpioY1LOxNo92jq0Lyp8y.jpeg" src-width="1280" src-height="492" align="center"/>

After searching, the list displays all invitation relationships bound for that user. Click the details button to view specific user binding information.

<img src="/assets/Oyf6b07gNoqpsGxIGpdjDO1apQe.jpeg" src-width="1280" src-height="395" align="center"/>

<img src="/assets/FMwzbjQSCoHpa7x7AAtjFasgpFe.jpeg" src-width="1280" src-height="632" align="center"/>

