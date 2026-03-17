---
title: 系统介绍
slug: Ax55w2aTFie5LBkEUQbcErsTn1u
sidebar_position: 1
---


# 系统介绍

# 一、系统介绍

出金功能是指投资者从其证券账户中提取资金的操作。这个功能允许投资者将其证券账户中的资金转移到其银行账户或其他指定的账户中。

Whale系统包含了处理出金申请、提现处理、对账、单独处理异常出金、出金记录查询等功能，由于监理与风控需求，系统的功能设计具备多角色、流程化的特色，在兼顾出金效率的同时，同步降低了资金风险。

整体业务流程如下：

<img src="/assets/YfmSbxzjaoP9qRxfdZ9jQZfhp9e.png" src-width="2146" src-height="256" align="center"/>

# 二、操作说明

# 出金配置

## 资金参数配置

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>业务参数设置 &gt; 资金参数&gt;公司银行账户</p>
</div>

<img src="/assets/Yc86b25pOo4MGbxxW4ojPOOUphg.png" src-width="2844" src-height="1304" align="center"/>

- 点选【新建】，进入二级页面补充出金频道讯息（券商公司用户付款的银行账户和出金方式组合，比如：工银亚洲 001-支票转账）

<img src="/assets/EfH0bL2L0oxYFgx1OXmjCoYIphh.png" src-width="2846" src-height="1330" align="center"/>

- 打开币种的出金功能开关

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>菜单入口：业务参数设定&gt;资金参数&gt;币种</p>
</div>

<img src="/assets/ZvACbu3PLo2hDoxg3TqjtfHJpRd.png" src-width="2858" src-height="1318" align="center"/>

- 点选【新建】，进入二级页面，将出金功能的选项设为「是」

<img src="/assets/WjymbmTn1oQwEhxGlsGjR77Epvf.png" src-width="2864" src-height="1330" align="center"/>

## 自动出金规则

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>业务参数设置&gt;出金规则&gt;自动出金规则</p>
</div>

配置出金渠道打包规则，用以控制出金批量是自动还是手工处理。同时还能通过规则控制出金的单笔限额，以及服务窗口期以及支持的客户银行等。

目前可支持的出金策略包括：单笔实时、定时打包人工审核、手工打包和批量自动

<img src="/assets/UBrubTxewosjFNxHtL7j4hAwp3g.png" src-width="3304" src-height="878" align="center"/>

<b>操作按钮说明</b>

- 新建：可以根据券商公司对应出金渠道新建自动出金规则
- 编辑：对已添加的自动出金规则可选择编辑
- 删除：删除已有的自动出金规则

## 日限额以及变动表

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>业务参数设置&gt;出金规则&gt;日限额</p>
</div>

客户相应出金的渠道可能存在日限额，所以为了降低出金异常情况，建立了出金日限额监控提示以及管理。

<img src="/assets/FskcbzuLvoU8mpx95NwjwijjpQ4.png" src-width="3292" src-height="730" align="center"/>

<b>操作按钮说明</b>

- 新建：可以根据需求配置出金银行相关日限额
- 编辑：对已添加的日限额可选择编辑
- 删除：删除已有的日限额
- 调整：调整当前出金银行对应的日限额额度

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>业务参数设置&gt;出金规则&gt;日限额变动表</p>
</div>

可以查询出金银行的日限额历史变动记录

<img src="/assets/NdmtbgB2PomRUmx8O8Ljn6EYpQc.png" src-width="3264" src-height="1102" align="center"/>

对于日限额达到日剩余额度警戒线，系统会自动推送消息告警

<img src="/assets/RQ4xbJH86oXcWpxCqWHjB6y3pkc.png" src-width="1156" src-height="138" align="center"/>

## 余额拦截

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>业务参数设置&gt;出金规则&gt;余额拦截</p>
</div>

目前指用于出金业务。在出金业务中，系统会根据财务人员选择的出金银行进行余额查询，根据查询到的余额对待出金的金额进行判断，如果余额不足以支持用户提交的出金请求，则会将相应的出金进行拦截，等待财务后续人工处理。

<img src="/assets/UO0fbR6WaobkaXxm6Lijokb5ppg.png" src-width="3308" src-height="1048" align="center"/>

<b>操作按钮说明</b>

- 编辑：对于已接入 API 银行的余额查询记录可以编辑提示余额和拦截余额
- 启用：对于已接入 API 银行的余额查询记录选择启用
- 停用：对于已接入 API 银行的余额查询记录选择停用

对于银行余额达到提示余额时，系统会自动推送讯息警告

<img src="/assets/D5ihb7ofvo9c56xLX6rjb9GnpSP.png" src-width="830" src-height="194" align="center"/>

对于银行余额达到拦截余额时，系统会自动拦截对应出金并且进行告警

<img src="/assets/WYqMbiQ85oAjwGxauRIj44cxpee.png" src-width="772" src-height="220" align="center"/>

## 自动审核规则

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p> 业务参数设置&gt;出金规则&gt;自动审核规则</p>
</div>

对于客户提交出金申请是否需要后台人工审核，可以在「自动审核规则」进行设定。目前可支援的审核规则包括：人工审批需工单、人工审批无需工单、自动提交和自动驳回

<img src="/assets/SYzkbOBVMogY99xpqpcjoTMUpNb.png" src-width="3280" src-height="672" align="center"/>

<b>操作按钮说明</b>

- 新建：可以根据需求配置自动审核规则
- 编辑：对已添加的自动审核规则可选择编辑
- 启用：对于已添加的自动审核规则选择启用
- 停用：对于已添加的自动审核规则选择停用

## 更多设置

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>业务参数设置&gt;出金规则&gt;更多设置</p>
</div>

对于在「款项管理-出金-提现处理-待处理」对应操作的【直接出账】提交后是否需要工单审批，可以在「更多设置」进行配置

<img src="/assets/UfSZbJg9TodgJax4OUQjNLxBpXc.png" src-width="3302" src-height="366" align="center"/>

## 出金参数

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p> 业务参数设置&gt;出金规则&gt;出金参数</p>
</div>

可根据客户出金银行区分配置预计到账时间、预估费用等参数

<img src="/assets/Xnorb63iToyFj8xjUzhjX3Etphg.png" src-width="3262" src-height="1084" align="center"/>

<b>操作按钮说明</b>

- 新建：可以根据需求配置出金参数
- 编辑：对已添加的出金参数可选择编辑
- 复制：通过复制已有的出金参数进行快速新建

# 出金操作

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>菜单入口：款项管理-出金</p>
</div>

## 出金申请

出金申请为用户方提出，申请的内容包含了币种、申请金额、收款银行卡与备注4大部分。WHALE使用者可以手动帮助客户进行证券入仓并根据客户提交的申请进行驳回、提交审批等操作。

- 手工提现

适用于使用者联络后台操作员进行手动出金的场景，操作员需要依序填写客户的币种、申请金额、出金手续费、收款银行卡、备注资讯。如果客户有出金的证明也可以上传至系统。

<img src="/assets/Ks5KbGh3Jo3WHjxG0iEjmzo8pRc.png" src-width="1192" src-height="2434" align="center"/>

- 提交（<b>可批量操作</b>）：经过操作人员初步审查无误后，可以将申请提交至下一节点的操作人员进行审核-提现操作
- 驳回（<b>可批量操作）</b>：若客户递交的出金申请资料有误或使用者反馈本次申请无效时，操作员可以进行【驳回】操作
- 删除：若客户递交的出金申请资料有误或使用者反馈本次申请无效时，操作员也可以透过【删除】按钮直接删除目标记录
- 修改：若在提交出金申请前，发现客户递交的某笔具出金申请有问题，可在与客户确认无误后可以透过【编辑】按钮进行修正，修改后需进行工单审批，审批通过后修改内容生效。
    - 修改的范围：申请金额、出金手续费、收款银行卡、备注、凭证（重新上传）

<img src="/assets/WP60bCcVTohMAzxbSumjMMwip5c.png" src-width="3824" src-height="1418" align="center"/>

<img src="/assets/BvQab4xF2ornqixex2VjpJHxpgh.png" src-width="3322" src-height="1674" align="center"/>

## 提现处理

在初审人员提交出金申请后，复审操作人员需要进行提现处理。提现处理提供了2种方式：直接出账与打包提审。其中：

<table header_row="1">
<colgroup>
<col width="100"/>
<col width="344"/>
</colgroup>
<thead>
<tr><th><p>出金方式</p></th><th><p>适用场景</p></th></tr>
</thead>
<tbody>
<tr><td><p>直接出账</p></td><td><p>出金的记录较少，且需要快速进行出金</p></td></tr>
<tr><td><p>打包提审</p></td><td><ul>
<li>出金记录数量较多，需支援针对某一时段、特定客户或其他需集中处理出金的情境。</li>
<li>若已对接 API 渠道出金，则仅能透过打包提审方式进行出帐。</li>
</ul></td></tr>
</tbody>
</table>

- 直接出账
    <img src="/assets/PDZzbZULhoGcENxS9wxjNkqDpDc.png" src-width="3826" src-height="1024" align="center"/>
    <img src="/assets/BrpKbcaAyoZUfbxkr8LjcGOipTc.png" src-width="1674" src-height="1748" align="center"/>
    <img src="/assets/KeFfbbUQ3okZIFxBOQtjyqdApQg.png" src-width="3810" src-height="1860" align="center"/>
    - 选择目标记录后，点选操作列的【直接出账】
    - 在弹窗中输入银行名称、银行账户、渠道等信息，并在出账明细中可选择是否补充银行流水信息
    - 提交审核后，记录流转至「直接出账待处理」页面，审核者需进行工单审批，审核通过后，完成出账

- 打包提审
    <img src="/assets/BwzmbIqmeoix1nxS6qdjjM0mpug.png" src-width="3818" src-height="1536" align="center"/>
    <img src="/assets/TH54bGUR3o99efx11QBj2hxwpZg.png" src-width="3832" src-height="1848" align="center"/>
    <img src="/assets/N68mbCkSZoZFESx7ouvjU7n7pdb.png" src-width="3830" src-height="1146" align="center"/>
    <img src="/assets/D6S0bNYxIoqkgvxgubZjCtirpAg.png" src-width="3826" src-height="1826" align="center"/>
    <img src="/assets/Q6GzbDztNoAe5xxipVxjnJm6pgb.png" src-width="3910" src-height="1942" align="center"/>
    - 选择目标记录后，点选批次操作行的【打包提审】，如果在打包后需要进行移除部分明细记录，可以在弹跳窗内进行操作，填好出金的银行资讯以及渠道资讯后，该批进入审核流程
    - 提交审核后，记录流转至「打包待处理」页面，审核者需进行工单审批，审核通过后。
    - 若选择的渠道出金方式为网银，则需由财务部线下至网银操作付款。若有对接批次付款档案出金，可于批次审核通过后下载批次档，直接汇入网银进行拨款，简化网银作业流程。作业完成后，依据网银实际付款结果，回到 WBO 后台手工更新出金状态。
        <img src="/assets/RedgbrrgFoD2qAxN93rjDjgxpsc.png" src-width="3836" src-height="1826" align="center"/>
        - 点选批次记录中的【检视并更新结果】进入弹跳窗内，依照批次内的明细记录实际出金情况进行手动更新为「成功」（可批次操作）
            <img src="/assets/H9VDbp5OhoQ7BUxYud7jeSBbppo.png" src-width="1280" src-height="680" align="center"/>
    - 若选择的渠道出金方式为 API，则无须线下透过网银付款。批次审核通过后，系统将直接提交至银行处理；银行处理完毕后，系统会自动更新出金状态，处理结果可于后台查询。

- 指标卡

若出金业务量较大，可以透过系统的分类展示卡进行精细化作业，指标卡的左右排布反映了业务操作的先后顺序

<img src="/assets/HLnLbe8xFo4Tdmxwl2ejyEPYp7d.png" src-width="3830" src-height="1268" align="center"/>

- 支票列印

用户若采用<b>支票方式出金</b>，流程结束后需列印支票时，可点选页面右上方的【支票列印】按钮进入二级页面。

可支援支票列印的出金帐户，须符合以下条件：

<table header_row="1">
<colgroup>
<col width="122"/>
<col width="155"/>
</colgroup>
<thead>
<tr><th><p>银行</p></th><th><p>SWIFT CODE</p></th></tr>
</thead>
<tbody>
<tr><td><p>中银香港</p></td><td><p>BKCHHKHHXXX</p></td></tr>
<tr><td><p>创兴银行</p></td><td><p>LCHBHKHH</p></td></tr>
<tr><td><p>华侨永亨银行</p></td><td><p>WIHBHKHH</p></td></tr>
<tr><td><p>渣打银行</p></td><td><p>SCBLHKHHXXX</p></td></tr>
<tr><td><p>大新银行</p></td><td><p>DSBAHKHH</p></td></tr>
</tbody>
</table>

<img src="/assets/THR7bELzlooyZtxWyP2jezBzpGd.png" src-width="3326" src-height="1712" align="center"/>

页面内显示全部支票方式出金的记录，使用者选择目标记录后可选择支票补打或首打，（支援大量列印）输入支票号，点选【确定列印】

<img src="/assets/E1QMbkumEoyGKKxbnJLjbh8QpkL.png" src-width="3324" src-height="1758" align="center"/>

## 出金对账

为了保障资金流水的准确性，业务中需要将银行的流水与系统中的出金记录进行比对，降低资金流失的风险。银行流水的来源有2种：①API对接（自动产生）、②手动导入。（详见详见「出金账单」章节）

- 对账：用户可以选择目标期间的银行流水进行刷新，系统将自动匹配银行流水与系统的出金记录，对账完成后，可以关注清单中的「对账结果」列，如果不一致，需要进一步追踪处理。

<img src="/assets/LMNibqqoPoHfgWxXRWTj5iMJpmB.png" src-width="3826" src-height="1790" align="center"/>

<img src="/assets/DjVPbB9AbowSWbxBgWgjKa1QpGe.png" src-width="3818" src-height="1808" align="center"/>

## 异常出金

若 API 提交出金后，银行回传的错误讯息无法解析为成功或失败，系统将自动判定为异常单。若是人工处理网银出金时，将结果更新为异常，亦可于异常出金页面进行处理（支援批量操作）。系统提供了4种处理方式：
- 转成功：指出金异常经人工确认银行已完成出帐，将提现单状态更新为成功，并解冻用户资金进行出帐。
- 转失败：指出金异常经人工确认银行未出帐且后续不会自动出帐，且因用户提交资讯错误导致无法出帐，将提现单状态更新为失败，并将资金解冻退回用户帐户。
- 再付款：经确认银行端出帐失败且不再出帐，但人工确认需再次为用户打款；因对应渠道具备防重功能，需重新产生提现单后再进行付款。
- 重提交：经确认银行端出帐失败且不再出帐，但人工确认需再次为用户打款；若对应渠道无防重功能，或尚未提交至渠道，则直接重新提交原提现单即可。

<img src="/assets/WAO6bPnTJoEycZx0Gc2jUBcGp4c.png" src-width="3826" src-height="1788" align="center"/>

- 选择了具体的处理方式后，记录流转只待审核页面，业务人员需要再次复核处理结果，通过后异常出金记录处理完毕

<img src="/assets/L37CbhU2aoajKbxEFBXjEJKcpfe.png" src-width="3330" src-height="1764" align="center"/>

## 出金记录

出金记录页面记录出金的全流程状态，使用者可随时进行查询、汇出等操作

<img src="/assets/Z6HHbGiMno1ohYxfWlfj6YQnpzg.png" src-width="3816" src-height="1854" align="center"/>

## 出金账单

指代券商公司银行账户所有资金的出账变动记录，是核对出金业务的重要依据。

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>菜单入口：款项管理-银行账单-出金账单</p>
</div>

- 如果银行已经对接银企直连，则系统可以自动取得银行账单。
    - 若无法对接银企直连，则需要人工后台依照对应银行账单范本进行人工导入

<img src="/assets/YlxUbEbfUov4trxV1ThjzpQ7pIf.png" src-width="3818" src-height="1796" align="center"/>

<img src="/assets/UylVb9gesou0egx696OjzjGsptg.png" src-width="3820" src-height="1866" align="center"/>

- 对于系统取得或手动汇入的银行账单，人工确认相应入账为冗余资料且匹配状态为“未匹配”，可选择手动删除；

<img src="/assets/FOs9btJUEoHE8TxWXC1jQdDKpWf.png" src-width="3316" src-height="1692" align="center"/>

- 解析银行账单时，可能存在银行出账的负金额，此时对系统原本判断为出账就会出错。若人工发现有这样的情况，可以手工将对应的出账置为入账；

<img src="/assets/EgStbUUzyodAa5xicAOjWcU9p0c.png" src-width="3308" src-height="1700" align="center"/>

- 对于未配对的提现单需要人工进行根据实际出账进行关联打标。
    - 打标后若发现为误操作，仍可进行【拒绝】操作

<img src="/assets/AegGbalg3om30CxzXcEjMan8prf.png" src-width="3326" src-height="1718" align="center"/>

<img src="/assets/UWhwbbGcDoqBohxo0Dcjqflppbb.png" src-width="3308" src-height="1708" align="center"/>

