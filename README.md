# dot-pro

一个 Codex 技能，用于协调 ChatGPT 网页 Pro、Dot 和本地 Codex 完成获授权的协作任务。它也支持用户明确要求的网页 Deep Research 与图像工作流。

对代码任务，已连接兼容 Git MCP 的 Pro 优先直接读取固定版本、修改文本文件、提交并创建或续更 PR。Dot 负责需要执行环境的工作和项目检查；Codex 负责核对结果以及获授权的本地集成。具体分工以用户选择和实际能力为准。

## 安装

在 Codex 中使用自带的 `$skill-installer`，例如：

> 使用 `$skill-installer` 从 `AshWood97/dot-pro` 的 `skills/dot-pro` 安装技能。

安装后在下一轮对话中使用 `$dot-pro`。安装内容和说明见 [技能正文](skills/dot-pro/SKILL.md) 与 [MCP 接口参考](skills/dot-pro/references/git-mcp.md)。仓库根目录还提供便携插件元数据 [plugin.json](plugin.json)；推荐优先通过 skill-installer 安装技能。

## 准备与使用

1. 按任务需要准备可用的 ChatGPT Pro 会话、Dot 和 Codex 原生浏览器控制能力。多个账号由使用者指定或按任务上下文选择，提交前确认当前账号、会话和模型。
2. 若要求 Pro 直接向 Git 交付，需要用户已批准的兼容 MCP 服务和该会话实际可用的连接。服务地址与认证由使用者提供；本仓库不附带 Git MCP 服务端，也不自动安装或部署服务。
3. 按 [OpenAI 官方自定义 MCP 接入说明](https://developers.openai.com/api/docs/guides/custom-mcp-server)在 ChatGPT 中添加服务、按服务配置设置认证并安装，然后在会话中用 `@` 选择连接。根据当前界面和授权处理写入确认。
4. 给出项目、目标、版本或工作区来源、预期交付和授权范围。技能会固定 manifest 与导出提交，按需要读取源码，通过兼容工具提交任务分支并创建或续更 PR。

示例请求：

> 使用 `$dot-pro`，让已连接 Git MCP 的 Pro 根据指定固定版本实现这个改动并提交 PR；由 Dot 执行项目检查，Codex 核对并接收结果。

如 Pro 会话没有连接或缺少工具，技能会说明实际缺口，并在获授权时将具体源码上下文和补丁交给 Dot 执行；不会把其他模型或普通浏览说成 Pro 的 Git 写入能力。可用账号、工具、模型及配额均以当前实际状态为准。

## 能力与边界

- 已在一个连接兼容服务的 Pro 会话中验证：读取固定版本、提交并再次更新同一分支、创建和续更同一 PR，以及读取交付状态。这说明该次接入与交付流程可用，不代表任意账号、服务或业务测试均已通过。
- [接口参考](skills/dot-pro/references/git-mcp.md)描述 `project_context`、`read_repository`、`commit_files`、`pull_request` 和 `get_delivery` 的实际参数。该接口不提供 shell、测试、构建、Issue 管理、合并或部署。
- 写入结果不明确时，先查询原任务的交付状态，再决定是否重试；同一任务保留固定基线和实际分支。Azure PR 不等于公司仓库已接收、合并或上线。
- Deep Research 使用网站的实际研究模式并返回可取得的报告与来源；图像任务使用网站生成或编辑并取回实际原图。不可用时报告限制。
- 技能本身不会授权发送资料、安装连接、提交代码、合并或部署。遵守任务授权、项目规则和实际平台提示，只交付已完成且可核对的结果。

## 项目来源和许可证

本项目由 `codex-chatgpt-bridge` 更名并重写，旧实现保留在 Git 历史中。项目沿用原 [MIT 许可证](LICENSE)；单独安装的技能目录也包含该许可证。
