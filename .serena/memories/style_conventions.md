# Code Style and Conventions

## TypeScript Configuration
- Target: ES2022
- Module: ESNext (ES modules)
- Strict mode enabled
- Import paths use `.js` extension for MCP SDK imports

## Code Style
- **Indentation**: 2 spaces
- **Quotes**: Double quotes for strings
- **Semicolons**: Required
- **Class members**: Use `private` keyword for encapsulation
- **Types**: Use Zod for runtime validation, infer types with `z.infer<>`
- **Async/await**: Preferred over raw promises

## Naming Conventions
- **Classes**: PascalCase (e.g., `NanoBananaMCP`)
- **Methods/Functions**: camelCase (e.g., `setupHandlers`, `generateImage`)
- **Constants**: camelCase for schema definitions (e.g., `ConfigSchema`)
- **Variables**: camelCase
- **Files**: kebab-case for config files, camelCase for source files

## ESLint Rules
- Unused variables error (except those prefixed with `_`)
- Based on `eslint:recommended`
- Uses `@typescript-eslint/parser`

## Patterns Used
- **Schema validation**: Zod schemas with `.parse()` or `.safeParse()`
- **Error handling**: `McpError` with `ErrorCode` enum from MCP SDK
- **Async methods**: All image operations are async
- **Class-based architecture**: Single main class encapsulates server logic

## Import Style
```typescript
import { Server } from "@modelcontextprotocol/sdk/server/index.js";
import { z } from "zod";
import fs from "fs/promises";
```
