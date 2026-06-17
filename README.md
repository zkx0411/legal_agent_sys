# legal_agent_sys
## 融合多Agent与RAG的法律知识服务系统，结合可视化流程组件对案件流程进行操作管理

### 多Agent采用两层设计
#### 第一层（决策层）：
    可以根据需求切换速度快或者功能全的Agent，负责信息的处理以及任务拆分发布
    quick_agent基于检索增强生成和联网搜索的智能体
    chat_agent在quick_agent的基础上添加了任务拆分思考过程，且提供文书生成下载
    work_agent相对于chat_agent新增了查询数据库功能

#### 第二层（执行层）：
    由专项Agent组成执行具体任务
    vector_store负责RAG相关的处理，从本地知识库检索信息
    search_agent联网搜索，是本地知识库未检索到时的保底机制
    agent_executor负责查询数据库内相关的信息

### 项目内的API_KEY已全部删去，如需使用请自行替换config.py以及.env内的值
