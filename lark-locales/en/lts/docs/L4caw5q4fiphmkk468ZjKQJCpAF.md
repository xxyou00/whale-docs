---
title: Position Management
slug: L4caw5q4fiphmkk468ZjKQJCpAF
sidebar_position: 5
---


# Position Management

# System Overview

This manual standardizes the full backend operation workflow for fiat and cryptocurrency position management, covering core procedures such as position inquiry, allocation rule configuration, automatic allocation, and manual allocation. It is intended to guide backend operators to perform tasks in a standardized manner, ensure business compliance and fund security, and mitigate operational risks.

# Prerequisites

- Backend operators must log in to the WBO backend system with a dedicated account and password. After successful login, they may access the following core modules: "Virtual Asset Management - Position Management", "Funds Management - Bank Statements - Company Fund Allocation", "Business Parameter Settings - Fund Parameters - Settlement Channel Account", and "Business Parameter Settings - Fund Parameters - Fund Allocation Configuration".
- Operator accounts must be preauthorized with the relevant permissions for "Position Management", "Company Fund Allocation", "Settlement Channel Account", and "Fund Allocation Configuration". If an account lacks the corresponding permissions, submit a permission request to the system administrator; operations may proceed only after permissions are granted.

# Operation Paths and Permission Descriptions

- The following table lists the core modules, associated permission descriptions, and permission identifiers. Operators must perform actions according to their own permissions; unauthorized operations are strictly prohibited.

# Operation Instructions

## Position Inquiry Operations

- Log in to the WBO backend system and navigate to the "Virtual Asset Management - Position Management" module. Executing inquiries requires the permission identifier: `assets.position_anagement_inquiry_query`.
    - After entering the module, you may filter query criteria according to business needs (e.g., update time, currency, channel account type). Enter the appropriate parameters and click the "Query" button.
        <img src="/assets/Y1RXbBpsAortfRxoBkOjX7oapse.png" src-width="3304" src-height="908" align="center"/>

- To perform subsequent operations within this module, additional operation permission is required: `assets.position_anagement_inquiry_operation`.
    - The system is preset to poll position information automatically every five minutes. To query the real-time balances of each account and currency for a channel, click the "Refresh" button to update manually.

        <img src="/assets/EClHbEFnuouVnAxBeNkjKdNupQc.png" src-width="3274" src-height="882" align="center"/>
    - For high-balance accounts, you may configure an alert threshold and a blocking threshold as needed:
        - If an alert threshold is configured and the channel available balance &lt; alert threshold, the system will automatically send an alert notification according to the notification subscription settings.

            <img src="/assets/SkD7bf7yUoOK5txgfBrjRMI7pTg.png" src-width="3300" src-height="1316" align="center"/>
        - If a blocking threshold is configured and the channel available balance &lt; blocking threshold, the system will send an alert notification according to the notification subscription settings; if the account is used for withdrawal principal blocking or withdrawal fee blocking scenarios, the system will enforce a business block in the "Virtual Asset Management - Withdrawals - Withdrawal Application" module. The rules are as follows:
            1. If the withdrawal fee account balance is insufficient, the withdrawal application cannot be approved; the system will block the process and display: "The channel account's balance for this currency is insufficient for fees; please perform a fund allocation first."
            2. If the withdrawal principal account balance is insufficient, the withdrawal application cannot be approved; the system will block the process and display: "The channel account's balance for this currency is insufficient for principal; please perform a fund allocation first."
            3. If both the principal and fee accounts are insufficient, the withdrawal application cannot be approved; the system will block the process and display: "The channel account's balance for this currency is insufficient for both principal and fees; please perform a fund allocation first."
                <img src="/assets/QBm9bEfDHo9YcfxSeEHjvRsTpxc.png" src-width="3330" src-height="1204" align="center"/>

## Settlement Channel Account Configuration

- Before performing fund allocation operations, complete the upstream channel account information configuration. The configuration must take effect before transfers between accounts can be executed.
- Log in to the WBO backend system and navigate to "Business Parameter Settings - Fund Parameters - Settlement Channel Account". Executing configuration operations requires the permission identifier: `atm.settle_chnl_bank_acct_operation`.
    - On the configuration page, you may perform "Create" and "Edit" operations. The specific procedures are as follows:
        - Create account information: Click the "Create" button and accurately fill in the settlement channel information (including settlement channel, currency type, and currency) and the primary account information (including primary account number and business scenario). After verifying all parameters are correct, submit and save; the configuration takes effect immediately.
            <img src="/assets/HtCzbOG4JooHLXxe8ybjanlypgg.png" src-width="3266" src-height="702" align="center"/>
        - Edit account information: Select the account configuration record to be modified, click the "Edit" button, adjust the relevant parameters according to business requirements, and submit to save; the updated configuration will overwrite the previous one. Pay particular attention to the potential impact of configuration changes on currently executing and upcoming fund allocation operations to avoid business anomalies.

            <img src="/assets/MSp9bOjdPouGjWxAmL9jSlYJpZb.png" src-width="3272" src-height="1738" align="center"/>

- After configuration is complete, users with the query permission identifier `atm.settle_chnl_bank_acct_inquiry` may access the module to view all configured account information and verify parameter accuracy to ensure configuration aligns with business requirements.

    <img src="/assets/AogdbNFnuojiDqxzeG3jwV0Hpqe.png" src-width="3252" src-height="1744" align="center"/>

## Allocation Rule Configuration

- To enable the system to execute fund allocations automatically, preconfigure automatic allocation scenarios and corresponding rules in the backend.
- Log in to the WBO backend system and navigate to "Business Parameter Settings - Fund Parameters - Fund Allocation Configuration". Executing rule configuration operations requires the permission identifier: `atm.funds_alloc_config_operation`.
    - On the configuration page, you may perform "Create Rule", "Edit Rule", and "Copy Rule" operations. The procedures are as follows:
        - Create rule: Click the "Create" button, select the allocation type as "Transfer Between Settlement Accounts", choose the outbound channel as "settlement_hashkey_hk", and configure the automatic transfer rules according to different business scenarios. After confirming parameters are correct, submit and save.
            <img src="/assets/O6bqb6zrDo3gxfxXQKHjmydHpvb.png" src-width="3320" src-height="1564" align="center"/>
        - Edit rule: Select the allocation rule to be modified, click the "Edit" button, adjust relevant parameters according to business requirements, and submit to save; the modified rule will overwrite the original. Pay special attention to the impact of rule changes on currently executing automatic allocations and subsequent operations to avoid business anomalies.

            <img src="/assets/K4ZdbrvKzo06ASx06lAjC4tJpjh.png" src-width="3298" src-height="734" align="center"/>
        - Copy rule: Select an existing configured rule, click the "Copy" button, and modify relevant parameters based on the original rule to simplify the creation of new rules and improve configuration efficiency.

            <img src="/assets/IRs8b6PCSoOuFpxj2v6jSA2hp7c.png" src-width="3298" src-height="734" align="center"/>

- After rule configuration, users with the query permission identifier `atm.funds_alloc_config_inquiry` may access the module to view all configured allocation rules and verify parameter accuracy to ensure that rules meet automatic allocation requirements.

    <img src="/assets/MEvPbS4RwoZ5d7xLdyGjjNG5pXf.png" src-width="3320" src-height="1564" align="center"/>

## Automatic Allocation Operations

- Automatic allocation requires prior completion of the "Fund Allocation Configuration" (see Section 4.3). The system will automatically execute allocations based on preconfigured triggering conditions without manual intervention. Current automatic allocation scenarios include the following two major types:
    - Scheduled transfers: Support configuration of scheduled tasks (e.g., daily at midnight) that transfer surplus funds among deposit accounts, trading accounts, etc., according to preset rules. Supported schedule types include: calendar day, Hong Kong stock trading day, and week.
    - Event-triggered transfers:
        - Position shortage: In "Virtual Asset Management - Position Management", if the channel available balance for the corresponding primary account &lt; blocking threshold, the system will match the primary account to "Business Parameter Settings - Fund Parameters - Fund Allocation Configuration". If there exists an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate an allocation according to that rule. If the automatic allocation fails due to insufficient balance in the outbound account, a manual transfer must be initiated subsequently.
        - Upon withdrawal submission (principal): When a withdrawal application is generated in "Virtual Asset Management - Withdrawals - Withdrawal Application", for the principal portion the system will match "Business Parameter Settings - Fund Parameters - Fund Allocation Configuration". If there exists an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate an allocation according to that rule. If the allocation fails due to insufficient balance in the outbound account, a manual transfer must be initiated subsequently.
        - Upon withdrawal submission (fee): When a withdrawal application is generated in "Virtual Asset Management - Withdrawals - Withdrawal Application", for the fee portion the system will match "Business Parameter Settings - Fund Parameters - Fund Allocation Configuration". If there exists an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate an allocation according to that rule. If the allocation fails due to insufficient balance in the outbound account, a manual transfer must be initiated subsequently.
        - Upon withdrawal failure (principal): When a withdrawal application fails in "Virtual Asset Management - Withdrawals - Withdrawal Application", for the principal portion the system will match "Business Parameter Settings - Fund Parameters - Fund Allocation Configuration". If there exists an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate an allocation according to that rule. If the allocation fails due to insufficient balance in the outbound account, a manual transfer must be initiated subsequently.
        - Upon withdrawal failure (fee): When a withdrawal application fails in "Virtual Asset Management - Withdrawals - Withdrawal Application", for the fee portion the system will match "Business Parameter Settings - Fund Parameters - Fund Allocation Configuration". If there exists an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate an allocation according to that rule. If the allocation fails due to insufficient balance in the outbound account, a manual transfer must be initiated subsequently.
        - Upon deposit success: When a deposit is shown as successful in "Virtual Asset Management - Deposits - Deposit Records", the system will match "Business Parameter Settings - Fund Parameters - Fund Allocation Configuration". If there exists an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will automatically initiate an allocation according to that rule. If the allocation fails due to insufficient balance in the outbound account, a manual transfer must be initiated subsequently.

- Operators may review automatic allocation execution records (including allocation time, amount, currency, source account, destination account, business order number, and other core information) in the "Funds Management - Bank Statements - Company Fund Allocation" module (requires the `atm.company_fund_allocation_inquiry` query permission) for audit and traceability purposes.

    <img src="/assets/YyaqbHRumoh4qSxoWNojElPApXe.png" src-width="3294" src-height="670" align="center"/>

- If automatic allocation fails, the system will clearly indicate the failure reason (e.g., insufficient account balance). Operators must promptly investigate the issue, adjust the corresponding rules or replenish funds, and may manually trigger a retry (requires the "Funds Management - Bank Statements - Company Fund Allocation" operation permission) to ensure successful completion of the fund allocation.

    <img src="/assets/Re0HbVZODod7qkx2UF5jdSr3pPK.png" src-width="3304" src-height="852" align="center"/>

## Manual Allocation Operations

- Log in to the WBO backend system and navigate to "Funds Management - Bank Statements - Company Fund Allocation". Executing manual allocation operations requires the permission identifier: `atm.company_fund_allocation_operation`.
    - Click the "Create" button and accurately fill in the allocation information, including source account, destination account, allocation currency, allocation amount, and allocation remarks (clearly indicate the reason for allocation to facilitate subsequent tracing and auditing). Verify all information is correct and submit.
        <img src="/assets/FJvSbRucUoxSoaxnEhDj9I3GpQc.png" src-width="3296" src-height="694" align="center"/>

- Allocation requests submitted manually via the "Create" button, or allocation requests with an approval strategy of "Work Order Review" in "Business Parameter Settings - Fund Parameters - Fund Allocation Configuration", will automatically enter the approval workflow. Approval must be conducted by personnel with the permission identifier `atm.company_fund_allocation_approval`:
    - Upon approval, the system will execute the allocation automatically.
    - If the request is rejected, the allocation attempt fails; if the allocation is still required, submit a new manual allocation request.
    <img src="/assets/HQyFbVJX4oJW2PxMvgXj9SegpUb.png" src-width="3286" src-height="686" align="center"/>

- After the allocation operation is complete, operators with the query permission identifier `atm.company_fund_allocation_inquiry` may review the execution status and record details of manual allocations to verify the data and ensure the allocation process is compliant and accurate.

    <img src="/assets/RLDpbtYuAoQHlCxtWSnjJHRRpgh.png" src-width="3284" src-height="1166" align="center"/>

# Precautions

- Operators must securely safeguard account credentials and must not lend them to others. Lock the system promptly upon leaving and log out properly to prevent account compromise and resulting fund risks.
- All operations must strictly follow this manual. Unauthorized operations and improper allocations are strictly prohibited. Carefully verify related parameters during operations (e.g., account information, amounts, currencies) to avoid operational errors.
- Maintain records for critical operations such as allocation rule configuration and manual allocations to facilitate subsequent audits. If anomalies are detected (e.g., position irregularities, allocation failures, data discrepancies), report them to the administrator immediately; concealment is strictly prohibited.
- System permission changes must be performed centrally by the administrator. If an operator requires permission adjustments, submit a formal request and obtain approval before changes take effect. After permission changes, familiarize yourself promptly with the operations allowed under the new permissions.
- Fiat and cryptocurrency position changes are sensitive. Operators must monitor positions in real time, especially account balances near automatic allocation thresholds, and prepare funds in advance to avoid disruptions to normal business operations due to insufficient positions.

