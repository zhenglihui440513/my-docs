# 基本信息

23年5月；power system；Yang(西交大自动化-就职-可能博后)；co-author有陈玥

# 关键词

非常棒的背景介绍；本文解决的问题比较简单；Stackelberg博弈（上层定价下层P2P交易）

# DER-挑战-P2P-好处

在技术进步和推进低碳社会的压力的推动下，电力系统正在经历分布式能源（DER）的稳步增长，例如家用电池、屋顶太阳能电池板和现场风能涡轮机等[1]。因此，传统的集中式能源管理受到挑战，因为客户侧的分布式能源超出了电力系统运营商的控制范围。在这种背景下，点对点（P2P）能源交易已成为一种有前途的分布式能源交易机制[2]。 P2P旨在建立一个以消费者为中心的电力市场，允许拥有DER的消费者（即产消者）相互交易能源剩余或不足[3]，[4]。 P2P的愿景是让产消者通过互补、灵活的发电和消费，自主、经济地实现供需平衡。 P2P能源交易对电网运营商和产消者双方都有利。具体来说，P2P 可以通过允许产消者向邻居出售剩余的本地可再生能源发电来为产消者带来货币价值，反之亦然 [5]。 P2P也有利于电网运营，因为它可以降低发电和输电扩张的成本，以应对逐年增长的需求，并通过推动当地自给自足来减少输电损耗[6]。

> DRIVEN by the technology advances and the pressure to advance low-carbon society, power systems are experiencing the steady increase of distributed energy resources (DERs), such as home batteries, roof-top solar panels, and on-site wind turbines, etc. [1]. As a result, the traditional centralized energy management is being challenged as the DERs on the customer side are beyond the control of power systems operator. In this context, peer-to-peer (P2P) energy trading has emerged as a promising mechanism to account for the DERs [2]. P2P aims for a consumer-centric electricity market which allows the consumers with DERs (i.e., prosumer) to trade energy surplus or deficiency mutually [3], [4]. The vision of P2P is to empower the prosumers to achieve the balance of supply and demand autonomously and economically by leveraging their complementary and flexible generation and consumption. P2P energy trading is beneficial to both the power grid operator and the prosumers. Specifically, P2P can bring monetary value to the prosumers by allowing them to sell surplus local renewable generation to their neighbors or vice verse [5]. P2P also favors the power grid operation in term of reducing the cost of generation and transmission expansion to account for the yearly increasing demand as well as reducing transmission loss by driving local self-sufficiency [6].

 

# Clearing-categorized-blockchain

由于其广泛的前景，P2P能源交易机制引起了研究界的广泛兴趣。大量工作致力于解决具有定制偏好或兴趣的产消者的供需投标匹配问题。这通常称为市场出清机制。讨论的机制多种多样且丰富，可以大致分为基于优化的方法[7]、[8]、拍卖方案[6]、[9]和双边合同谈判[10]、[11]。不少全面、系统的综述已经记录了这些市场出清机制，例如[5]、[12]-[14]。除此之外，许多著作都讨论了利用众所周知的区块链技术实现P2P市场的信任、安全和透明（示例参见[15]、[16]）。

> Due to the widespread prospect, P2P energy trading mechanism has raised extensive interest from the research community. A large body of works has made efforts in addressing the matching of supply and demand bids for prosumers with customized preferences or interests. This is usually termed market clearing mechanisms. The mechanisms in discussion are diverse and plentiful, which can be broadly categorized by optimization-based approaches [7], [8], auction schemes [6], [9], and bilateral contract negotiations [10], [11]. Quite a few of comprehensive and systematic reviews have documented those market clearing mechanisms, such as [5], [12]–[14]. On top of that, many works has discussed the trust, secure, and transparent implementation of P2P markets by employing the well-known blockchain technology (see [15], [16] for examples).

 

# Interaction-维护双方

上述研究主要集中在虚拟层和产消者角度的能源交易商业模式。而P2P市场中的能源交易需要由电网运营商在物理层进行电力传输，电网运营商负责确保传输容量约束并补偿传输损耗。在这方面，虚拟层进行能源交易的产消者与物理层进行交易的电网运营商之间的有效互动对于P2P市场方案的成功部署至关重要。交互需要保证P2P市场中产消者的经济利益，并确保电网运营商的运营可行性。这已被确定为 P2P 交易的剩余关键问题[17]。

> The above studies are mainly focused on the business models of energy trading in virtual layer and in the shoes of prosumers. Whereas the energy transaction in a P2P market require the delivery of power in physical layer taken by the power grid operator who is responsible for securing the transmission capacity constraints and compensating the transmission loss. In this regard, the effective interaction between the prosumers making energy transaction in virtual layer and the power grid operator delivering the trades in physical layer is essential for the successful deployment of P2P market scheme. The interaction requires to secure the economic benefit of prosumers in the P2P market as well as ensure the operation feasibility of power grid operator. This has been identified as a remaining key issue for P2P transaction [17].

 

# NUC好处：回收成本、影响P2P

允许电网运营商向产消者征收一些电网相关成本（通常称为网络费用）以进行 P2P 交易的想法已被提倡作为桥接这种互动的有前途的工具。从多方面考虑，网络收费是合理、自然的。首先，电网收费是电网归因网络投资成本和输电损耗的必要条件[18]。在传统电力系统中，用户与电网进行能源交易，这种成本已经内化在电价中，因此很自然地通过一些价格机制将P2P的类似成本转嫁给产消者。此外，网络收费可以作为塑造P2P市场的手段，以保证电网运营商物理层的可行运行[19]。网络费用通常是按交易收取的，因此可以用来指导P2P市场中产消者的能源交易行为。

> The idea to allow the grid operator to impose some grid related cost (usually known as network charge) on the prosumers for P2P transaction has been advocated as a promising tool to bridge this interaction. Network charge is reasonable and natural considering many aspects. First of all, network charge is necessary for the power grid to attribute the network investment cost and the transmission loss [18]. In traditional power systems where customers trade energy with the power grid, such cost has been internalized in the electricity price, it is therefore natural to pass the similar cost of P2P to the prosumers via some price mechanisms. Besides, network charge can work as a means to shape the P2P market so as to ensure the feasible operation of physical layer taken by the grid operator [19]. Network charge is often charged by trades, therefore it can be used to guide the energy trading behaviors of prosumers in the P2P market. 

 

# NUC实例-不足

因此，最近的一些工作依赖于网络费用来计算与电网相关的成本并塑造 P2P 市场，例如[11]、[18]、[20]。具体来说，[20]在开发去中心化的P2P市场清算机制时涉及网络费用。文献[18]比较模拟了三种网络收费模型（即独特模型、基于电气距离的模型和区域模型）对P2P市场塑造的影响。这项工作[11]依赖于网络收费模型来实现产消者之间的事后传输损耗分配。这些工作证明了网络收费在塑造P2P市场方面的有效性。此外，网络收费可以作为归因于电网运营商实际承担的电网相关成本和输电损耗的工具。

> As a result, several recent works have relied on network charge to account for the grid-related cost and shape the P2P markets, such as [11], [18], [20]. Specifically, [20] has involved network charge in developing a decentralized P2P market clearing mechanism. The work [18] comparatively simulated three network charge models (i.e., unique model, electrical distance based model, and zonal model) on shaping the P2P market. The work [11] has relied on a network charge model to achieve ex-post transmission loss allocations across the prosumers. These works have demonstrated the effectiveness of network charge in shaping P2P market. In addition, network charge can work as a tool to attribute grid-related cost and transmission loss which are actually taken by the grid operator. 

 然而，现有的工作主要集中在研究网络收费将如何影响P2P市场中产消者的行为，而不是研究如何设计网络收费价格，将电网运营商和产消者作为独立的利益相关者并扮演不同的角色。

> However, the existing works have mainly focused on studying how the network charge will affect the behaviors of prosumers in a P2P market instead of studying how the network charge price to be designed which couples the grid operator and the prosumers acting as independent stakeholders and playing different roles.

# 最优NUC设计

为了填补这一空白，本文旨在研究一种综合考虑提供输电服务的电网运营商和在P2P市场上进行能源交易的产消者的最优网络收费机制。

> To fill the gap, this paper aims to study an optimal network charge mechanism that jointly considers the power grid operator who provides transmission service and the prosumers who make energy transaction in a P2P market. 
