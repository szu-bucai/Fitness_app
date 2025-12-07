# web-admin 目录说明

本目录为【Web 管理后台】主代码目录，采用 Vue3 框架（推荐搭配 AntD/Element/ECharts 等），与后端 admin 模块数据联动。

## 主要结构
- src/
  - api/        管理后台 API 接口封装，仅对接 backend C
  - components/ 管理后台通用 UI 组件（表格、图表等）
  - views/      各主页面视图（Dashboard、UserMgmt、ContentMgmt等）
  - App.vue     根组件
  - index.js    入口文件
- package.json  前端依赖声明

## 开发建议
- 页面逻辑建议模块拆分，复用组件尽量沉淀到 components/
- 数据请求统一封装进 api/
- 视图文件结构清晰，便于多人协作
