# Troubleshooting

## Error: Unsafe call of a(n) error type typed value (Prisma + TypeScript + ESLint)

When setting up the first entity in the database using the Prisma ORM, you may encounter the following error in ESLint/TypeScript:

```
Unsafe call of a(n) error type typed value.eslint@typescript-eslint/no-unsafe-call
Unsafe member access .deleteMany on an error typed value.eslint@typescript-eslint/no-unsafe-member-access
```

This issue occurs because Prisma generates types and methods dynamically from the `schema.prisma` file. If the TypeScript Server (TS Server) is not restarted after schema changes, it may not correctly recognize the new classes/types, treating everything as `any` and causing type errors in ESLint.

### How to fix

1. **Restart the TS Server in VS Code:**
   - Open the command palette (`Ctrl+Shift+P` or `Cmd+Shift+P`).
   - Search for `TypeScript: Restart TS Server` and run the command.

2. **After restarting, Prisma type errors should disappear.**

### Reference

- [T3 Stack Tutorial - FROM 0 TO PROD FOR $0 (Next.js, tRPC, TypeScript, Tailwind, Prisma & More)](https://youtu.be/YkOSUVzOAA4?si=Bjhbadv2E_uwkk2w&t=1432)