# KeeperMind - 基于Memento-Agent的个人知识管理智能体

## 项目简介
KeeperMind是一个基于Memento-Agent智能体框架二次开发的轻量化个人知识管理系统，实现了文档导入、文本清洗、向量存储、语义检索、AI问答的核心链路，解决了个人学习中信息碎片化、检索效率低的问题。

## 技术栈
- **编程语言**：Python
- **智能体框架**：Memento-Agent
- **向量数据库**：ChromaDB
- **大模型API**：OpenAI API
- **工具协议**：MCP协议（Memento Control Protocol）
- **文档解析**：pypdf

## 核心功能
1. **多格式文档导入**：支持PDF、Markdown、纯文本文件的解析与清洗
2. **三层记忆架构**：基于Memento-Agent原生机制，实现短期、中期、长期记忆分层管理
3. **语义检索**：基于ChromaDB + OpenAI Embedding的向量相似度检索
4. **AI智能问答**：基于RAG（检索增强生成）的私有知识库问答

## 项目结构
KeeperMind/
├── .env.example              # 环境变量示例
├── .gitignore                # Git忽略文件
├── README.md                 # 项目说明
├── requirements.txt          # 依赖包
├── main.py                   # 项目入口
├── keepermind/               # 核心代码目录
│   ├── __init__.py
│   ├── agent/                # Agent模块
│   │   ├── __init__.py
│   │   └── keeper_agent.py   # 定制化知识管理Agent
│   ├── memory/               # 记忆模块
│   │   ├── __init__.py
│   │   └── three_layer_memory.py  # 三层记忆架构
│   ├── tools/                # MCP工具模块
│   │   ├── __init__.py
│   │   ├── document_tools.py # 文档解析工具
│   │   └── vector_tools.py   # 向量数据库工具
│   └── utils/                # 工具函数
│       ├── __init__.py
│       ├── config.py         # 配置管理
│       └── text_utils.py     # 文本清洗工具
└── tests/                    # 测试代码
    └── test_basic.py
