# 隐含马尔科夫模型(Hidden Markov model, HMM)

隐含马尔可夫模型是关于时序的概率模型，描述由一个隐藏的马尔科夫链随机生成不可观测的状态随机序列，再由各个状态生成一个观测从而产生观测随机序列的过程。隐藏的马尔科夫链随机生成的状态的序列，成为状态序列(state sequence)；每个状态生成一个观测，而由此产生的观测的随机序列，成为观测序列(observation sequence)。序列的每一个位置又可以看作是一个时刻。

隐含马尔科夫模型(Hidden Markov model，HMM)
$$
Q={q_1,q_2,...,q_N} \\ V={v_1,v_2,...,v_M} \\
$$
其中，*N*是可能的状态数，*M*是可能的观测数。

*I*是长度为*T*的状态序列，*O*是对应的观测序列：
$$
I=(i_1,i_2,...,i_T) \\ O = (o_1,o_2,...,O_T)  
$$


A是状态转移矩阵：
$$
A=[a_{ij}]_N\times_N
$$
其中
$$
a_{ij} = P(i_t+1=q_j|i_t=q_i),\quad i = 1,2,...,N;\quad j=1,2,...,N
$$
B是观测概率矩阵：
$$
B=[b_j(k)]_N\times_M
$$
其中，
$$
b_j(k)=P(o_t=v_k|i_t=q_j),\quad k=1,2,...,M; \quad j = 1,2,...,N
$$
$\pi$是初始状态概向量：
$$
\pi=(\pi_i)
$$
其中，
$$
\pi_i=P(i_1=q_i),\quad i=1,2,...,N
$$
是时刻$t=1$处于状态$q_i$的概率。