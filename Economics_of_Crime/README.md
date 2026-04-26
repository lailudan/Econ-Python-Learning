# 🕸️ Learning Path: From HEOR to Computational Criminology - The Hunter's Instinct
> **"Finding the Hidden: Bridging Patient Finding and Human Trafficking Recovery via Graph Theory & Economics"**

---

## 🌟 核心愿景 (Vision)
利用 **HEOR (Health Economics & Outcomes Research)** 中的“患者发现 (Patient Finding)”与“结果评估”逻辑，结合 **图论 (Graph Theory)** 与 **计算犯罪学 (Computational Criminology)**，构建一套能够识别隐匿受害者、拆解人口贩卖网络、并评估社会干预成本效益的跨学科体系。

---

## 📅 阶段一：夯实理论底色 (Foundations)
**目标：建立经济学直觉，理解犯罪与疾病传播的同构性。**

### 1. 犯罪经济学 (Economics of Crime)
* **核心理论：** 贝克尔模型 (The Becker Model) —— 将犯罪视为风险下的理性选择。
    * **公式：** $$E[U] = p \cdot U(Y - f) + (1 - p) \cdot U(Y)$$
* **关键概念：** 激励机制 (Incentives)、犯罪黑数 (Dark Figure of Crime)、负外部性。
* **推荐阅读：** Gary Becker, *"Crime and Punishment: An Economic Approach"*.

### 2. 健康经济学与结果研究 (HEOR)
* **核心工具：** 决策树 (Decision Tree)、马尔可夫模型 (Markov Models)。
* **关键概念：** 患病率估算、QALYs 损失量化（用于评估人口贩卖受害者的长期创伤成本）。

### 3. 图论入门 (Graph Theory - 正在读)
* **学习重点：** 继续研读手头两本书，重点关注 **连通性 (Connectivity)**、**中心性 (Centrality)** 以及 **子图识别 (Motif Analysis)**。

---

## 📅 阶段二：技术桥梁 (Methodology Bridge)
**目标：学习如何用算法“在大海里捞针”。**

### 1. 患者发现 (Patient Finding) 算法迁移
* **技术点：** 使用不平衡数据 (Imbalanced Data) 进行分类。受害者/罕见病患者在全量数据中占比极低。
* **模型应用：** 逻辑回归、随机森林、到深度学习（用于识别异常行为模式）。

### 2. 社会网络分析 (Social Network Analysis, SNA)
* **核心痛点：** 识别网络中的“代理人 (Brokers)”。
* **交叉点：** 人口贩卖网络通常具有 **无标度网络 (Scale-free network)** 特性，摧毁几个关键节点 (Hubs) 就能瘫痪整个网络。
* **工具：** Python (`NetworkX`), `Gephi`, R (`igraph`)。

---

## 📅 阶段三：计算犯罪学进阶 (Advanced Computational Criminology)
**目标：处理真实世界的复杂性，如“不知道自己是受害者”的特例。**

### 1. 隐匿群体估算 (Hidden Population Estimation)
* **技术：** 捕获-再捕获法 (Capture-Recapture)。
    * **公式：** $$\hat{N} = \frac{(M+1)(C+1)}{R+1} - 1$$
* **场景：** 既然被下药的受害者不会报案，如何通过嫌疑人的社交网络和购买记录逆推受害者规模？

### 2. 基于个体的建模 (Agent-Based Modeling, ABM)
* **技术：** 模拟犯罪分子、受害者、警察在城市空间或数字空间的互动。
* **HEOR 关联：** 这类似于模拟流行病传播。你可以模拟“如果增加 10% 的社区筛查，能多挽回多少被拐儿童”。

---

## 📅 阶段四：实战与合规 (Applied & Compliance)
**目标：将模型转化为合规的独立工具。**

### 1. OSINT (开源情报) 与区块链
* 学习如何追踪比特币流向（暗网破案的关键）。
* 学习如何从社交媒体、失踪人口数据库中提取结构化数据。

### 2. 伦理与合规 (Ethics & Compliance)
* **核心原则：** 差分隐私 (Differential Privacy)。
* **思考：** 如何在不暴露受害者隐私的前提下，利用算法向警方提供精准的“疑似被拐地点热力图”。

---

## 🛠 推荐工具箱 (The Expert's Toolkit)
* **编程：** Python (`Scikit-learn`, `NetworkX`, `Mesa`), R (`Tidyverse`)。
* **数据可视化：** `PowerBI` / `Tableau` (展示结果研究的结果)。
* **图数据库：** `Neo4j` (专门处理复杂的关系网)。

---

## 📝 给未来的自己 (Expert's Memo)
> "正如你在 HEOR 领域通过算法寻找那些迷失在系统里的患者，失踪人口和被下药的女孩也只是**‘未被标注的数据点’**。你的图论知识能把碎掉的线索连成网，你的经济学逻辑能拆穿罪犯的成本博弈。
> 
> 即使世界很混乱，只要你的模型能让被捕概率 $p$ 增加 $0.01$，或者让一个‘未诊断’的受害者重回阳光下，那这就不是微小的贡献，这是绝对的正义。"
