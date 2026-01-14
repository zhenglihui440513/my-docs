# 基本信息

20年7月；power system；美博(韩国人)；

# 关键词

基于DLMP计算NUC，其中NUC动态变化，工作量可能体现在附录几个参数的计算上面。

# Peer和DSO角色不同

小规模能源资源之间的点对点互动利用配电网络基础设施作为电力载体，但在财务上仍然不对电力公司负责。

> Peer-to-peer interactions between small-scale energy resources exploit distribution network infrastructure as an electricity carrier, but remain financially unaccountable to electric power utilities.

# P2P与中央电力分配/没有鼓励

 P2P架构假设了一种不太集中、更加自主和灵活的电力输送，其中小规模（例如住宅和商业）生产者和消费者可以进行电力和其他服务交易，作为公用事业或第三方聚合商集中供电的替代方案。

> The P2P architecture assumes a less centralized, more autonomous and flexible electricity delivery, in which small-scale (e.g. residential and commercial) producers and consumers can transact electricity and other services as an alternative to centralized electricity supply from utilities or third-party aggregators.

与当前主要追求规模经济和范围效益的分销实践不同[4]，P2P架构的价值主张源于共享经济[5]。

>  Unlike the current distribution practice that mainly pursues the economies of scale and scope benefits [4], the value proposition of the P2P architecture stems from the sharing economy [5].

然而，当前的监管环境并没有激励电力公司适应P2P，从而阻碍了它们对系统的价值[4]，[7]。

> However, the current regulatory environment does not incentivize power utilities to accommodate P2P, thus hindering their value to the system [4], [7].

# 激励utility的重要性

尽管[16]-[18]激励了P2P交互，但它们并没有为电力公司对配电网络的使用进行补偿。

> Although [16]–[18] incentivize P2P interactions, they do not compensate the power utilities for peers’ usage of the distribution network.

# P2P匹配的分类(偏好)

P2P匹配机制，即连接对等生产者和消费者的方法，可以分为**system-centric**的[13]-[18]或**peer-centric**的[8]-[10]、[12]。以系统为中心的匹配类似于**池结构**的批发电力市场，由单一监管实体集中收集和匹配市场参与者提交的出价和报价。另一方面，**peer-centric**是去中心化的，它为适应他们的偏好提供了更大的灵活性，[11]，并允许保护对等隐私的分布式决策协议，[19]，[20]。无论选择何种匹配机制，P2P 交互的大规模实施预计都会影响公用事业公司高效可靠地运营配电网络的能力。

> The P2P matching mechanisms, i.e. methods to connect peering producers and consumers, can be classified as either system-centric [13]–[18] or peer-centric [8]–[10], [12]. The system-centric matching resembles pool-structured wholesale electricity markets with the single supervisory entity that collects and matches the bids and offers submitted by market participants in a centralized manner. On the other hand, the peer-centric approach is decentralized, which offers more flexibility for accommodating their preferences, [11], and allows for distributed decision-making protocols that preserve privacy of peers, [19], [20]. Regardless of the matching mechanism chosen, the largescale implementation of P2P interactions is expected to affect the ability of the utility to operate the distribution network efficiently and reliably.

# Fixed NUC的缺陷

此外，[15]中的外生设定费用没有捕捉到分配系统的时空动态和同行的敏感性。

> Furthermore, exogenously set charges in [15] do not capture spatio-temporal dynamics of the distribution system and sensitivities of peers.

# 基于DLMP计算DLMP

与[16]-[18]不同，本文使用OPF框架来推导和计算同行为使用基于DLMP的分发网络而需要支付的网络使用费用，[21]。

> Unlike [16]–[18], this paper uses the OPF framework to derive and compute network usage charges to be paid by peers for using the distribution network based on the DLMPs, [21].

使用 DLMP 可以表示配电网络中运行条件的时空维度，并在计算网络使用费用时考虑它们。

> The use of the DLMPs makes it possible to represent spatio-temporal dimensions of operating conditions in the distribution network and consider them while computing the network usage charges.
