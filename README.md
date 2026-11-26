# date-tool-mcp

一个基于 [Model Context Protocol (MCP)](https://modelcontextprotocol.io) 的简单日期工具服务，提供获取当前日期的能力。

## 功能

### Tools

| 工具名 | 描述 | 参数 | 返回 |
|--------|------|------|------|
| `get_today` | 返回当前的年月日 | 无 | `string` — 格式 `YYYY-MM-DD`，例如 `2026-11-26` |

### Resources

无。

### Prompts

无。

## 安装

### 方式一：从源码安装
bash
git clone https://github.com/yourusername/date-tool-mcp.git
cd date-tool-mcp
pip install -e .
服务启动后会通过 **stdio** 与 MCP 客户端通信，无需额外端口。

## 集成配置

### Claude Desktop

在 `claude_desktop_config.json` 中添加：
{
"mcpServers": {
"date-tool": {
"command": "python",
"args": ["/绝对路径/to/main.py"],
"env": {}
}
}
}
