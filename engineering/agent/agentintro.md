

# abstract

目前的agent开发作为新一轮ai热潮，梳理清楚主要脉络能够帮助我们更好的学习，但是agent开发知识零碎，没有系统的知识，所以我制作了一个agent的简要综述。我想根据自己的调查不仅让大家的知识更宽泛，而且更有深度



# llm

agent首先是围绕llm构建出来的工程件，要理解agent首先一定要对llm有个系统的了解

## llm架构

decoder-only 架构

MoE架构

## 模型训练

1.模型预训练

2.模型中训练

3.模型后训练

# agent

首先是一个agent应该有的框架[1]

memory       planning&reasoning

​		llm core

​	        tools

​		tool call                           ops



harness     sandbox   session[2]

> pet / cow

> memory为了让llm拥有能够识别的记忆，短期记忆，长期记忆，技巧记忆

planning&reasoning：

思考的越多结果越好：

1.信任问题                               2.bad plan                           3.good plan fail to implement

react框架，reasoning->action->reasoning...

reflexion

通过实际调用的工具来判断整个是不是

React框架

缺陷：

1. 一直陷入loop->设置最大量

2. 

改进：



agent的历史



memory的几个：

1.日常感知的记忆



2.整体的感觉的记忆

通过日常的信息进行总结，形成一个整体观念

> 问题印象一旦产生很难消除

3.特殊技能的记忆

> 使用tool library构建的，然后根据需求更新tool

tool call

​     怎么训练使用tool，让llm自己加toolcall，如果对结果有用就留下来。

​    特别多的tool，通过有用的数据训练一个goralla-27B这个其实没怎么看懂

1.system architecture

2.datasets

3.eval

> first thing to do is build 50-100 tests,to let you know what is good.



workflow vs  agent

RAG

MCP



## llm的不能知道你自己的知识

RAG

## llm不能接触外界环境

tool use& function calling

## 多个agent如何共同协作





ref：

[1]CS329z:

1.Lecture 1: Foundations & Landscape

2.Lecture 2: LLMs for Builders

3.Lecture 3: RAG + Agents 

4.Lecture 4: Tool Use & Function Calling 

5.Lecture 5: Frameworks & Agent Design

6.Lecture 6: Agent Design Patterns & Scaffolds

7.Lecture 7: Agent Memory Architectures

8.Lecture 8: Multi-Agent Systems

9.Lecture 9: Optimization

[2]大厂agent500问绿皮书：

1.模型架构

2.工具管理

3.容错与鲁棒性

4.记忆与上下文

5.评估与全局观

6.多智能体协作

7.工程化踩坑

8.prompt工程与框架原理

9.RAG与检索系统

10.训练数据与模型优化

11.AI代码分析与测试

12.业务ai工程分析

13.简历项目拷打

14.面试偏好

15.概念考察

16.agent infra

17.ai infra

[3]深入理解 AI Agent

1.AI Agent入门

2.上下文工程

3.用户记忆和知识库

4.工具

5.coding agent

6.agent评估

7.模型后训练

8.agent的持续进化

9.多模态与实时交互

10.多agent协作

[4]ai实战手册

第 1 章：AI Agent 基础概念

第 2 章：从零手写 ReAct Agent

第 3 章：LangGraph 图编排实战

第 4 章：CrewAI 多智能体协作

第 5 章：AutoGen / Microsoft Agent Framework 对话驱动

第 6 章：LlamaIndex RAG 知识库

第 7 章：Dify 低代码可视化平台

第 8 章：OpenAI Agents SDK

第 9 章：Claude Agent SDK

第 10 章：Mastra TypeScript Agent

第 11 章：MCP 协议完全指南

第 12 章：Ollama 本地大模型部署

第 13 章：多 Agent 协作模式详解

第 14 章：记忆系统与状态管理

第 15 章：Token 成本优化策略

第 16 章：调试、监控与可观测性

第 17 章：全栈实战——研究报告生成系统

第 18 章：选型决策树与最佳实践

第 19 章：Agent 通用工具箱 — 与框架无关的公共设施

第 20 章：OpenAI Codex CLI — 从终端到生产

第 21 章：DeepSeek Harness（dsh）— 2026 年度最具潜力的开源 Agent 第 22 章：Continue 编辑器 — 让 VSCode / JetBrains 变成 AI 编码助手

第 23 章：Aider 代码助手 — 终端里的 AI 编程伙伴

第 24 章：Trae IDE — 字节跳动的 AI 原生开发环境

第 25 章：Harness Engineering 驾驭工程 — 2026 年 Agent 的核心竞争力

第 26 章：Agent Skills 编写实战 — 把你的经验打包成一个文件

第 27 章：上下文工程（Context Engineering）— 在有限注意力里做取舍

第 28 章：2026 热门项目全景 — 六大顶流与本书的串联地图

第 29 章：Agent 经济与商业化 — 当 Agent 学会花钱和赚钱

[5]大模型基础

1.语言模型基础

2.大语言模型架构

3.prompt工程

4.参数高效微调

5.模型编辑

6.检索增强生成

[6]claude managed agents with opus 5.5



