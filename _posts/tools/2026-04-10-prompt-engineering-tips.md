---
title: "Prompt Engineering 实用技巧总结"
date: 2026-04-10
topic: "工具与实践"
tags: [Prompt Engineering, LLM, 实战技巧]
---

Prompt Engineering 是与大语言模型高效交互的关键技能。本文总结了一些实用的技巧和最佳实践。

## 基本原则

### 1. 明确且具体

模糊的指令会导致模糊的结果。尽量在 prompt 中提供具体的要求：

```
# 不好的 prompt
帮我写一段代码

# 好的 prompt
用 Python 写一个函数，接收一个字符串列表，返回其中长度大于 5 的字符串，按字母排序
```

### 2. 提供上下文

给模型足够的背景信息，帮助它理解你的需求：

```python
# 在 prompt 中提供上下文的模板
context = """
项目背景：这是一个 Flask Web 应用
技术栈：Python 3.11, Flask 3.0, SQLAlchemy
需求：添加用户认证功能
约束：使用 JWT token，不使用 session
"""
```

### 3. Few-shot Learning

通过示例来引导模型输出格式：

```
输入：The movie was great
情感：正面

输入：I didn't like the service
情感：负面

输入：The weather is nice today
情感：
```

## 高级技巧

### Chain-of-Thought (CoT)

让模型分步思考，显著提升推理能力：

> 请一步一步思考这个问题，先分析已知条件，再推导结论。

### Role Prompting

为模型设定一个专业角色：

> 你是一位有 10 年经验的 Python 后端工程师，擅长系统设计和性能优化。

## 常见误区

| 误区 | 正确做法 |
|------|----------|
| prompt 越长越好 | 简洁明确，去掉冗余信息 |
| 一次性完成复杂任务 | 拆解为多个子任务 |
| 忽略输出格式 | 明确指定期望的输出格式 |
| 不迭代优化 | 根据结果持续调整 prompt |

## 总结

Prompt Engineering 是一项需要不断练习的技能。核心思路是：**明确目标、提供上下文、引导格式、迭代优化**。
