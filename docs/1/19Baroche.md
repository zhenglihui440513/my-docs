# 基本信息

19年7月；power system；Baroche（丹麦 SATIE实验室）

# 关键词

第一次提出利用NUC协调P2P交易；

# 审查法

The various **attribution** mechanisms are to impact trades and subsequent network usage. The first approach to coordinated **multi-lateral** electricity trades was already proposed nearly 20 years ago [4]. The original aim was to allow for the separation of economics and reliability of system operation, as is the case for current European pool-based electricity markets. The proposal involved an iterative process with all players proposing their trades first, followed by the system operator to decide whether the trades respect operational constraints, or not. This proposal was recently enhanced in [5], also analyzing game-theoretical properties of the solutions obtained.

> 各种归因机制都会影响交易和随后的网络使用。第一个协调多边电力贸易的方法已在近 20 年前提出[4]。最初的目标是实现系统运行的经济性和可靠性的分离，就像当前欧洲基于池的电力市场的情况一样。该提案涉及一个迭代过程，所有参与者首先提出他们的交易，然后由系统操作员决定交易是否遵守操作限制。该提议最近在[5]中得到了增强，还分析了所获得的解决方案的博弈论特性。

# OPF

A second approach may consist in relying on optimal power flow (OPF) models, allowing to consider network constraints in an endogenous manner (see e.g. [6]). While those are traditionally solved in a centralized fashion, many decomposition techniques were proposed to solve them in a distributed fashion.

> 第二种方法可能包括依赖最优潮流（OPF）模型，允许以内生方式考虑网络约束（参见例如[6]）。虽然这些问题传统上是以集中式方式解决的，但人们提出了许多分解技术来以分布式方式解决它们。

# Nodal price的特征

In network-constrained economic dispatch problems, e.g. [16], nodal prices classically encompasses both energy generation and congestion-related costs.

> 在网络受限的经济调度问题中，例如[16]，节点价格通常包含能源发电和拥堵相关成本。

# NUC好处

This network charge component is not only to recover all network costs but also other costs e.g. operational, taxes and policy-related costs.

> 该网络费用部分不仅可以收回所有网络成本，还可以收回其他成本，例如：运营、税收和政策相关成本。

Hence, network constraints are not forced directly but rather accommodated through these network charges.

> 因此，网络约束不是直接强制的，而是通过这些网络费用来调节的。

Another important benefit of this approach is that market participants have knowledge of network charges prior to the negotiation process.

> 这种方法的另一个重要好处是市场参与者在谈判过程之前就了解网络费用。

Contrary to a classical economic dispatch, this transparency on network charges enables agents to anticipate on what it will cost them to trade on the network.

> 与传统的经济调度相反，这种网络费用的透明度使代理商能够预测他们在网络上进行交易的成本

The resulting P2P market formulation comprises a simple tool, transparent to market participants, for system and market operators to limit potential detrimental effects that might be induced by P2P markets on power networks.

> 由此产生的 P2P 市场公式包括一个对市场参与者透明的简单工具，供系统和市场运营商限制 P2P 市场可能对电力网络造成的潜在有害影响。

# 拒绝DLMP

Even though local marginal prices seem effective, they may be largely rejected for their opacity by P2P market participants anxious for transparency.

> 尽管本地边际价格看似有效，但它们可能会因不透明而被渴望透明度的 P2P 市场参与者所拒绝。
