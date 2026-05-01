# SCU-HUB
四川大学学生常用网站导航聚合页，主要面向CS/EE相关专业学生(其实主要面向作者自己，哈哈)。本项目主要由cursor(based on opus4.7)实现，作者主要贡献在于项目需求和设计文档的编写、代码的调试及检查。
本项目为本学院计算机网络与通信课程的第一次实验作业。虽然代码主要由llms编写，但也不能说作者完全不懂HTML,毕竟从大一开始也做过好几个网页了（老师别挂我ww）。
现在对于本项目进行简单说明。

## 简介

SCU Hub 是一个面向四川大学学生的静态导航页面，整合了教务、图书馆、在线课程、校园生活、工程工具、效率工具等常用网站，支持本地模糊搜索与 Google 搜索跳转。

## 功能

- 按分类浏览常用网站，点击或悬停展开
- 本地模糊搜索，按名称、分类或 URL 过滤
- Google 搜索模式，输入关键词按 Enter 直接跳转
- 响应式布局，适配桌面与移动端
- 纯静态，无需服务器或构建工具

## 文件结构

```
scu-hub/
├── index.html      # 主页面
├── data.js         # 网站数据（分类与链接）
├── logo1.jpeg      # 网站logo图片
├── small logo.png  # 箭头图标
├── 01.png ~ 06.png # 各分类图标
└── README.md
```

## 部署

### 本地预览

直接用浏览器打开 `index.html` 即可。

### GitHub Pages

1. Fork 或 clone 本仓库
2. 进入仓库 **Settings → Pages**
3. Source 选择 `main` 分支，`/ (root)` 目录
4. 保存后访问 `https://<your-username>.github.io/<repo-name>/`

## 添加网站

编辑 `data.js`，在 `sites` 数组末尾追加一条记录：

```js
{ category: 'Productivity', name: '示例网站', url: 'https://example.com/' }
```

可用分类：`Study` · `Research` · `Online Courses` · `Campus Life` · `Engineering` · `Productivity`

如需新增分类，在 `categories` 数组中添加分类名，并提供对应图标图片。

## License

[MIT](./LICENSE)
