# Building-Secure-and-Reliable-Systems-Chinese
Building Secure and Reliabble Systems  Google 系统架构解密 构建安全可靠的系统

[English](https://google.github.io/building-secure-and-reliable-systems/raw/toc.html)

# 第一章 安全性与可靠性的交集
## 1.1 从密码和电钻谈起  
## 1.2 可靠性与安全性：设计注意事项  
## 1.3 机密性、完整性、可用性  
### 1.3.1 机密性  
### 1.3.2 完整性  
### 1.3.3 可用性  
## 1.4 可靠性与安全性：共性  
### 1.4.1 隐形  
### 1.4.2 评估  
### 1.4.3 简洁性  
### 1.4.4 演变  
### 1.4.5 弹性  
### 1.4.6 从设计到生成  
### 1.4.7 调查系统与日志  
### 1.4.8 危机响应  
### 1.4.9 恢复  
## 1.5 小结
# 第二章 了解攻击者
## 2.1 攻击者发动机
## 2.2 攻击者画像
### 2.2.1 业余爱好者
### 2.2.2 漏洞研究人员
### 2.2.3 黑客活动家
### 2.2.4 犯罪份子
### 2.2.5 自动化和人工智能
### 2.2.6 内部人员
## 2.3 攻击者方法论
### 2.3.1 威胁情报
### 2.3.1 网络杀伤链
### 2.3.1 TTP
## 2.3 风险评估注意事项
## 2.3 小结
# 第三章 示例分析： 安全代理
## 3.1 生成环境中的安全代理    
## 3.2 Goolge 工作代理    
## 3.3 小结    
# 第四章 设计中的权衡  
## 4.1 设计的目的和要求
### 4.1.1 特性需求
### 4.1.2 非功能性需求
### 4.1.3 功能与涌现特性
### 4.1.4 案例：Google 的设计文档
## 4.2 需要平衡
## 4.3 处理紧张局势
### 4.3.1 案例：微服务和Google Web应用程序框架
### 4.3.1 统一涌现特性的需求
## 4.4 初始速度与持续速度
## 4.5 小结
# 第五章 最小特权设计  
## 5.1 概念和术语  
### 5.1.1 最小特权  
### 5.1.2 零信任网络  
### 5.1.3 零接触  
## 5.2 基于风险的访问分类  
## 5.3 最佳实践  
### 5.3.1 API 功能最小化  
### 5.3.2 Breakglass 机制  
### 5.3.3 审计  
### 5.3.4 测试和最小特权  
### 5.3.5 诊断被解决的访问  
### 5.3.6 优雅失败和 Breakglass 机制  
## 5.4 工作案例：配置分发  
### 5.4.1 基于 OpenSSH 实现的POSIX API  
### 5.4.2 软件更新API 
### 5.4.3 自定义 OPENSSH ForceCommand  
### 5.4.4 自定义 HTTP 接收器 (边车)  
### 5.4.5 自定义 HTTP 接收器 （内置）  
### 5.4.6 权衡取舍    
## 5.5 一种基于认证和授权决策的策略框架  
### 5.5.1 使用高级授权控件 
### 5.5.2 投入广泛使用的授权框架 
### 5.5.3 避免潜在的陷阱 
## 5.6 高级控制  
### 5.6.1 MPA  
### 5.6.2 3FA  
### 5.6.3 业务数据  
### 5.6.4 临时访问  
### 5.6.5 代理  
## 5.7 权衡与冲突  
###  5.7.1 增加了安全复杂性 
###  5.7.2 对合作商及公司文化的影响 
###  5.7.3 影响安全性质量数据和系统 
###  5.7.4 对用户工作效率的影响 
###  5.7.5 对开发复杂性的影响 
## 5.8 小结    
# 第六章 面向易理解性的设计 
## 6.1 为什么易理解性很重要 
### 6.1.1 系统不变量
### 6.1.2 分析不变量
### 6.1.3 心智模型
## 6.2 设计易理解的系统 
### 6.2.1 复杂性与易理解性
### 6.2.2 分解复杂性
### 6.2.3 集中负责安全性和可靠性需求
## 6.3 系统架构 
### 6.3.1 易于理解的接口规范 
### 6.3.2 易于理解的身份、认证和访问控制 
### 6.3.3 安全边界  
## 6.4 软件设计 
### 6.4.1 使用应用程序框架满足服务需求
### 6.4.2 理解复杂的数据流
### 6.4.3 考虑API的可用性
## 6.5 总结 
# 第七章 适应变化的设计 
## 7.1 安全变更的类型  
## 7.2 变更中的设计  
## 7.3 让发布更容易的架构决策  
## 7.4 不同的变更：不同的速度与不同的时间线  
## 7.5 难点：计划调整  
## 7.6 不断扩大的范围：心脏滴血漏洞  
## 7.7 小结  
# 第八章 弹性的设计  
## 8.1 弹性设计原则  
## 8.2 纵深防御  
## 8.3 控制降级  
## 8.4 控制爆炸半径  
## 8.5 故障域和冗余   
## 8.6 持续验证   
## 8.7 实践建议：着手点   
## 8.8 小结   
# 第九章 面向恢复性的设计  
## 9.1 要恢复什么  
## 9.2 恢复机制的设计原则
## 9.3 紧急访问
## 9.4 预期外的收益
## 9.5 小结
# 第十章 缓解拒绝服务攻击 
## 10.1 攻防双方策略 
## 10.2 面向防御的设计 
## 10.3 缓解攻击 
## 10.4 应对源于服务本身的 “攻击” 
## 10.5 小结 
# 第十一章 案例分析: 设计、实现和维护一个可信任的公共CA  
# 第十二章 编写代码  
# 第十三章 代码测试  
# 第十四章 部署代码  
# 第十五章 调查系统  
# 第十六章 防灾规划  
# 第十七章 危机管理  
# 第十八章 恢复和售后  
# 第十九章 案例研究：Chrome 安全团队  
# 第二十章 理解角色和责任  
# 第二十一章 建立安全可靠的文化  
# 总结  
# 附录 灾难风险评估矩阵  