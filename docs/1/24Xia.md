# 基本信息

24年6月；TII；Xia（河海大学能源与电气学院助理教授）；

# 关键词

DLMP-parametrized ADMM；

为了明确地将耦合网络约束添加到产消者的问题中，我们对配电网潮流模型进行线性化，并将线性约束投影到产消者的可行区域（OE）。然后，我们分析网络约束的 P2P 交易能源市场中的 GNE，并将原始 GNE 简化为**归一化纳什均衡**（NNE）。我们将原始模型放松为部分对偶问题，并采用 DLMP 来描述产消者对配电网络运营的**异构影响**。我们修改ADMM算法来分解产消者的交易流程以保护他们的隐私。最后列出并讨论了 NNE 的算法收敛性和市场特性。引入四总线玩具模型来说明我们提出的方法的收敛性和特性。我们导入了修改后的 IEEE 69 总线系统，以进一步突出我们模型的优势。

# 第一篇网络约束+GNE

Since all participants’ strategies affect the distribution network power flow (DNPF), a generalized Nash game (GNG) is formulated among P2P market participants [3].

> 由于所有参与者的策略都会影响配电网潮流（DNPF），因此P2P市场参与者之间制定了广义纳什博弈（GNG）[3]。

To our best knowledge, our work is the first paper going beyond the VE subset for specific P2P market properties.

> 据我们所知，我们的工作是第一篇超越特定 P2P 市场属性的 VE 子集的论文。VE：变分平衡

To our best knowledge, this article is the first work to exploit the NNE of the P2P energy market considering the coupling network constraints.

> 据我们所知，本文是第一篇考虑耦合网络约束的 P2P 能源市场 NNE 开发工作。

# 双层框架

Since the prosumers do not know the detailed network parameters, a bi-level P2P energy-sharing market is considered a silver bullet to accommodate the network constraints [4].

> 由于产消者不知道详细的网络参数，双层 P2P 能源共享市场被认为是适应网络约束的灵丹妙药 [4]。

# 网络约束P2P交易模型要解决的问题

There are following several significant research gaps in network-constrained P2P trading model.

\1) Once the P2P transaction cannot pass the security check, the traditional approach directly discards the corresponding transaction. Such an approach seriously damages the market participants’ interests and reduces their enthusiasm for participating. An interactive mechanism that can simulate negotiations between prosumers and the operator should be exploited.

> 一旦P2P交易无法通过安全检查，传统做法会直接丢弃对应的交易。这种做法严重损害了市场参与者的利益，降低了他们的参与积极性。应利用可以模拟产消者和运营商之间谈判的交互机制。

\2) The DNPF is affected by all prosumers’ trading strategies. The prosumers thus formulate a GNG constrained by the coupling distribution network constraints. The GNG coupled by distribution network constraints is seldom discussed in the existing literature due to the complexity of DNPF.

> DNPF 受到所有产消者交易策略的影响。因此，产消者制定了受耦合分销网络约束的 GNG。由于DNPF的复杂性，现有文献中很少讨论配电网约束耦合的GNG。DNPF：配网潮流。

\3) To simplify the equilibrium seeking of GNG, most existing literature assumes the coupling constraints share the same Lagrange multiplier. However, the prosumers at different nodes have heterogeneous impacts on the DNPF. The GNE solution algorithm allowing various Lagrange multipliers of coupling constraints should be developed.

> 为了简化 GNG 的平衡寻求，大多数现有文献假设耦合约束共享相同的拉格朗日乘子。然而，不同节点的产消者对DNPF的影响是异质的。应开发允许耦合约束的各种拉格朗日乘数的 GNE 求解算法。

# 现有不足

The direct ban on energy sharing hinders the P2P energy market development.

> 能源共享的直接禁止阻碍了P2P能源市场的发展。

\1) the iteration convergence is highly dependent on parameter tuning, 3) the iteration number increases sharply with the expansion of the market size,

> 1）迭代收敛高度依赖于参数调整，没有标准化的流程
>
> 3）随着市场规模的扩大，迭代次数急剧增加，阻碍了不同市场参与者之间的进一步合作。

Without iteration, operating envelope (OE) was employed.

> 若不使用迭代，[8]中采用操作范围（OE）作为能源产消者的可行区域。

Assuming the prosumer models are feasible, compact, and convex, the original P2P energy market clearing problem can be equivalent to a variational inequality [14].

> 假设产消者模型是可行的、紧凑的、凸的，原始的P2P能源市场出清问题可以等价于变分不等式[14]。

However, various prosumers have heterogeneous impacts on the distribution network. It is impractical to assume the same shadow price for all prosumers [16].

> 然而，不同的产消者对分销网络有不同的影响。假设所有产消者都具有相同的影子价格是不切实际的[16]。

The simplified linear power flow model was imported in [20] to constrain the traded energy, which is inexact.

> 文献[20]中引入了简化的线性潮流模型来约束交易能量，但该模型并不精确。
