# Nano-Banana MCP Server

## Purpose
An MCP (Model Context Protocol) server that provides AI image generation and editing capabilities using Google's Gemini 3 Pro Image API via OpenRouter. It allows AI assistants to generate images from text prompts, edit existing images, and iterate on creations.

## Tech Stack
- **Language**: TypeScript (ES2022 target, ESNext modules)
- **Runtime**: Node.js 18.0.0+
- **Key Dependencies**:
  - `@modelcontextprotocol/sdk` - MCP protocol implementation
  - `@openrouter/sdk` - OpenRouter API client (Gemini 3 Pro Image)
  - `zod` - Schema validation
  - `dotenv` - Environment variable loading

## Project Structure
```
nano-banana-mcp/
├── src/
│   ├── index.ts          # Main MCP server implementation
│   └── test/
│       └── index.test.ts # Tests
├── dist/                  # Compiled JavaScript output
├── package.json
├── tsconfig.json
├── .eslintrc.json
└── README.md
```

## Main Architecture
- Single main class `NanoBananaMCP` in `src/index.ts`
- Handles all MCP tool implementations:
  - `configure_openrouter_token` - API key configuration
  - `generate_image` - Create new images
  - `edit_image` - Modify existing images
  - `continue_editing` - Iterative editing
  - `get_last_image_info` - Image info retrieval
  - `get_configuration_status` - Check API key status

## Configuration
- API key loaded from:
  1. MCP config environment variables (highest priority)
  2. System environment variables (`OPENROUTER_API_KEY`)
  3. Local `.nano-banana-config.json` file (lowest priority)
