# Spring 6 中文文档

这是一个基于 Spring 6 中文文档项目，面向 Spring 6 学习与实践场景，覆盖 Spring 基础、Spring 集成、反应式 Spring 和 Spring 部署等主题。

项目当前已根据章节目录搭建好文档骨架。每一章和每个小节都已创建对应的 MDX 页面，后续可以按章节逐步补充正文、代码示例、图示和参考链接。

## 项目内容

- 第 1 部分：Spring 基础
- 第 2 部分：Spring 集成
- 第 3 部分：反应式 Spring
- 第 4 部分：部署 Spring
- 附录：初始化 Spring 应用

## 技术栈

- [Mintlify](https://mintlify.com)：文档站点框架
- MDX：文档页面格式
- `docs.json`：站点配置与导航配置

## 本地运行

确保已安装 Mintlify CLI：

```bash
mint version
```

启动本地预览：

```bash
mint dev
```

默认访问地址：

```text
http://localhost:3000
```

## 常用命令

```bash
# 本地预览
mint dev

# 校验文档构建
mint validate

# 检查内部链接
mint broken-links
```

## 目录结构

```text
.
├── docs.json                    # Mintlify 站点配置与导航
├── index.mdx                    # 首页
├── spring-basics/               # 第 1 部分：Spring 基础
├── spring-integration/          # 第 2 部分：Spring 集成
├── reactive-spring/             # 第 3 部分：反应式 Spring
├── deploying-spring/            # 第 4 部分：部署 Spring
├── appendix/                    # 附录
├── logo/                        # 站点 Logo
└── style.css                    # 自定义样式
```

## 写作约定

- 每个页面使用 `.mdx` 格式。
- 每个页面必须包含 `title` 和 `description` frontmatter。
- 新增页面后，需要同步更新 `docs.json` 的 `navigation`。
- 内部链接使用根路径，不带文件扩展名，例如 `/spring-basics/getting-started`。
- 代码块需要声明语言类型，例如：

```java
public class Example {
}
```

## 中英文内容切换

本项目采用“单页内中英文切换”的方式，而不是整个站点的多语言切换。

在需要展示中英文对照的页面中，可以使用 Mintlify 的 `<Tabs>` 组件：

```mdx
<Tabs>
  <Tab title="中文">
    这里编写中文内容。
  </Tab>

  <Tab title="English">
    Write the English content here.
  </Tab>
</Tabs>
```

如果同一页面中有多个包含 `中文` 和 `English` 的 Tab 组，Mintlify 会自动同步相同标题的 Tab 选择。

## 后续计划

- 按章节补充 Spring 6 中文正文。
- 为关键主题补充可运行代码示例。
- 增加常见问题和实践建议。
- 检查并统一术语翻译。

## 许可证

本项目采用 MIT License。详情请查看 `LICENSE` 文件。
