# CLAUDE.md - Agent Guidelines

## Commands
- Build/start: `npm start` or `bun run index.ts`
- Run with input: `npm start "your query"` or `bun run index.ts "your query"`
- Dev mode: `npx tsx index.ts "your query"`

## Code Style
- TypeScript with strong typing (use explicit types)
- No semicolons (relies on Prettier's `semi: false`)
- Single quotes for strings (`singleQuote: true`)
- Use async/await for promises
- Use destructuring for function parameters with defaults
- Tools follow a standard pattern with Zod validation
- Error handling: Catch errors close to their source
- File organization: One feature per file, export from index.ts

## Naming Conventions
- PascalCase for types and interfaces
- camelCase for variables, functions, and methods
- Descriptive function names (verb + noun)
- Tool definitions end with `ToolDefinition` (e.g., `dadJokeToolDefinition`)

## Imports
- Import from node_modules first, then relative imports
- Group imports by source (external libraries, then local)
- Use explicit imports, not wildcard `import * as`