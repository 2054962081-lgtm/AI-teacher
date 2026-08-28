# 苏格拉底式启发教学 Agent 👉 [在线查看作品集](./index.html)

面向数学辅导场景的 AI Agent 项目，通过 **题目检查、逻辑求解、学生状态识别、文本情绪识别、教学策略控制** 等结构化节点，实现分步启发式教学与多轮互动。

## 项目结构

```text
AI-teacher/
├─ index.html                     # 在线作品集
├─ AI产品经理作品集_苏格拉底式启发教学Agent.pdf   # PDF 作品集
└─ README.md                      # 项目说明
```

## 启动项目
https://www.coze.cn/store/agent/7603941188114382848?bot_id=true

## 核心工作流

```text
图片 / 文本输入
      ↓
Question_Check
      ↓
Logic_Solver
      ↓
Student_State
      ↓
Emotion
      ↓
Teaching_Strategy
      ↓
Response
      ↓
Context
```

### 节点职责

- **Question_Check**：提取题目结构并判断可解性
- **Logic_Solver**：生成标准答案、解题方法与完整步骤
- **Student_State**：判断学生当前理解程度和卡点
- **Emotion**：识别文本中的犹豫、畏难、挫败等情绪信号
- **Teaching_Strategy**：决定追问、提示、纠错或任务拆分
- **Response**：生成最终学生可见回复
- **Context**：记录已完成步骤与下一轮目标

## 核心设计

### 1. 解题与教学分离

`Logic_Solver` 负责内部完整求解，`Teaching_Strategy` 根据学生当前状态决定本轮展示的信息量。

### 2. 状态与情绪独立控制

- **Student_State** 控制教学难度
- **Emotion** 控制回复语气

### 3. 分级提示策略

```text
一级提示：关注题目条件
二级提示：提示数量关系或知识点
三级提示：帮助完成局部推导
解释兜底：解释关键步骤
```

## 项目工作

- 完成数学辅导场景问题拆解与产品方案设计
- 设计 Agent 整体工作流及节点职责
- 定义 Question_Check、Logic_Solver 等结构化输出字段
- 设计学生状态与文本情绪双控制机制
- 设计分级提示与多轮上下文更新策略
- 基于 Coze 完成核心工作流搭建
