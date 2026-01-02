# Nano-Banana OpenRouter MCP Server

> **Fork of [ConechoAI/Nano-Banana-MCP](https://github.com/ConechoAI/Nano-Banana-MCP)** - Migrated from Google AI SDK to OpenRouter for accessing Gemini 3 Pro Image (Nano Banana Pro).

A Model Context Protocol (MCP) server that provides AI image generation and editing capabilities using **Google's Gemini 3 Pro Image** model via **OpenRouter**. Generate stunning images, edit existing ones, and iterate on your creations with simple text prompts.

## What's Different from the Original?

| Aspect | Original | This Fork |
|--------|----------|-----------|
| **SDK** | `@google/genai` | `@openrouter/sdk` |
| **Model** | Gemini 2.5 Flash Image | Gemini 3 Pro Image (Nano Banana Pro) |
| **API Key** | `GEMINI_API_KEY` (Google AI Studio) | `OPENROUTER_API_KEY` (OpenRouter) |
| **Benefits** | Direct Google access | Unified API, fallback providers, usage analytics |

## Why OpenRouter?

- **Unified API**: Access 300+ models through one endpoint
- **Fallback Providers**: Automatic failover if primary provider is unavailable
- **Usage Analytics**: Track costs and usage across all your AI applications
- **Gemini 3 Pro Image**: Access to the latest Nano Banana Pro model with improved image generation

## Features

- **Generate Images**: Create new images from text descriptions
- **Edit Images**: Modify existing images with text prompts
- **Iterative Editing**: Continue editing the last generated/edited image
- **Multiple Reference Images**: Use reference images for style transfer and guidance
- **Cross-Platform**: Smart file paths for Windows, macOS, and Linux
- **Auto File Management**: Automatic image saving with organized naming

## Setup

1. **Get your OpenRouter API key**:
   - Visit [OpenRouter Settings](https://openrouter.ai/settings/keys)
   - Create a new API key
   - Copy it for configuration

2. **Install and configure** (see examples below)

## Usage with Claude Code

```json
{
  "mcpServers": {
    "nano-banana": {
      "command": "npx",
      "args": ["nano-banana-openrouter-mcp"],
      "env": {
        "OPENROUTER_API_KEY": "your-openrouter-api-key-here"
      }
    }
  }
}
```

## Usage with Cursor

```json
{
  "nano-banana": {
    "command": "npx",
    "args": ["nano-banana-openrouter-mcp"],
    "env": {
      "OPENROUTER_API_KEY": "your-openrouter-api-key-here"
    }
  }
}
```

## Available Tools

| Tool | Description |
|------|-------------|
| `generate_image` | Create a new image from a text prompt |
| `edit_image` | Edit a specific image file with optional reference images |
| `continue_editing` | Continue editing the last generated/edited image |
| `get_last_image_info` | Get information about the last generated image |
| `configure_openrouter_token` | Configure your OpenRouter API key |
| `get_configuration_status` | Check if the API key is configured |

## Configuration Priority

1. **MCP Environment Variables** (Highest) - `"env": { "OPENROUTER_API_KEY": "..." }`
2. **System Environment Variable** - `export OPENROUTER_API_KEY="..."`
3. **Local Config File** (Lowest) - `.nano-banana-config.json`

## Example Workflow

```
> Generate an image of a sunset over mountains

> Continue editing to add some birds in the sky

> Continue editing to make it more dramatic with vibrant colors
```

## Local Development

```bash
git clone https://github.com/Kaden-Schutt/Nano-Banana-OpenRouter-MCP.git
cd Nano-Banana-OpenRouter-MCP
npm install
npm run dev
```

## Requirements

- Node.js 18.0.0+
- OpenRouter API key from [openrouter.ai/settings/keys](https://openrouter.ai/settings/keys)

## Tech Stack

- **TypeScript** - Type-safe development
- **OpenRouter SDK** - Unified AI model access
- **Gemini 3 Pro Image** - Google's latest image generation model
- **MCP SDK** - Model Context Protocol

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Acknowledgments

- **[ConechoAI/Nano-Banana-MCP](https://github.com/ConechoAI/Nano-Banana-MCP)** - Original project
- **[Claude Code](https://claude.ai/code)** - For generating this migration
- **[OpenRouter](https://openrouter.ai)** - For unified AI model access
- **[Google AI](https://ai.google)** - For the Gemini 3 Pro Image model
