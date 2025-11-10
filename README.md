# SeeDream Image MCP

基于火山引擎 SeeDream 模型的 MCP (Model Context Protocol) 图片生成工具。

## ✨ 特性

- 🎨 使用火山引擎 SeeDream 4.0 模型生成高质量图片
- 🔧 支持自定义尺寸、智能参考图等
- 📝 无需编写复杂提示词，AI自动根据需求生成生图提示词
- 🔌 MCP 协议支持，可在 Cursor、Claude Desktop 等客户端中使用

## 🚀 快速开始

### 1. 获取火山引擎 API Key

前往 [火山引擎->火山方舟控制台](https://console.volcengine.com/ark/region:ark+cn-beijing/apiKey) 开通服务并申请 API Key。

### 2. 使用 npx 运行

```bash
npx seedream-image-mcp --ark-key=YOUR_API_KEY
```

### 3. 在 Cursor、Claude Desktop 中配置

编辑 `Cursor MCP配置` 或 `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "seedream-image": {
      "command": "npx",
      "args": ["seedream-image-mcp", "--ark-key=YOUR_API_KEY"]
    }
  }
}
```

## 📖 使用示例

在 AI Agent 工具中，你可以这样使用：

```
为这个页面添加合适的图片，避免过于单调
```

AI 会自动调用工具完成生成。

## 📌 注意事项

**图片链接时效性**：本项目使用火山引擎原始 API，生成的图片链接通常在 24 小时后失效。如果你需要长期保存图片，请及时下载到本地。

## 🔄 两种使用方式

你可以根据自己的需求选择：

### 方式一：本地运行 🔧
- 需要自己申请火山引擎 API key
- 图片链接 24 小时后失效，需下载到本地使用。

### 方式二：云端版本 ✨
- ✅ 无需申请 API key，开箱即用
- ✅ 图片支持永久存储在 CDN
- ✅ 支持 webp 压缩、背景移除、快速并发生成多张图片等功能
- ✅ 提供一定的免费额度
- ✅ 量大时价格更优惠

👉 了解云端版本：[https://mcp.pixelark.art](https://mcp.pixelark.art)

---

## 🛠️ 开发

### 安装依赖

```bash
bun install
```

### 本地运行

```bash
bun run src/index.ts --ark-key=YOUR_API_KEY
```

## 📄 许可证

MIT

## 🔗 相关链接

- [云端版本](https://mcp.pixelark.art)
- [火山引擎 SeeDream](https://www.volcengine.com/docs/ark/doubao-seedream)
- [MCP 协议](https://modelcontextprotocol.io)
