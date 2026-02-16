# 📘 Ludan's Path to Economic Data Science (Python Edition)

**Owner:** Ludan Lai  
**Goal:** Master Python for HEOR & Econometrics (Architecture -> Economics Transition)  
**Status:** Initialization (Level 0)

---

## 🚀 Phase 1: 环境搭建 & Hello World (1-2 周)
> **目标：** 只要能把 Python 打开，跑通第一行代码

### 1.1 安装：Anaconda

* **下载：** 去 [Anaconda 官网](https://www.anaconda.com/) 下载个人版。
* **为什么：** （常用的库：Pandas, NumPy, Matplotlib）

### 1.2 工作台：Jupyter Notebook
安装完 Anaconda 后，找到 **Jupyter Notebook** (或者 **JupyterLab**) 图标，点击打开。
* **它是什么：** 它不是黑乎乎的命令行，它像一本**交互式的笔记本**。
* **怎么用：** 在网页里写代码，按 `Shift + Enter`，结果直接在下面显示。可以写笔记、贴图片、画公式，非常适合我们这种“视觉系”动物。
* **第一行代码：**
    ```python
    print("Hello, Economist Ludan!")
    ```
    *(看到这句话打印出来，Phase 1 就通关了！)*

---

## 📊 Phase 2: 数据积木 (Pandas) (核心中的核心)
> **目标：** 像玩乐高一样处理 Excel 表格。这是未来 80% 的工作内容。

### 2.1 核心库：Pandas (`import pandas as pd`)
不要去学怎么用 Python 写贪吃蛇。只学 Pandas。
* **读取数据：** `df = pd.read_excel('my_data.xlsx')` —— 一行代码顶替 Excel 打开文件的过程。
* **看数据：** `df.head()` —— 看看前 5 行长啥样。
* **筛选：** `df[df['age'] > 60]` —— 找出所有 60 岁以上的患者。
* **统计：** `df.describe()` —— 一秒钟算出所有变量的平均值、标准差。

### 2.2 必修概念
* **DataFrame:** 就是 Python 里的 Excel 表格。
* **Series:** 表格里的一列。
* **Index:** 表格的行号。

**🚧 练习作业：**
找一个手边的 Excel 表格（比如播客的听众数据，或者你记账的表），用 Pandas 读取它，算出平均值。

---

## 🎨 Phase 3: 视觉化与初步绘图 (Matplotlib & Seaborn)
> **目标：** 只有画出图，才能直观看到“趋势”。利用建筑学审美！

### 3.1 基础绘图 (`import matplotlib.pyplot as plt`)
* 最丑但最基础的库。先学会画散点图 (Scatter Plot) 和折线图 (Line Plot)。

### 3.2 进阶美化 (`import seaborn as sns`)
* **神器！** 它可以画出你在 *The Economist* 杂志上看到的那种高级统计图。
* **核心图表：**
    * `sns.histplot()`: 直方图（看数据分布，比如收入是不是正态分布）。
    * `sns.boxplot()`: 箱线图（看有没有离群值，药企非常看重这个）。
    * `sns.regplot()`: 自动给你画出散点图 + 回归拟合线（瞬间感觉像经济学家了）。

---

## 📈 Phase 4: 武器库 —— 计量经济学 (Statsmodels)
> **目标：** 不再只是“看图说话”，而是给出“P值”和“置信区间”。

### 4.1 像 Stata 一样思考 (`import statsmodels.api as sm`)
这是你做 HEOR 研究的终极武器。
* **OLS 回归 (最重要)：**
    ```python
    # 假设 y 是健康状况，X 是药品剂量
    X = sm.add_constant(X) # 加上截距项（别问，加就是了）
    model = sm.OLS(y, X).fit()
    print(model.summary())
    ```
* **看懂 `summary()`：**
    * **Coef (系数):** 吃这个药，健康值增加多少？
    * **P>|t| (P值):** 这个结果是瞎猫碰死耗子吗？（要小于 0.05）
    * **R-squared:** 模型解释力度有多大？

---

## 📚 资源 

1.  **B 站/YouTube 搜索关键词：** "Python Pandas 数据分析 教程" (找播放量高的，哪怕是教做股票分析的也行，逻辑是一样的)。
2.  **书（案头备查）：** 《利用 Python 进行数据分析》(Python for Data Analysis) —— 作者就是 Pandas 的亲爹 Wes McKinney。不用全看，当字典查。
3.  **练习场：** Kaggle (如果不急，先不用碰，但我后面会带你做一些小项目)。

---

## 🗓️ Next Action Items (Ludan's To-Do)

- [ ] **Day 1:** 下载并安装 Anaconda。成功打开 Jupyter Notebook。
- [ ] **Day 2:** 搞懂 `print("Hello World")` 和 `1 + 1` 等于几。
- [ ] **Day 3:** 找个 Excel 文件，试着用 `pd.read_excel()` 读取它。
