# 矿池

<!-- TOC -->

- [矿池](#%E7%9F%BF%E6%B1%A0)
    - [1. 托管矿池](#1-%E6%89%98%E7%AE%A1%E7%9F%BF%E6%B1%A0)
    - [2. P2P矿池](#2-p2p%E7%9F%BF%E6%B1%A0)

<!-- /TOC -->

在这个激烈竞争的环境中，个体矿工独立工作（也就是solo挖矿）没有一点机会。他们找到一个区块以抵消电力和硬件成本的可能性非常小，以至于可以称得上是赌博，就像是买彩票。就算是最快的消费型ASIC也不能和那些在巨大机房里拥有数万芯片并靠近水电站的商业矿场竞争。

现在矿工们合作组成矿池，汇集数以千计参与者们的算力并分享奖励。通过参加矿池，矿工们得到整体回报的一小部分，但通常每天都能得到，因而减少了不确定性。

让我们来看一个具体的例子。假设一名矿工已经购买了算力共计14,000GH/S，或14TH/S的设备，在2017年，它的价值大约是2500美元。

该设备运行功率为1.3千瓦（KW），每日耗电32度，每日平均成本1或2美元。以目前的比特币难度，该矿工solo方式挖出一个块平均需要4年。如果这个矿工确实在这个时限内挖出一个区块，奖励12.5个比特币，如果 每个比特币价格约为1000美元（译者：这是作者出版此书的价格，2017年10月22日译者看到的价格是5880美元），可以得到12,500美元的收入。这甚至不能覆盖整个硬件和整个时间段的电力消耗，净亏损约为1,000美元。而且，在4年的时间周期内能否挖出一个块还主要靠矿工的运气。他有可能在4年中得到两个块从而赚到非常大的利润。或者，他可能5年都找不到一个块，从而遭受经济损失。

更糟的是，比特币的工作证明（POW）算法的难度可能在这段时间内显著上升，按照目前算力增长的速度，这意味着矿工在设备被下一代更有效率的矿机取代之前，最多有1年的时间取得成果。如果这个矿工加入矿池，而不是等待4年内可能出现一次的暴利，他每周能赚取大约50-60美元。矿池的常规收入能帮他随时间摊销硬件和电力的成本，并且不用承担巨大的风险。在1-2年后，硬件仍然会过时，风险仍然很高，但在此期间的收入至少是定期的和可靠的。

从财务数据分析，这只有非常低的电力成本（每千瓦不到1美分），非常大的规模时才有意义。矿池通过专用挖矿协议协调成百上千的矿工。

个人矿工在建立矿池账号后，设置他们的矿机连接到矿池服务器。他们的挖矿设备在挖矿时保持和矿池服务器的连接，和其他矿工同步各自的工作。这样，矿池中的矿工分享挖矿任务，之后分 享奖励。成功出块的奖励支付到矿池的比特币地址，而不是单个矿工的。一旦奖励达到一个特定的阈值，矿池服务器便会定期支 付奖励到矿工的比特币地址。

通常情况下，矿池服务器会为提供矿池服务收取一个百分比的费用。参加矿池的矿工把搜寻候选区块的工作量分割，并根据他们挖矿的贡献赚取“份额”。矿池为赚取“份额”设置了一个低难度 的目标，通常比比特币网络难度低1000倍以上。

当矿池中有人成功挖出一块，矿池获得奖励，并和所有矿工按照他们做出贡献的“份额”数的比例分配。矿池对任何矿工开放，无论大小、专业或业余。一个矿池的参与者中，有人只有一台小矿机，而有些人有一车库高端挖 矿硬件。有人只用几十度电挖矿，也有人会用一个数据中心消耗兆瓦级的电量。矿池如何衡量每个人的贡献，既能公平 分配奖励，又避免作弊的可能？答案是在设置一个较低难度的前提下，使用比特币的工作量证明算法来衡量每个矿工的贡献。

因此，即使是池中最小的矿工也经常能分得奖励，这足以激励他们为矿池做出贡献。通过设置一个较低的取得份 额的难度，矿池可以计量出每个矿工完成的工作量。每当矿工发现一个小于矿池难度的区块头hash，就证明了它已经完 成了寻找结果所需的hash计算。更重要的是，这些为取得份额贡献而做的工作，能以一个统计学上可衡量的方法，整体 寻找一个比特币网络的目标散列值。成千上万的矿工尝试较小区间的hash值，最终可以找到符合比特币网络要求的结果。

让我们回到骰子游戏的比喻。如果骰子玩家的目标是扔骰子结果都小于4（整体网络难度），一个矿池可以设置一个更容易的目标，统计有多少次池中的玩家扔出的结果小于8。当池中的玩家扔出的结果小于8（矿池份额目标），他们得到份额，但他们没有赢得游戏，因为没有完成游戏目标（小于4）。但池中的玩家会更经常的达到较容易的矿池份额目 标，规律地赚取他们的份额，尽管他们没有完成更难的赢得比赛的目标。时不时地，池中的一个成员有可能会扔出一个小于4的结果，矿池获胜。然后，收益可以在池中玩家获得的份额基础上分配。

尽管目标设置为8或更少并没有赢得游戏，但是这是一个衡量玩家们扔出的点数的公平方法，同时它偶尔会产生一个小于4的结果。同样的，一个矿池会将矿池难度设置在保证一个单独的矿工能够频繁地找到一个符合矿池难度的区块头hash来赢取份 额。时不时的，某次尝试会产生一个符合比特币网络目标的区块头hash，产生一个有效块，然后整个矿池获胜。

## 1. 托管矿池

大部分矿池是“托管的”，意思是有一个公司或者个人经营一个矿池服务器。矿池服务器的所有者叫矿池管理员，同时他 从矿工的收入中收取一个百分比的费用。矿池服务器运行专业软件以及协调池中矿工们活动的矿池采矿协议。矿池服务器同时也连接到一个或更多比特币完全节点并直接访问一个块链数据库的完整副本。这使得矿池服务器可以代替矿池中的矿工验证区块和交易，缓解他们运行一个完整节点的负担。

对于池中的矿工，这是一个重要的考量，因为一个完整节点要求一个拥有最少100-150GB的永久储存空间（磁盘）和最少2GB到4GB内存（RAM）的专用计算机。

此外，运行一个完整节点的比特币软件需要监控、维护和频繁升级。由于缺乏维护或资源导致的任何宕机都会伤害到矿工的利润。对于很多矿工来说，不需要跑一个完整节点就能采矿，也是加入托管矿池的一大好处。

矿工连接到矿池服务器使用一个采矿协议比如Stratum\(STM\)或者 GetBlockTemplate\(GBT\)。一个旧标准GetWork\(GWK\)自从2012年底已经基本上过时了，因为它不支持在hash速度超过4GH/S时采矿。STM和GBT协议都创建包含候选区块头模板的区块模板。矿池服务器通过打包交易，添加coinbase交易（和额外的随机值空间），计算MERKLE根，并连接到上一个块hash来建立一个候选区块。这个候选区块的头部作为模板分发给每个矿工。矿工用这个区块模板在低于比特币网络的难度下采矿，并发送成功的结果返回矿池服务器赚取份额。

## 2. P2P矿池

托管矿池存在管理人作弊的可能，管理人可以利用矿池进行双重支付或使区块无效。（参见“10.12 共识攻击”） 此外，中 心化的矿池服务器代表着单点故障。如果因为拒绝服务攻击服务器挂了或者被减慢，池中矿工就不能采矿。

在2011年， 为了解决由中心化造成的这些问题，提出和实施了一个新的矿池挖矿方法。P2Pool是一个点对点的矿池，没有中心管理 人。P2Pool通过将矿池服务器的功能去中心化，实现一个并行的类似区块链的系统，名叫份额链（share chain）。

一个份额链是一个难度低于比特币区块链的区块链系统。份额链允许池中矿工在一个去中心化的池中合作，以每30秒一个份额区块的速度在份额 链上采矿，并获得份额。份额链上的区块记录了贡献工作的矿工的份额，并且继承了之前份额区块上的份额记录。当一个份额区块上还实现了比特币网络的难度目标时，它将被广播并包含到比特币的区块链上，并奖励所有已经在份额链区 块中取得份额的池中矿工。

本质上说，比起用一个矿池服务器记录矿工的份额和奖励，份额链允许所有矿工通过类似比特币区块链系统的去中心化的共识机制跟踪所有份额。P2Pool采矿方式比在矿池中采矿要复杂的多，因为它要求矿工运行空间、内存、带宽充足的专用计算机来支持一个比特 币的完整节点和P2Pool节点软件。P2Pool矿工连接他们的采矿硬件到本地P2Pool节点，它通过发送区块模板到矿机来 模拟一个矿池服务器的功能。在P2Pool中，单独的矿工创建自己的候选区块，打包交易，非常类似于solo矿工，但是他 们在份额链上合作采矿。

P2Pool是一种比单独挖矿有更细粒度收入优势的混合方法。但是不需要像托管矿池那样给管理人太多权力。即使P2Pool减少了采矿池运营商的中心化程度，但也可能容易受到份额链本身的51％的攻击。 P2Pool的广泛采用并不能解决比特币本身的51％攻击问题。相反，作为多样化采矿生态系统的一部分，P2Pool整体使得比特币更加强大。