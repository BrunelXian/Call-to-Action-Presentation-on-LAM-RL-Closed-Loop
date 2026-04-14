# 面向TWI的LAM-RL-Agent Presentation 的延申材料和文档仓库
本仓库用于集中存放一套面向 `TWI` 的个人汇报材料，包括演示文稿、研究计划书，以及为形成该叙事所做的背景调查与分析笔记。
本Readme主要为宣讲人提供一个简单的背景介绍，而非项目介绍。
项目介绍的具体内容在Slides中。
本项目居然是我手搓的你干信，我居然还干上了古法编程！！

<h1 align="center">LAM-RL-Agent Presentation for TWI call-to-action
   <p>延申材料和文档仓库</h1>

![project](https://img.shields.io/badge/project-industrial_AI-blue)
![focus](https://img.shields.io/badge/focus-adaptive_optimisation-orange)
![domain](https://img.shields.io/badge/domain-LAM-green)
![scope](https://img.shields.io/badge/scope-process_control-lightgrey)
![method](https://img.shields.io/badge/method-reinforcement%20learning--based-yellow)

## 核心阅读重点

本仓库最重要的两条背景主线是：

1. **TWI 近两年的投资意向与技术布局**
2. **TWI 与其他高校在 AI 方向的合作现状**
3. 针对TWI和EPSRC的不同听众的术语调整

之所以把这两点写在Readme，是因为本项目并不是单纯从“学术上 AI 很先进”出发，而是试图回答一个更现实的问题：

```
ApaAdaptive closed-looped agent 在商业上有更大的价值 
```
---

## 重点背景判断

### 1. TWI 的投资意向与战略偏好

主要依据：
1. TWI的收入主要46%来自于咨询服务，而非企业会员费。所以更看重技术转化为**工业咨询服务**的能力。

2. TWI的计划路线图中，技术向投资只有两条
   - 优先加大氢能与能源转型技术投资 
   - **加速AI/ML与数字化NDT/监测技术**
 并在第二条中重点说明了投资智能检查系统、自动化机器人焊接及增材制造验证。通过软件许可创造 recurring revenue。

主要结论：
目前Slides的V4.0之后的版本的核心目标
```
从展现 **技术** →展现**增强其高附加值工程服务能力**
```
那么它对 TWI 的战略意义通常会高于单纯的学术展示型研究。

Ref：
[TWI的财报与RoadMap原帖](research/01-twi-investment-and-strategy/TWI财务报表与技术路线图相关链接.md) --  [TWI的收入结构与投资分析](research/01-twi-investment-and-strategy/TWI收入结构与投入分析.md)  --  [TWI的投资偏好于项目匹配分析](research/01-twi-investment-and-strategy/TWI的投资偏好与项目匹配分析.md)

---

### 2. TWI 与高校 AI 合作的现状及其局限

#### 2.1 TWI和 高校AI的合作汇总

##### 关于LAM AI的合作：

1. **AMIC（Additive Manufacturing Innovation Centre）**

和 **Lancaster University** 联合建立的研究中心. 
   
目前披露的方向：Digital Twin driven monitoring和 AM process modelling [Ref](https://www.twi-global.com/innovation-network/centres/innovation-centres/additive-manufacturing-innovation-center "AMIC Ref.")

2. **Applied Artificial Intelligence Innovation Centre**

和 **University of Huddersfield** 合作的研究中心

2025年成立，规划阶段，目标是  Autonomous systems + AI decision systems. [Ref](https://www.bindt.org/News/february-2025/university-of-huddersfield-and-twi-partner-on-strategic-rd)

3. 关于其他方向的AI合作：

只有无所检测，目前有个课题组就是 AI and Machine Learning in NDT [Ref](https://theweldinginstitute.com/insights/13447592)

技术路线是，对于pipeline： NDT data → ML classifier → defect detection

**结论**：
TWI 已公开的一些 AI 合作与相关活动，主要包括：
- 面向增材制造的 AI / machine learning 监测与建模
- 面向智能制造的数据分析与制造洞察
- 面向无损检测（NDT）的缺陷识别与分类
它们说明 TWI 已经意识到 AI 在制造中的潜力，并且已经开始布局。

[关于TWI的AI项目的情报汇总.md](research/02-twi-ai-collaborations/关于TWI的AI与增材制造项目的情报汇总.md)

#### 2.2 目前TWI的AI方向的分析与经验吸取

从当前公开信息来看，这些工作大多仍停留在如下技术链条：

`sensor -> model -> prediction`

这类方法可以提高可见性、辅助分析、改善监测，但其工业价值仍主要集中在“解释信号”“预测结果”这一层。

本仓库所项目强调的关键技术缺口，是更进一步的能力：

`传感器 -> 状态估计 -> 决策 -> 安全范围内的实时工艺调整`

换句话说，当前很多已公开的 AI 路线，本质上仍然偏向于用神经网络去拟合信号、做缺陷预测或做事后解释；但如果这些结果无法进入 **自适应优化（adaptive optimisation）** 或 **安全约束下的实时调节**，其对高价值制造流程的决策意义仍然有限。

因此，本仓库更倾向于将该方向表述为：

**adaptive process stabilisation（自适应过程稳定化）**

而不是简单地表述成“AI control”。

[TWI 技术采用逻辑与 Adaptive Optimisation 的定位](research/03-pitch-positioning/TWI 技术采用逻辑与 Adaptive Optimisation 的定位.md)

### 3. 面向不同对象的术语调整

与Proposal不同，TWI的听众更偏向工业应用：

- **弱化 AI 术语本身，强化制造价值**
- 叙事重点从 **monitoring** 推进到 **process understanding**，再推进到 **adaptive optimisation**
- 将该方向包装为 **现有工业能力的增强与升级**，而不是高风险的技术颠覆

这样做的原因很直接：对 TWI 而言，更有说服力的不是“算法本身多先进”，而是这项工作是否能够形成工业能力、服务价值、部署路径和长期战略意义。

详细参考：[1](archive/(ARCHIVED) TWI Presentation V7.0.md) - [2](archive/(ARCHIVED) V5.0 关于风险技术的表达.md) - [3](archive/(ARCHIVED) 为什么Presentation to TWI V4.0版本的不好.md) - [4](archive/(ARCHIVED) 关于淘汰V7.0 的想法.md) - 

---

## 仓库内容

本仓库目前包含三层材料：

1. **Presentation**
   面向 TWI 的 call-to-action 演示文稿。
2. **Proposal**
   支撑该方向的研究计划书与技术说明。
3. **Background Research**
   用于支撑叙事和判断的背景资料，包括 TWI 的战略、财务结构、AI 合作现状以及项目定位逻辑。

---

## 仓库结构

当前仓库结构如下：

```text
/
|-- README.md
|-- Presentation to TWI v8.0.pptx
|-- EPSRC AI-LAM Proposal 4th Draft.docx
|-- research/
|-- archive/
```

各部分用途如下：

- 仓库根目录存放当前版本的 presentation 与 proposal
- `research/` 存放按主题分类的背景调查材料
- `archive/` 存放已淘汰的叙事版本与历史草稿

---

这里是一个小尾巴。

🟨 正宗老代码

┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ 🟥 坚持手写┃🟨 拒绝 AI ┃🐒😂（抱着键盘）┃
┃🟦纯手工 ┃🟥硬核┃ 🟦夜编程 ┃🔴0% AI 添加┃
┃ 🟦 是老派的┃🟥 无 Bug ┃     ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

