---
title: Position Management
slug: L4caw5q4fiphmkk468ZjKQJCpAF
sidebar_position: 5
---


# Position Management

## System Introduction

This manual standardizes the full back-office operational procedures for fiat and cryptocurrency position management, covering core operations such as position inquiry, allocation rule configuration, automatic allocations, and manual allocations. It is intended to guide back-office personnel in performing tasks in a standardized manner, ensuring business compliance and fund security and mitigating operational risk.

## Prerequisites

- Back-office personnel must log in to the WBO backend system using a dedicated account and password. After successful login, they can access the following core modules: "Virtual Asset Management - Position Management", "Funds Management - Bank Statements - Company Fund Allocation", "Business Parameter Settings - Funds Parameters - Settlement Channel Account", and "Business Parameter Settings - Funds Parameters - Funds Allocation Configuration".
- Operator accounts must have been granted the relevant permissions for "Position Management", "Company Fund Allocation", "Settlement Channel Account", and "Funds Allocation Configuration" in advance. If an account lacks the required permissions, contact the system administrator to submit a permission request; operations may only proceed after permissions are granted.

## Operation Paths and Permission Descriptions

Below are the core modules with their permission names, corresponding operation descriptions, and permission identifiers. Operators must perform actions within their authorized scope; unauthorized operations are strictly prohibited.

## Operational Instructions

### Position Inquiry Operations

- Log in to the WBO backend system and navigate to the "Virtual Asset Management - Position Management" module. Executing inquiries requires the permission identifier: `assets.position_anagement_inquiry_query`.
    - After entering the module, filter query conditions as needed (e.g., update time, currency, channel account type). Enter the corresponding parameters and click the "Query" button.
        <img src="/assets/TQCpbU4dIog36zx3tUYjTPhspFf.png" src-width="3768" src-height="1508" align="center"/>

- To perform subsequent operations within this module, request the additional operation permission: `assets.position_anagement_inquiry_operation`.
    - The system polls position information automatically every five minutes. To retrieve the current balances for each channel account and currency, click the "Refresh" button to update manually.

        <img src="/assets/E9j6bqNDfoE6Bgx9M3kj3Y5dpXb.png" src-width="3790" src-height="1488" align="center"/>
    - For large accounts, configure both alert thresholds and blocking thresholds as needed:
        - If an alert threshold is configured and the channel's available balance &lt; alert threshold, the system will automatically send an alert notification according to the message subscription settings.
            <img src="/assets/DfwubbDOuoNKLXxBgKoj3GEDp8W.png" src-width="3752" src-height="1458" align="center"/>
        - If a blocking threshold is configured and the channel's available balance &lt; blocking threshold, the system will send an alert notification according to the message subscription settings; if the account is used for intercepting principal or fees for withdrawals, the system will enforce business interception in the "Virtual Asset Management - Withdrawals - Withdrawal Application" module. The rules are as follows:
            1. If the withdrawal fee account balance is insufficient, the withdrawal application cannot be approved. The system will block the operation and display: "The channel account's fee balance for this currency is insufficient. Please perform a fund allocation first."
            2. If the withdrawal principal account balance is insufficient, the withdrawal application cannot be approved. The system will block the operation and display: "The channel account's principal balance for this currency is insufficient. Please perform a fund allocation first."
            3. If both principal and fee accounts are insufficient, the withdrawal application cannot be approved. The system will block the operation and display: "The channel account's principal and fee balances for this currency are insufficient. Please perform a fund allocation first."
                <img src="/assets/QtUkbuIyao5jr3xRuNPjw1Ijpeb.png" src-width="3780" src-height="1464" align="center"/>

### Settlement Channel Account Configuration

- Before performing allocation operations, configure upstream channel account information. Allocations between accounts may only be performed after the configuration becomes effective.
- Log in to the WBO backend system and navigate to "Business Parameter Settings - Funds Parameters - Settlement Channel Account". Performing configuration operations requires the permission identifier: `atm.settle_chnl_bank_acct_operation`.
    - On the configuration page, you may perform "Create" and "Edit" operations. Procedures:
        - Create account information: Click the "Create" button and accurately fill in the settlement channel information (including settlement channel, currency type, and currency) and the main account information (including main account number and business scenario). Verify all parameters and submit to save; the configuration takes effect immediately.
            <img src="/assets/RxGtb9JomoIojlxr7cdjETM2pGg.png" src-width="3812" src-height="1340" align="center"/>
            <img src="/assets/NcWybDY5NoS4p7x6mxEjK8Jjpbh.png" src-width="3470" src-height="1528" align="center"/>
        - Edit account information: Select the account configuration record to modify, click the "Edit" button, adjust parameters as required, and submit to overwrite the existing configuration. Pay special attention to potential impacts of configuration changes on ongoing and upcoming allocation operations to avoid business anomalies.
            <img src="/assets/CEpqbQhVjogbRKxXXFbjXdyhphe.png" src-width="3404" src-height="1504" align="center"/>

- After configuration, users with the `atm.settle_chnl_bank_acct_inquiry` query permission may access the module to review all configured account information and verify parameter accuracy to ensure that configurations meet actual business requirements.

    <img src="/assets/WOVGbUux3oX7wVxcTm8jq9N5pSh.png" src-width="3808" src-height="1150" align="center"/>

### Allocation Rule Configuration

- To enable automatic fund allocations, preconfigure automatic allocation scenarios and corresponding rules in the backend.
- Log in to the WBO backend system and navigate to "Business Parameter Settings - Funds Parameters - Funds Allocation Configuration". Performing rule configuration requires the permission identifier: `atm.funds_alloc_config_operation`.
    - On the configuration page, you may perform "Create Rule", "Edit Rule", and "Copy Rule" operations. Procedures:
        - Create Rule: Click the "Create" button, set the allocation type to "Transfer between settlement accounts", select the outgoing channel as "settlement_hashkey_hk", and configure automatic transfer rules according to different business scenarios. Verify parameters and submit to save.
            <img src="/assets/HYdYbccwGoNvCYxdsjRjoiYApFi.png" src-width="3802" src-height="1102" align="center"/>
            <img src="/assets/UnW4bU1NqoIpRWxLTwnjq134pGf.png" src-width="2976" src-height="3542" align="center"/>
        - Edit Rule: Select the rule to modify, click "Edit", adjust parameters according to business requirements, and submit to overwrite the existing rule. Pay special attention to impacts on currently executing and future automatic allocation tasks to prevent business anomalies.

            <img src="/assets/U1smbAuZToGY7hxcOw3jDlCqpIb.png" src-width="3812" src-height="1062" align="center"/>
        - Copy Rule: Select an existing configured rule and click "Copy" to modify parameters based on the original rule, simplifying the creation of new rules and improving configuration efficiency.

            <img src="/assets/Vh5zbAVGyocaM8xK091jT7O5pyf.png" src-width="3760" src-height="1056" align="center"/>

- After rule configuration, users with the `atm.funds_alloc_config_inquiry` query permission may review all configured allocation rules and verify parameter accuracy to ensure rules meet automatic allocation requirements.

    <img src="/assets/LTd4bIfXWoFheAxnpfFjEWGApWe.png" src-width="3812" src-height="1118" align="center"/>

### Automatic Allocation Operations

- Automatic allocations require prior completion of "Funds Allocation Configuration" (see Section 4.3). The system will execute allocations automatically based on preconfigured trigger conditions without manual intervention. Current automatic allocation trigger scenarios include two main categories:
    - Scheduled transfers: Support configuration of scheduled tasks (e.g., daily at midnight) to automatically transfer surplus funds among deposit accounts, trading accounts, etc., according to preset rules. Supported scheduling types are: calendar day, Hong Kong trading day, and weekly.
    - Event-triggered transfers:
        - When positions are insufficient: In "Virtual Asset Management - Position Management", if the corresponding channel available balance for a main account &lt; blocking threshold, the system will match the main account to "Business Parameter Settings - Funds Parameters - Funds Allocation Configuration"; if there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate the allocation according to that rule. If automatic allocation fails due to insufficient balance in the outgoing account, subsequent manual transfer is required.
        - On withdrawal submission (principal): When a withdrawal application is generated in "Virtual Asset Management - Withdrawals - Withdrawal Application" and applies to the principal portion, the system will match "Business Parameter Settings - Funds Parameters - Funds Allocation Configuration"; if there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate allocation per the rule. If allocation fails due to insufficient outgoing account balance, manual transfer is required afterward.
        - On withdrawal submission (fees): When a withdrawal application is generated and applies to the fee portion, the system will match the funds allocation configuration; if there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate allocation per the rule. If allocation fails due to insufficient outgoing account balance, manual transfer is required afterward.
        - On withdrawal failure (principal): When a withdrawal application fails and applies to the principal portion, the system will match the funds allocation configuration; if there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate allocation per the rule. If allocation fails due to insufficient outgoing account balance, manual transfer is required afterward.
        - On withdrawal failure (fees): When a withdrawal application fails and applies to the fee portion, the system will match the funds allocation configuration; if there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate allocation per the rule. If allocation fails due to insufficient outgoing account balance, manual transfer is required afterward.
        - On deposit success: When a deposit is marked successful in "Virtual Asset Management - Deposits - Deposit Records", the system will match the funds allocation configuration; if there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate allocation per the rule. If allocation fails due to insufficient outgoing account balance, manual transfer is required afterward.

- Operators may use the "Funds Management - Bank Statements - Company Fund Allocation" module (requires the `atm.company_fund_allocation_inquiry` query permission) to view automatic allocation execution records, including allocation time, amount, currency, source account, destination account, business order number, and other core information for traceability and auditing.

    <img src="/assets/Wjm3bQe7iofhbjxQnTnjJWgdp1c.png" src-width="3784" src-height="1062" align="center"/>

- If automatic allocation fails, the system will clearly indicate the failure reason (e.g., insufficient account balance). Operators must promptly investigate, adjust the relevant rules or replenish funds, and may manually trigger a retry (requires the corresponding operation permission in "Funds Management - Bank Statements - Company Fund Allocation") to ensure successful fund allocation.

    <img src="/assets/BgqEbVaFnoflagxCekqjuG7OpTd.png" src-width="3786" src-height="1262" align="center"/>

### Manual Allocation Operations

- Log in to the WBO backend system and navigate to "Funds Management - Bank Statements - Company Fund Allocation". Performing manual allocation operations requires the permission identifier: `atm.company_fund_allocation_operation`.
    - Click the "Create" button and accurately complete the allocation information, including initiating account, receiving account, allocation currency, allocation amount, and allocation remarks (clearly state the allocation reason to facilitate subsequent traceability and auditing). Verify all information and submit.


        <img src="/assets/PlW0blVApo4tQQxAPmJjh6qcpEg.png" src-width="3766" src-height="1200" align="center"/>
        <img src="/assets/ZzPObbgySoLuCRxmnT7jL0vRpOc.png" src-width="2792" src-height="2738" align="center"/>

- Manual allocation applications submitted via the "Create" button, or allocation applications whose audit strategy in "Business Parameter Settings - Funds Parameters - Funds Allocation Configuration" is "work order approval", will enter the approval workflow automatically and must be reviewed by personnel with the permission identifier `atm.company_fund_allocation_approval`:
    - After approval, the system will automatically execute the allocation.
    - If rejected, the allocation application fails; if the allocation remains necessary, a new manual allocation application must be submitted.
        <img src="/assets/B9rybOhS0oBu1yxam1Tj0mZNpng.png" src-width="3740" src-height="1042" align="center"/>

- After allocation completion, operators with the `atm.company_fund_allocation_inquiry` query permission may view the execution status and detailed records of manual allocations to verify all related data and ensure allocation compliance and accuracy.

    <img src="/assets/ArA8bfs9ko5QtQxtJxEjTTtwpic.png" src-width="3756" src-height="804" align="center"/>

## Notes

- Operators must securely protect account credentials, strictly prohibit lending accounts to others, lock the system promptly after login if necessary, and log out properly after use to prevent account compromise and associated fund risk.
- All operations must strictly follow this manual. Unauthorized operations and improper allocations are strictly forbidden. During operations, carefully verify related parameters (e.g., account information, amounts, currencies) to avoid mistakes.
- Record-keeping is required for key operations such as allocation rule configuration and manual allocations to support future audits. If anomalies are detected (e.g., abnormal positions, allocation failures, data discrepancies), report them to the administrator promptly; concealment is strictly prohibited.
- System permission changes must be performed centrally by administrators. If an operator requires permission changes, submit a formal application; changes take effect only after approval. After permission changes, familiarize yourself with the new permission scope promptly.
- Fiat and cryptocurrency position changes are sensitive. Operators must monitor position status in real time, especially balances near automatic allocation thresholds, and prepare funds in advance to prevent insufficient positions from disrupting business operations.

