# 多AGENT协同

crewai module



1.构建agent

2.设置task

3.组件crew



## 1.如何构建agent

构建agent方法

```python
Agent(
	role = ...
	# 智能体的工作内容及其专长领域
	goal=...
	backstory=...
    tool=[]
    verbose=...
    allow_delegation=bool,
    llm=...
    )
```

***

怎么样构建一个好的role：

1. 具体且专业
2. 与现实职业保持一致：基于公认的专业原型来确定角色
3. 包含领域专场：指定智能体的知识领域

***

怎么样构建一个好的goal：

1. 明确且以结果为导向：定义试图实现的目标
2. 强调质量标准：包含对工作质量的期望
3. 纳入成功标准：帮助智能体理解什么是好的成果

***

怎么样构建一个好的backstory：

1. 建立专长和经验：解释智能体是如何获得技能的
2. 定义工作风格和价值观：描述智能体处理工作的方式
3. 创造连贯的人格：确保背景故事的所有元素与角色和目标保持一致

***

专家优于通才

> 怎么创建一个llm实例：
>
> ```python
> from langchain.openai import ChatOpenAI
> llm = ChatOpenAI(model="Qwen/Qwen3.5-4B",base_url,api_key)
> ```

***

```python
Task(
	desciption=...
    expecter_output=...
    agent=...
    context=...
)
```

***

怎么样写一个好的task：

1. 任务专注于一个明确的目标，表现最好
2. 明确输入和输出
3. 包含目的和上下文
4. 使用结构化输出工具：json...

***

```python
tasks=...
crew=Crew(
	agents=...
    tasks=...
    process=...
    verbose=...
    memory=...
)
crew.kickoff()
```

crew的两种工作模式：

hierarchical:层级的

manager+workers

使用

```python
manager_agent=manager
```

指定哪个agent是管理者

***

并行执行：

sequential：序列的

虽然没有这种直接设置并行的

但是可以直接设置sequential

***

## 集成工具



























































