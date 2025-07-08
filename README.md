## 成果展示 (Results Showcase)

*以下所有图表均为真实实验数据生成，从多个维度展示了我们方法的有效性、高效性和创新性。*

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
可视化结果清晰地揭示了我们模型的智能之处。传统方法机械地选择了网络中度数最高的几个“集散中心”（Hubs）。而我们的模型不仅能识别这些Hub，还能更精准地定位到那些连接不同社群、在信息传播中扮演 **“结构性桥梁”** 角色的关键节点，可视化结果也为模型的决策提供了**良好的可解释性**。
