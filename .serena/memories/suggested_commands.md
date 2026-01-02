# Suggested Commands

## Development Commands (npm scripts)
| Command | Description |
|---------|-------------|
| `npm run build` | Compile TypeScript to JavaScript (output in `dist/`) |
| `npm run start` | Run the compiled server (`node dist/index.js`) |
| `npm run dev` | Run in development mode with hot reload (`tsx src/index.ts`) |
| `npm run test` | Run Jest tests |
| `npm run lint` | Run ESLint on source files |
| `npm run typecheck` | Run TypeScript type checking without emitting |

## Git Commands
| Command | Description |
|---------|-------------|
| `git status` | Check working tree status |
| `git diff` | View unstaged changes |
| `git log --oneline -10` | View recent commits |
| `git branch -a` | List all branches |

## System Commands (macOS/Darwin)
| Command | Description |
|---------|-------------|
| `ls -la` | List files with details |
| `find . -name "*.ts"` | Find TypeScript files |
| `grep -r "pattern" src/` | Search for pattern in source |

## NPM Publishing
| Command | Description |
|---------|-------------|
| `npm run prepublishOnly` | Build and typecheck before publishing |
| `npm publish` | Publish to npm registry |
