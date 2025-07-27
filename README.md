### <strong>TIG-IM</strong>

<p>
大家好！本项目是我当前正在进行的一项学术研究的核心实现，聚焦于通过图神经网络（GNN）建模复杂网络结构，并高效识别其中的重要节点，具有较高的理论价值和应用潜力。
摘要—在复杂网络中识别关键节点是一项具有挑战性的任务，需在效率、准确性与冗余消除之间取得平衡。为此，本文提出了一种基于图神经网络的两阶段归纳式影响力最大化框架 TIG-IM。第一阶段中，构建多任务学习的全局评分器，利用图注意力网络（GAT）同时预测SIR传播得分与我们新提出的三维桥接中介中心性，以高效筛选跨社区桥接节点构成候选集。第二阶段中，引入融合度惩罚与多样性正则项的局部选择器，在候选子图上进行再排序，生成结构分散且传播能力互补的最终种子集。理论分析证明评分器满足单调性，其局部损失函数可视为最大后验估计（MAP）。该框架具备近线性时间复杂度 𝑂(𝑛+𝑚)。在九个不同领域的真实网络上进行的实验结果表明，TIG-IM在传播效果和计算效率方面显著优于多种先进方法。消融实验进一步验证了三大核心模块（3D桥接中心性、度惩罚、多样性重排序）间的协同增益。
</p>

---

<table>
  <tr>
    <td valign="top" width="50%">
      <h4 style="margin-top:0;">📌 当前进展 (Current Status)</h4>
      <p>
      我们计划于 <strong>2025年8月</strong> 完成全部实验，并正式提交论文。
      </p>
      <p>
      出于对未公开研究成果的保护，完整源代码目前存储于私有仓库中。我们将在论文接收完成后正式开源全部实现。
      </p>
    </td>
    <td valign="top" width="50%">
      <h4 style="margin-top:0;">🤝 合作与交流 (Collaboration & Access)</h4>
      <p>
      若您对该项目感兴趣，欢迎通过邮件与我联系。无论您希望进行代码审阅、技术交流，还是借鉴实现方法，我都将非常乐意在确认用途后，提供项目代码的限时访问权限，以支持更多科研合作与学习交流。
      </p>
      <p>
      📧 <strong>联系邮箱</strong>: <code>2428389368@qq.com</code>
      </p>
    </td>
  </tr>
</table>
</div>

## 成果展示 (Results Showcase)

*以下所有图表均为真实实验数据生成。*

---

### **1. 算法有效性：多网络影响力传播对比 (SIR模型)**

为了验证我们模型的性能和泛化能力，我们在多个不同类型的真实世界网络上进行了影响力扩散实验。

<table align="center">
  <tr>
    
  </tr>
  <tr>
    <td>
      <img src="https://github.com/user-attachments/assets/061f9344-ed49-4f89-b273-edea277a44d3" alt="SIR Performance on USAir97" width="100%">
    </td>
    <td>
     <img src="https://github.com/user-attachments/assets/89be6ca0-d84e-467b-8bc7-8b533a252c5e" alt="Execution Time Comparison" width="100%">
    </td>
  </tr>
</table>

---
---

### **3. 节点选择策略可视化**

此图直观对比了传统“度中心性”和我们模型所选出的Top-K节点在 `NC` 网络拓扑上的位置。

<p align="center">
  <img src="https://github.com/user-attachments/assets/9941a562-0e61-4e66-af91-147554170a3a" alt="Top-K Node Visualization" width="80%">
</p>

**💡 分析与结论**:
传统方法通常选择网络中度数最高的几个“集散中心”（Hubs）。我们的模型不仅能识别这些Hub，还能更精准地定位到那些连接不同社群、在信息传播中扮演 **“结构性桥梁”** 角色的关键节点。
