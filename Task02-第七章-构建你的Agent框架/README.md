# Task02: 第七章 构建你的 Agent 框架

> **打卡状态**：✅ 已完成（交付物已归档）  
> **任务要求**：习题；笔记；视频

---

## 📂 本阶段交付物导航

- 📖 **[核心学习笔记（点击查看）](./学习笔记.md)**
  - 自建 Agent 框架的必要性与商业框架四大局限
  - HelloAgents 核心设计哲学：“万事万物皆为工具”
  - `HelloAgentsLLM` 扩展体系与自动检测（Auto-Detection）
  - 核心接口三层架构：`Message` (Pydantic)、`Config` (单例模式)、`Agent` (模板方法模式)
  - 经典范式框架化与工具系统（ToolRegistry / ToolChain / 异步执行器）
  - 互动思考题深度解析

- 📝 **[课后习题解答（点击查看）](./习题解答.md)**
  - 包含本章全部 6 道大题的高质量工程级解答：
    1. 框架局限性剖析与“万物皆为工具”优劣
    2. 继承扩展新提供商代码示例 & VLLM/SGLang/Ollama 推理引擎对比
    3. 设计模式与数据契约分析（模板方法模式、单例模式）
    4. ReActAgent 框架化改进、质量评分反思机制、Tree-of-Thought (ToT) 智能体类设计
    5. 工具系统接口统一原则、工具链场景与异步执行边界
    6. 流式输出改造、多轮对话时空回溯树与第三方插件系统架构

---

## 🧪 本地代码实测验证记录

本地已安装 `hello-agents==0.1.1` 并全部测试通过（均由阿里魔搭 ModelScope `Qwen/Qwen3.5-27B` 强力驱动）：
- ✅ `my_main.py`：自定义 ModelScope Provider 调用成功
- ✅ `test_my_calculator.py`：自定义扩展计算器工具测试通过
- ✅ `test_simple_agent.py`：基础对话、工具调用、流式生成全通过
- ✅ `test_react_agent.py`：复合推理与行动循环全链路通过
