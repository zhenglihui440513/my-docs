260107 代码导读

# NUC

## case5

Pt_p,Pt_c是7×7；且有Pt_p+Pt_c'==0;

obj1和obj2是成本和效用；

obj3是fixed nuc和交易量和交易距离的乘积（固定成本）；



# public

## data

### get_voltage_coefficient

含义：获取r，x，M_incident

细节：得到标幺值；

### get_mt_result

含义：在有load和mt的场景下，得到Pf，Qf，Vb，P_g;

细节：需要进行一次gurobi的调用

输入load的数值（选择ieee33给定数值，转换成标幺值）；选择2倍；mt位置按照论文进行设置；

进行opf，基于给定的mt的成本参数，在不违约下最小化成本值；

关键约束在于Pf(1)==0，即不需要从主网进行电力购买；v_var设置成0.04，给p2p留下一点裕量；

### get_trade_info_test

含义：得到prosumer的参数；fixed_nuc;distance;

其中，a1,b1;a2,b2都是正数；最小最大出力是正值；最小最大消费是负值；

obj2=a2\*(P)^2+b2\*P；（第三象限开口向上）（取min值）；

nuc_price=0.1 \$/(MWh · ohm)

## matrix

### M_incident

含义：代表P=Mp中的M矩阵，转置一下也可以计算压降，维度是32×33维；（纯Lindistflow才有的产物）

算法细节：输入数据是feeder的from bus和to bus；

先利用feeder_i和feeder_j获得每一个bus的父节点和子节点；

然后，根据parent和children，获得M矩阵；

对任意bus，往上溯源，被溯到就将对应元素置为1；

### impedance

含义：得到z矩阵

细节：输入r和x，得到标幺值，进行根号下平方和计算；保存；

### V_distance_trade

含义：1×49维，利用z矩阵进行叠加

针对给定的7个producer和7个consumer的位置，依次计算对应的distance；

定义了一个函数，有c的位置，p的位置，parent向量，z向量，通过溯源的方式求和得到；

### M_ptdf（lindistflow才有）

含义：32*49矩阵，交易对feeder产生的影响（1，0，-1）

论文的写法较为简洁，比代码实现要好得多；

### M_VSC（lindistflow才有）

含义：33*49矩阵，交易对bus电压值产生的影响（正向为负值）；

论文写法较为简洁，代码实现看都看不懂；

但是应该测试一下论文写法写得对不对（自己感觉应该是对的）

