# 基本信息

24年3月；CSEE；Xiao(湖大电气博士)；co-author Mohammad Shahidehpour

# 关键词

dlmp+nuc+atc

# DER广泛部署带来的问题

The distribution system is facing changes related to increasing access of distributed energy resources (DERs), which have the potential to enhance system energy efficiency, economics, reliability, resilience, and sustainability [1], [2].

> 配电系统正面临着与分布式能源 (DER) 的增加相关的变化，这有可能提高系统能源效率、经济性、可靠性、弹性和可持续性 [1], [2]。

# P2P重要性/下一代技术

In the past few years, feed-in-tariff (FiT) has been used extensively to enable DER owners to participate in electricity trading [4]. However, in most countries, the FiT for selling electricity back to the power grid is lower than the price for buying electricity from the power grid [5], which allows very little profit for DER owners. As such, peer-to-peer (P2P) trading has emerged as a next-generation management technique for the smart grid which enables customers to participate in energy trading with others [6].

>  在过去几年中，上网电价补贴（FiT）已被广泛使用，使分布式能源所有者能够参与电力交易[4]。然而，在大多数国家，向电网售电的上网电价补贴低于从电网购电的价格[5]，这使得DER 所有者的利润微乎其微。因此，点对点（P2P）交易已成为智能电网的下一代管理技术，使客户能够参与与其他人的能源交易[6]。

# P2P设计研究脉络

阶段1：经济设计（不确定）；阶段2：跟网络一起设计(实例)；阶段3：考虑约束；

In [15], the distribution network is divided into several energy-shared regions to enable P2P trading and a Stackelberg-game-based model is proposed where the energy-shared regions are the leaders and the peers are followers. 

> 在[15]中，配电网络被划分为多个能源共享区域以实现P2P交易，并提出了基于Stackelberg博弈的模型，其中能源共享区域是领导者，peer是追随者。

[16] presents a methodology for the co-simulation of power distribution networks and local peer-to-peer energy trading platforms, which is demonstrated using a case study of a typical European suburban distribution network. 

> [16]提出了一种配电网络和本地点对点能源交易平台联合仿真的方法，并通过典型欧洲郊区配电网络的案例研究进行了演示。

[17] designs a P2P trading platform in the microgrid, where a hierarchical system architecture model is proposed to identify and categorize the key elements and technologies involved in P2P trading. 

>  [17]设计了微电网中的P2P交易平台，提出了分层系统架构模型来识别和分类P2P交易中涉及的关键要素和技术。

[18] proposes a loss allocation framework for P2P trading in unbalanced radial distribution networks.

>  [18]提出了不平衡径向分销网络中 P2P 交易的损失分配框架。

# ATC地位描述

ATC is one of the distributed optimization methods, which has been used for market-based power system planning [22] and operations [23].

> ATC是分布式优化方法之一，已用于基于市场的电力系统规划[22]和运行[23]。

Compared to other **distributed optimization methods**, such as the auxiliary problem principle, the alternating direction method of multipliers, and Benders decomposition, ATC has the following advantages [24]: 1) it provides a hierarchical structure to solve multilevel problems; 2) it deals with coupling variables between adjacent levels by using penalty functions; 3) it provides certain flexibilities on the selection of penalty functions.

> 与辅助问题原则、ADMM、Benders分解等其他分布式优化方法相比，ATC具有以下优点[24]：1）它提供了解决多级问题的层次结构； 2）利用惩罚函数处理相邻层之间的耦合变量； 3）在惩罚函数的选择上提供了一定的灵活性。

# 补充说明

In this paper, there are two assumptions: 1) the utility purchases active power from the wholesale market, and the reactive power is compensated at the substations. i.e., source buses of the distribution system;

> 本文有两个假设：1）公用事业公司从批发市场购买有功功率，无功功率在变电站得到补偿。
