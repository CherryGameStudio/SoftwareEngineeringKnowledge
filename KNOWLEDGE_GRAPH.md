# 🗺️ 全局知识关联图

> 本图汇总所有笔记中的"关联知识"，展示知识间的交叉与依赖关系。
> 每次新增或更新笔记的"关联知识"时，请同步更新此图。

## 知识关联全景

```mermaid
graph LR
    subgraph 编程基础
        编程语言
        数据结构与算法
        设计模式
        编程范式
    end

    subgraph 开发工具链
        Git
        构建工具
        包管理器
    end

    subgraph 系统与运维
        Linux
        Docker
        CI-CD[CI/CD]
        云服务
    end

    subgraph 网络与安全
        计算机网络
        HTTP
        TCP-IP[TCP/IP]
        DNS
        Web安全
    end

    subgraph 数据管理
        MySQL
        Redis
        MongoDB
        消息队列
    end

    subgraph 架构与设计
        系统设计
        微服务
        分布式系统
        API设计
    end

    subgraph 工程实践
        测试
        代码质量
        项目管理
    end

    %% === 知识关联 ===
    %% 随笔记增长不断扩充，格式：A -->|关系| B

    Docker -->|依赖| Linux
    Docker -->|用于| CI-CD
    Git -->|用于| CI-CD
    HTTP -->|基于| TCP-IP
    微服务 -->|使用| Docker
    微服务 -->|使用| API设计
    微服务 -->|需要| 消息队列
    Redis -->|用作| 缓存[缓存]
    测试 -->|保障| 代码质量
    设计模式 -->|指导| 系统设计
    编程语言 -->|实现| 数据结构与算法
    分布式系统 -->|依赖| 计算机网络
    云服务 -->|基于| 分布式系统
```

## 如何更新

1. 在笔记的**"关联知识"**部分添加新的关联
2. 回到本文件，在 `%% === 知识关联 ===` 下方添加新的连线
3. 格式：`A -->|关系描述| B`
4. 提交时在 commit message 中注明更新了关联图
