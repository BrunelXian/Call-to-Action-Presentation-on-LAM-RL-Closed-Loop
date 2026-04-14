---
date: 2025-11-29
tags:
  - EPSRC
  - LAM-AI
  - TWI
---
# 问题

意识到一个核心问题：

TWI 的业务模型是：
```
industrial membership organisation
```

他们的研究内容是，低风险，工业可接受，TRL高

他们关心

	工业客户是否愿意用
	设备是否安全
	TRL 是否可落地  
	是否能卖会员服务

所以他们更喜欢
- 可以提供过程可见性
- 不会直接干预设备运行

AI Control对于他们来说，错误的控制可能导致设备损坏


# 解决思路

## 表达方式的变化

**Closed-loop control** 更像是一个学院派概念，主要用于 **EPSRC 申请中的学术表述**。

在工业语境下，更合适的说法是：

> **adaptive process stabilisation**

他们的区别：

> Monitoring = 知道问题发生
> Adaptive optimisation =  防止问题发生


## 核心逻辑：

监控系统存在一个根本问题，检测到缺陷时通常已经晚了。
工业需求的不是更多传感器，是process stabilisation。

逻辑链：

```
monitoring → process understanding → adaptive control
```

## 工业中的类似案例

工业上存在很多adaptive optimisation
- CNC machining 
	- 根据cutting force调整feed rate和spindle speed
- semiconductor
	- 根据wafer temperature调整process power和gas flow


## 回答 TWI 的核心关注点

工业客户是否愿意用
	Adaptive optimisation 可以被定位为：
	**对现有工程实践的增强，而不是替代。**
	在工艺开发阶段，工程师本来就需要通过试错不断调整参数。
	Adaptive optimisation 只是提供一种 **数据驱动的参数优化工具**。

设备是否安全
	可以通过多层安全机制降低风险，例如：
		- 权限层级控制
		- 监控模式
		-有限自主优化
	系统只在 **安全范围（safe process envelope）内**进行优化，而不是直接控制机器。

TRL 是否可落地  
	Adaptive optimisation 不需要从低 TRL 开始。
	它可以在现有 **monitoring 系统的基础上逐步发展**。
	典型路径可以是：
		monitoring → process understanding → recommendation → adaptive optimisation

是否能卖会员服务
	在会员服务的商业模式上，有显著的优势。
	Monitoring 系统主要产生的是**数据**。数据本身难以商业化，而 **process know-how 是工业最有价值的资产**。
	因此 adaptive optimisation 更容易转化为：
		工艺优化服务
		参数开发服务
		AI 驱动制造解决方案
	这使其 **比 monitoring 更适合会员制商业模式。**

industry has already invested heavily in monitoring.  
The next challenge is how to use this information to stabilise the process.