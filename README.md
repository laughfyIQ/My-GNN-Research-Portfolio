### <strong>项目状态与源码访问说明</strong>

<p>
大家好！本项目是我当前正在进行的一项学术研究的核心实现，聚焦于通过图神经网络（GNN）建模复杂网络结构，并高效识别其中的重要节点，具有较高的理论价值和应用潜力。
</p>

---

<table>
  <tr>
    <td valign="top" width="50%">
      <h4 style="margin-top:0;">📌 当前进展 (Current Status)</h4>
      <p>
      我们计划于 <strong>2025年9月</strong> 完成全部实验，并正式提交论文。
      </p>
      <p>
      出于对未公开研究成果的保护，完整源代码目前存储于私有仓库中。我们将在论文投稿完成后正式开源全部实现。
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
