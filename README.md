## Introduction

## KBY Initial Bancor Offer 发行规则

KBY 将使用 Kyubey 协议合约和团购合约发行。
Kyubey 协议将设置价格与发行量的函数为一次函数，类似 P3D 的价格曲线。

- 价格增加速率：10^-10 / KBY
- 初始价格：0.002 EOS/KBY
- 初始 dummy 发行量：20M
- 初始 dummy 储备金：20k

dummy 的发行量和储备金并不存在，只是为了设置初始价格，
和调整初始价格曲线的位移而存在，从而防止早期投资者的收益过大。
我们只募集我们认为合理的金额。

- 一期募集金额 80k  EOS，时间：10.29th
- 二期募集金额 200k EOS，时间：2019 年 Q1，具体时间待定。

## eospinduoduo 团购合约
为了防止机器人和老鼠仓等行为，初始时合约的购买功能，仅开放给一个白名单合约 eospinduoduo。
用户可以在这个合约中进行统一登记，并在一定时间后，所有人按照相等的价格购买。

- https://kyubey.network/Home/Analysis/kyubey

## CW 储备金率
bancor 合约中的储备金率大概是一组多余的设计，
只需要给定价格关于发行量的函数即可。那么所需储备金关于发行量的函数即是这组函数的积分。

例如在 P3D 合约中，价格既是一次函数。
- https://kyubey.network/Home/Analysis/kyubey
- https://www.desmos.com/calculator/fzuirhfejx

## Project Progress 项目进度
项目进度参数是 Kyubey 孵化器协议中的一项核心设计，用来描述项目推进的进度。
和传统的募资方式不同的时，Kyubey 协议中并不设计项目方预留的 Token，也不能直接获得合约中的储备金。
项目方团队获得资金的方式，是通过按照 roadmap 中的承诺，一步一步达成 milestone，达到社区的认可，从而推进项目进度系数而获得的。

当项目初始发行时，项目进度为 0，此时市场的热度仅表示社区的认可程度，项目方此时并不能得到任何直接收益。
当项目进度推进时，项目方才可以将合约余额超过合约所需要最大储备金的部分转移到社区基金账户，
而 bancor 合约中新的交易也会根据项目进度收取手续费。

因而，当项目进度不断推进时，市场的流通量也会逐渐从孵化器合约转移到外部的交易所。

最终，当项目进度到达 100% 时，项目所有的交易量全部转移到外部交易所，项目方脱离孵化器合约，
相当于项目完成上市。

Kyubey 孵化器合约的目标和使命就是帮助每个项目推进项目进度，连接 dapp 开发者和社区，促进 dapp 的大规模落地。



