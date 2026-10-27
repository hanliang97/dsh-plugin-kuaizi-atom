# dsh-plugin-kuaizi-atom

[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) 插件：一键接入**筷子原子能力 MCP**（`kuaizi-atom`）——文生图 / 文生视频 / 视频处理 / 矩阵发布 / 数据洞察等全量原子能力工具。

## 安装

DSH Web UI → 插件 → 添加插件 → 安装源选 Git 仓库，输入：

```
https://github.com/hanliang97/dsh-plugin-kuaizi-atom
```

## 配置 Key

插件通过环境变量 `KUAIZI_API_KEY` 读取你的密钥（`pk_` 开头）：

```sh
KUAIZI_API_KEY=pk_xxxxxxxx npx @deepseek-ai/dsh web
```

Key 获取：[筷子原子能力平台 → MCP 接入目录](https://dev-fde.kuaizi.co/fde-atom-demo-web/#/mcp-catalog)（登录后在 MCP 连接配置里复制你的 pk_ Key）。

## 说明

- 默认连**生产**网关 `https://fde-api-ex.kuaizi.co/fde-kmcp/mcp`；开发环境把 `kuaizi-atom.cordis.yml` 里的 url 换成 `https://dev-fde-api-ex.kuaizi.co/fde-kmcp/mcp`
- 上传文件到存储后，**2 小时内必须调用 `store_register` 登记入台账**，否则文件清理失效
- 工具以 `mcp__kuaizi_atom__*` 形式出现在会话中
