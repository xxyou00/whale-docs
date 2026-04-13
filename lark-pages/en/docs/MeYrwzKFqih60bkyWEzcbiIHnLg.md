---
title: System Introduction
slug: MeYrwzKFqih60bkyWEzcbiIHnLg
sidebar_position: 3
---


# System Overview

# I. System Overview

Currency exchange refers to the action by which an investor converts funds from one currency into another.

The Whale system provides foundational parameter configuration and primary process operation features for currency exchange. Parameter configuration includes functions such as currency pairs, exchange strategies, and exchange-pool quota settings. Operation features include frequently used functions such as manual exchange, reference rate markups, and the handling of exception exchange records.

The overall business process is as follows:

<img src="/assets/BEr4wte5Hhi5DHbSFxojUPMupLd-board.jpeg"/>

System function architecture

<img src="/assets/AuaBwBcL4h1TFQb274oj4uOXpjb-board.jpeg"/>

## Prerequisite

1. First, enable the currency exchange switch for the currency.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Fund Parameter&gt; Currency Setup</p>
</div>

<img src="/assets/VSQcbbV6zofcItx7dnCj1QV4pOh.png" src-width="2984" src-height="1314" align="center"/>

<img src="/assets/R7B9bbB2doArEgx41JXjTJGrpDc.png" src-width="2988" src-height="1310" align="center"/>

1. Configure the exchange rate precision, amount precision, and amount retrieval/rounding logic for the corresponding currency.

<img src="/assets/TQW6bGkiloTMvgxPDYVjjrMSpLh.png" src-width="2936" src-height="1332" align="center"/>

1. Then configure the supported currency pairs and establish the corresponding exchange strategies. If an exchange pool strategy is to be used, the exchange pool quotas must also be set up. For details, see Section II Operation Instructions.

# II. Operation Instructions

## Service Parameter

The Service Parameter module allows for the initial setup of the currency exchange function. Depending on the actual situation of the foreign exchange business, operators may need to complete this setup once or revisit it multiple times to ensure that exchanges are processed accurately and efficiently.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Exchange</p>
</div>

### Currency Pairs

According to the currency scope involved in the foreign exchange business, set the source and target currencies.

- Add a currency pair

Click Add and select the source and target currencies. Note: Only one source currency can be selected per currency pair. Multiple target currencies may be selected.

<img src="/assets/MBrDbjuVdodeI9x3YlUjSFuApqb.png" src-width="3014" src-height="1308" align="center"/>

After the currency pair is set, the system will display it in card format. For set currency pairs, operators can click Set default currency pair, Edit, or Delete to manage them as needed.

### Currency Exchange Strategy

This refers to the strategy that defines the entire process from client exchange request submission to execution. Currently, two strategies are supported: Exchange Pool and Bank Exchange. Specifically:

- Create an exchange strategy

Click Create. In the pop-up window, fill in the following fields sequentially: Service Strategy Setting → Exchange Type Setting → Applicable Time Period Setting → Channel Setting → Covered Currency Pairs Setting.

<img src="/assets/QiZcbdcTuo8FRYxkstJjq34NpIe.png" src-width="2948" src-height="1332" align="center"/>

- Notes:
    - Multiple service time periods can be selected, but they must not overlap. The system will apply the service strategy based on the time periods selected by the operator.
    - An exchange channel should only be selected when the service strategy is set to Bank Exchange.

After the exchange strategy is set, operators can click Edit and toggle the enable/disable switch to manage it according to actual business needs.

<img src="/assets/KCcIbQ9K8oN4rsx6os6jF9ARpQc.png" src-width="2908" src-height="1304" align="center"/>

### Exchange Pool Quota Configuration

To implement the Exchange Pool strategy, operators need to establish the exchange pool logic. This tab allows operators to add, delete, and modify exchange quotas, and continuously calculates the exchange pool balance based on the operator's executed exchange records.

<img src="/assets/SblgbM1aEo0IV3xK2pAjp3Nipwc.png" src-width="2946" src-height="1300" align="center"/>

- Add (exchange pool quota): Set the exchange pool quota according to the currency. The configuration includes:
    - Spread Amount: After the exchange quota for a certain currency is used up, the account balance of that currency must not fall below this amount.
    - Adjust Remaining Balance: As exchange business continues, operators can increase or decrease the corresponding quota according to actual business needs.

<img src="/assets/TFCVbyPAHojciQxCwknjc5nCpkw.png" src-width="3016" src-height="1318" align="center"/>

### Markup Setting

As an intermediary platform for currency exchange, the broker may charge a fee on client exchange requests. The Markup Setting feature allows operators to apply a markup to either the reference exchange rate or the executed exchange rate, which serves as the broker's service fee.

- Add a markup: Click Add. In the pop-up window, set markups by currency pair based on the Ref Rate Source Channel.
    <img src="/assets/KJFAbDBsFoiI1zxk5yqjWpwhpMg.png" src-width="2992" src-height="1330" align="center"/>
    <img src="/assets/FlCFbvBICoMKRhxEYsJjxQMlpRd.png" src-width="2946" src-height="1290" align="center"/>
    - After the currency pair is selected, the system will automatically display the corresponding reference exchange rate.
    - Markups may be specified as a Value or a Ratio.
    - Setting a markup on the reference exchange rate:
    - Reference-rate markups are applied at the time of exchange request submission, based on the underlying reference exchange rate. A calculation example is as follows:
        - Given a currency pair selected by the operator, for example, USD to CNH, the exchange rate without markup is calculated as 7.8147 ÷ 1.095 = 7.1367 (Rounded to 4 decimal places, as defined in the currency configuration).
            > Notes: Reference exchange rate = Buy price of the source currency ÷ Sell price of the target currency
                        <img src="/assets/HBhJblgq7ozWAOx9ba7j6id6pfh.png" src-width="896" src-height="254" align="center"/>
                        - Based on the exchange rate without markup calculated above and the selected currency pair (USD to CNH), the exchange rate with markups can be calculated as follows:
            <img src="/assets/Z1jYbSByjow4iexBLK5jiFV5p3b.png" src-width="1506" src-height="208" align="center"/>
    - Setting a markup on the executed exchange rate:
    - Executed-rate markups are applied at the time the client's exchange transaction is executed, based on the actual execution rate. The calculation follows the same principle as the reference rate markup example above.

### Large Amount Criteria Setting

If the operator selects the Large Amount Exchange exchange type, the criteria for "large amount" need to be set on this page. That is, the operator needs to define the threshold amount above which a transaction will be processed as a Large Amount Exchange.

- Create a criterion for "large amount": Click Create and set the threshold according to the currency.

<img src="/assets/KSy6bCy0yoN1hhxop4ljhhzTpOg.png" src-width="3000" src-height="1318" align="center"/>

## Currency Exchange

After completing the business parameter settings, operators can proceed to operate the currency exchange business functions. The business functions include client currency exchange, reference exchange rate import, exception foreign exchange record handling, exchange pool quota viewing, and exchange profit/loss viewing.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Cash Management &gt; Currency Conversion</p>
</div>

### Client Currency Exchange

Currency exchange flow chart

<img src="/assets/BElWwQxu4hN2xNb1zBRjYksApmd-board.jpeg"/>

For detailed operations, see Quick Start.

### Reference Exchange Rate

For client currency exchange, operators can view, import, edit, and set markups for exchange rates in the back office.

- Specifically
    - Exchange Rate Channels include: Hong Kong Exchange, IB, Hang Seng, ICBC
    - Exchange Rate Types include: Book Rate, Spot Rate, HKEX Rate

- Batch Import: Click Batch Import, download the template, fill in the content, and then upload it.

<img src="/assets/NNUKb2ub9oy4tCx84xljxemtpbf.png" src-width="2982" src-height="1410" align="center"/>

The template content is as follows (all fields are mandatory):

### Exception Exchange Record

For detailed operations, see Quick Start.

### Exchange Pool Quota

The exchange pool quota is updated in real time based on clients' executed exchange records. If an operator modifies the latest quota under Service Parameter &gt; Exchange, the records on this page will also be automatically updated.

- Quota setting: Go to Service Parameter &gt; Exchange &gt; Exchange pool quota configuration.

<img src="/assets/VZp8bmnAXoDiRFxxU9lj0gMhpRe.png" src-width="2962" src-height="1296" align="center"/>

### Exchange Profit/Loss

Due to the time elapsed between the submission and completion of a foreign exchange request, fluctuations in exchange rates may affect the final exchange amount. This page displays the exchange profit/loss generated by each exchange request and supports remittance of these amounts to local accounts.

<img src="/assets/GmJDbzz8HohLFhxa1lSjBmE6pCh.png" src-width="2984" src-height="1288" align="center"/>

