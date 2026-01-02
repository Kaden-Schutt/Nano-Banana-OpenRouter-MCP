# Task Completion Checklist

When completing a task on this project, ensure the following steps are performed:

## Before Committing
1. **Type Check**: Run `npm run typecheck` to ensure no type errors
2. **Lint**: Run `npm run lint` to check for linting issues
3. **Build**: Run `npm run build` to verify compilation succeeds
4. **Test**: Run `npm run test` if tests exist for modified code

## Code Quality Checks
- [ ] No unused imports or variables
- [ ] Proper error handling with `McpError`
- [ ] Async operations properly awaited
- [ ] Zod schemas used for input validation
- [ ] No hardcoded sensitive values (use environment variables)

## Documentation
- [ ] Update README.md if adding new features or tools
- [ ] Update `.env.example` if adding new environment variables
- [ ] Add JSDoc comments for public methods if appropriate

## Testing
- [ ] Test new functionality manually with `npm run dev`
- [ ] Add unit tests for new functions in `src/test/`

## Quick Verification Command
```bash
npm run typecheck && npm run lint && npm run build
```
