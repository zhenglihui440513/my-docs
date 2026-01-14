# 基本信息

20年3月，TSG，Tushar（co author包括Vincent Poor），澳洲信息和电气学院的研究员

# 关键信息

cooperative Stackelberg 博弈，稳定解存在，稳定解的算法；

场景：CPS定价（主），peer交易（从）

[1] W. Tushar *et al.*, “Grid Influenced Peer-to-Peer Energy Trading,” *IEEE Transactions on Smart Grid*, vol. 11, no. 2, pp. 1407–1418, Mar. 2020.

关键信息：①直接说next-generation energy management mechanism

②对p2p的分类;③CDA的过程详解

## P2p重要性

RECENT advancements in cryptocurrencies and blockchain have led to a proliferation of peer-to-peer (P2P) energy trading schemes [1]–[3]. Essentially, P2P trading is a next-generation energy management mechanism for the smart grid that enables a customer of the network to independently participate in energy trading with other prosumers and the grid [4]. 

>加密货币和区块链的最新进展导致了点对点 (P2P) 能源交易方案的激增 [1]–[3]。本质上，P2P交易是智能电网的下一代能源管理机制，使网络客户能够独立参与与其他产消者和电网的能源交易[4]。

Potential benefits of P2P energy trading include renewable energy usage maximization, electricity cost reduction, peak load shaving, prosumer empowerment, and network operation and investment cost minimization.

> P2P能源交易的潜在好处包括可再生能源使用最大化、电力成本降低、调峰、产消者赋能以及网络运营和投资成本最小化。

## 三种分类

The first category of studies, such as [5]–[12], focus on the financial modeling of P2P energy trading markets.

> 第一类研究，例如[5]-[12]，重点关注P2P能源交易市场的财务建模。

The second category of studies focuses on the challenges of transferring energy over the physical layer [5] of the distribution network.

> 第二类研究重点关注通过配电网络的物理层 [5] 传输能源的挑战。

The final category of studies deals with engaging prosumers in P2P energy trading. A new concept of energy classes, allowing energy to be treated as a heterogeneous product, based on attributes of its source which are perceived by prosumers to have value is introduced in [17]. 

> 最后一类研究涉及让产消者参与 P2P 能源交易。 [17] 中引入了一种新的能源类别概念，它允许根据产消者认为有价值的来源属性，将能源视为异质产品。

## 实例

However, as identified in [5], integrating P2P energy trading mechanisms into energy policy requires P2P trading to fit and complement the existing energy system.

> 然而，正如[5]所指出的，将P2P能源交易机制纳入能源政策需要P2P交易适应和补充现有的能源体系。

One potential way to establish the suitability of a P2P energy trading scheme for implementation in the traditional energy system is to show how such a scheme can benefit the centralized power system (CPS). For example, by effectively supporting the outdated electrical grids at Brooklyn, Brooklyn Microgrid is actively working closely with utilities and is currently on its way to being licensed as an energy retailer [5].

> 在传统能源系统中实施的P2P能源交易方案的一种适合的方法，是展示这种方案如何使集中式电力系统（CPS）受益。例如，通过有效支持布鲁克林过时的电网，布鲁克林微电网积极与公用事业公司密切合作，目前正在获得能源零售商许可[5]。

## 本文场景（主从博弈，prosumer组成联盟）

At the peak hour, the CPS strategically chooses the selling price per unit of energy such that the supply of energy to prosumers (consequently, the cost of excess generation or reserve) reduces to zero.

>在高峰时段，CPS 战略性地选择每单位能源的销售价格，以使产消者的能源供应（因此，过量发电或储备的成本）减少到零。

We further note that price-based coordination of distributed energy resources to support the grid is also a topic of interest in the literature related to virtual power plant (VPP).

> 我们进一步注意到，基于价格的分布式能源协调以支持电网也是与虚拟发电厂（VPP）相关的文献中感兴趣的主题。
