 # 项目框架

/backend
├── config/ # 统一配置（DB 密钥、端口等）
├── node_modules/ # 依赖包（自动生成）
├── src/
│ ├── common/ # 公共工具和常量（如API响应格式、错误代码等）
│ ├── middleware/ # 中间件
│ │ ├── auth.js # JWT 鉴权中间件（Backend A）
│ │ └── sensitiveFilter.js # 敏感词过滤（Backend B）
│ ├── models/ # 数据库模型定义（A/B共享）
│ │ ├── User.js # 用户模型
│ │ ├── Content.js # 内容模型
│ ├── modules/ # 业务逻辑模块（分工独立）
│ │ ├── user/ # 用户、认证、好友（Backend A）
│ │ │ ├── user.controller.js
│ │ │ ├── user.service.js
│ │ │ └── user.router.js
│ │ ├── content/ # 内容、评论、标签（Backend B）
│ │ │ ├── content.controller.js
│ │ │ ├── content.service.js
│ │ │ └── content.router.js
│ │ └── admin/ # 管理端相关（Backend C）
│ │ ├── admin.controller.js
│ │ └── stats.service.js
│ └── app.js # 应用入口（路由加载等）
├── tests/ # 单元测试和集成测试
├── .env # 环境变量
└── package.json # 项目依赖及配置