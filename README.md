# Agent_LangGraph

一套**离线优先、可运行**的 LangGraph（Python）学习 notebook。

## 快速开始

- **版本**：本教程基于 `langgraph==1.2.5`
- **安装依赖**：

```bash
pip install -r references/Agent_LangGraph/requirements.txt
```

- **运行**：按顺序打开 `references/Agent_LangGraph/notebooks/` 下的 notebook，建议从 `01` 开始一路 Run All。

## 学习顺序（建议按编号）

- `01_从零理解LangGraph.ipynb`：State/Node/Edge/Graph 的最小心智模型
- `02_State深入：数据怎么流转.ipynb`：Reducer、并发写冲突、superstep 等
- `03_条件路由模式.ipynb`：条件路由（`add_conditional_edges` vs `Command`）与典型模式
- `04_Checkpointer与State管理.ipynb`：Checkpointer + `thread_id`、`get_state/update_state/get_state_history`、时间旅行
- `05_Human-in-the-Loop.ipynb`：`interrupt()` / `Command(resume=...)` 与 4 种 HIL 模式
- `06_Streaming：让执行过程可见.ipynb`：`stream`/`stream_mode` 与 `stream_events(v3)`（用于 UI/调试）
- `07_Store与长期记忆.ipynb`：Store（长期记忆）与 checkpointer（会话记忆）的分工
- `08_Subgraphs：把大图拆成模块.ipynb`：子图拆分与复用（两种通信方式）
- `09_Fault tolerance：超时、重试与错误处理.ipynb`：重试/超时/错误兜底/优雅停止与恢复
- `10_工程化：测试、可观测、部署.ipynb`：最小测试闭环、可观测、本地服务化与部署路径
- `11_加餐：补齐基础拼图（Functional API、Send、缓存、递归限制）.ipynb`：Functional API、Send/并行、Node caching、recursion_limit、Overwrite、Private state、Pydantic schema

## 参考（官方）

- [LangGraph 文档首页](https://docs.langchain.com/oss/python/langgraph/)
- [Graph API](https://docs.langchain.com/oss/python/langgraph/graph-api)
- [Use Graph API](https://docs.langchain.com/oss/python/langgraph/use-graph-api)
- [Interrupts](https://docs.langchain.com/oss/python/langgraph/interrupts)
- [Streaming](https://docs.langchain.com/oss/python/langgraph/streaming) / [Event streaming](https://docs.langchain.com/oss/python/langgraph/event-streaming)
- [Persistence](https://docs.langchain.com/oss/python/langgraph/persistence) / [Checkpointers](https://docs.langchain.com/oss/python/langgraph/checkpointers) / [Stores](https://docs.langchain.com/oss/python/langgraph/stores)
