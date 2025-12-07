# backend 目录说明

本目录为【后端服务】代码主目录，所有服务器端业务逻辑和配置均在此实现，供小程序端与 Web 管理后台使用。

## 主要结构

- config/         各类后台服务（数据库、Redis、OSS等）配置文件
- src/modules/    三级业务模块化实现（user, content, admin）
    - user: 用户/权限模块
    - content: 内容/评论/标签模块
    - admin: 管理后台相关API与数据统计
- src/middleware/ 通用服务中间件（如权限鉴权、敏感词过滤等）
- src/server.js   服务运行主入口

## 开发建议
- 编写代码时请根据功能划分对应子模块
- 所有公共能力建议以中间件方式实现以增强复用
- 配置项统一维护在 config/ 下
