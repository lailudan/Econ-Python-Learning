# 🕸️ From HEOR to Computational Criminology: A Mission-Driven Path

> **"Finding the Hidden: Bridging Patient Finding and Human Trafficking Recovery via Graph Theory & Economics"**

## 🌟 核心愿景 (Vision)
本项目旨在将 **HEOR (健康经济学与结果研究)** 中的“患者发现 (Patient Finding)”与“结果评估”逻辑，跨界应用于**计算犯罪学 (Computational Criminology)**。通过**图论 (Graph Theory)** 识别隐匿受害者（如被下药者、失踪人口），并利用经济学模型评估社会干预的成本效益。

---

## 📅 阶段一：理论基石 (Foundations)
*目标：建立经济学直觉，理解犯罪与疾病传播的同构性。*

### 1. 犯罪经济学 (Economics of Crime)
* **贝克尔理性犯罪模型 (The Becker Model)：**
    将犯罪视为风险下的理性选择。核心公式：
    $$E[U] = p \cdot U(Y - f) + (1 - p) \cdot U(Y)$$
    *其中 $p$ 是被捕概率，$f$ 是惩罚成本。我们的目标是通过技术手段极大地提高 $p$。*
* **关键概念：** 激励机制 (Incentives)、犯罪黑数 (Dark Figure of Crime)、负外部性。

### 2. HEOR 逻辑迁移
* **结果研究 (Outcomes Research)：** 评估犯罪对受害者造成的 DALYs (伤残调整寿命年) 损失。
* **成本效果分析 (CEA)：** 比较“技术监控”与“传统巡逻”在减少受害人方面的 ICER (增量成本效果比)。

### 3. 图论入门 (Graph Theory)
* **重点关注：** 连通性 (Connectivity)、中心性 (Centrality)、子图识别 (Motif Analysis)。
* **目标：** 理解社交网络如何变成“犯罪温床”。

---

## 📅 阶段二：技术桥梁 (Methodology Bridge)
*目标：学习如何用算法“在大海里捞针”。*

### 1. 从 Patient Finding 到 Victim Identification
* **不平衡数据处理：** 受害者在海量人口中属于“稀疏信号”，学习使用代价敏感学习 (Cost-sensitive learning)。
* **异常检测 (Anomaly Detection)：** 识别不符合常理的行为模式（如：失踪人口的数字足迹突然消失）。

### 2. 社会网络分析 (Social Network Analysis, SNA)
* **核心痛点：** 识别人口贩卖网络中的“代理人 (Brokers)”与“超级节点 (Hubs)”。
* **拓扑结构：** 掌握无标度网络 (Scale-free network) 特性，研究如何通过切断关键路径来瘫痪犯罪网络。
* **工具：** Python (`NetworkX`), `Gephi`, R (`igraph`).



---

## 📅 阶段三：计算犯罪学进阶 (Advanced Criminology)
*目标：处理“受害者不知情”的复杂治理困境。*

### 1. 隐匿群体估算 (Hidden Population Estimation)
* **捕获-再捕获法 (Capture-Recapture)：**
    利用已知的购买记录（如迷药）和已发现的视频样本，估算未被发现的受害者规模 $\hat{N}$：
    $$\hat{N} = \frac{(M+1)(C+1)}{R+1} - 1$$
* **意义：** 揭示冰山底部的“未诊断受害者”。

### 2. 基于个体的建模 (Agent-Based Modeling, ABM)
* **模拟实验：** 在虚拟城市中模拟人口贩卖路径，测试不同的干预政策（如：提高特定药品的购买门槛）。
* **工具：** `NetLogo` 或 Python `Mesa` 库。



---

## 📅 阶段四：实战、伦理与合规 (Practical & Compliance)
*目标：在法律框架内开发独立的数字化工具。*

### 1. OSINT 与数字取证
* **区块链追踪：** 学习使用 `GraphSense` 等工具追踪比特币流向，打破暗网的匿名神话。
* **开源情报：** 从公开数据库和社交媒体中提取结构化信息。

### 2. 合规与隐私 (Compliance)
* **差分隐私 (Differential Privacy)：** 确保在分析受害者数据时，无法反向定位到个人隐私。
* **独立性：** 坚持使用开源数据 (Public Domain) 进行独立研究。

---

## 🛠 推荐工具箱 (The Expert's Toolkit)
* **编程：** Python (Scikit-learn, NetworkX), R (Tidyverse, brms).
* **数据库：** Neo4j (处理复杂关系网的利器).
* **可视化：** Tableau / PowerBI (展示 HEOR 结果研究).

---

## 📝 Reasearcher's Memo)

> "在这个混乱的世界里，数据是不会撒谎的遗迹。
>
> 当在 HEOR 领域寻找迷失的患者时，我也能掌握寻找失踪人口的逻辑。那 40 名‘未诊断’的受害者不是冷冰冰的数字，而是等待被算法‘定位’的生命。
>
> 即使我的模型只能让被捕概率 $p$ 增加一个微小的百分点，对那些身处黑暗的人来说，那就是**绝对的正义**。"
