# TypeScript Standard

> Version: 1.0.0
>
> Status: Stable
>
> Last Updated: 2026-06-30

---

# Purpose

This standard defines how TypeScript should be used across all projects.

The objective is to maximize type safety, maintainability, readability, and long-term scalability.

---

# Core Principles

TypeScript is not JavaScript with types.

It is a design tool that catches problems before code reaches production.

The compiler should help engineers discover mistakes as early as possible.

---

# Compiler Configuration

Every production project must enable strict type checking.

Minimum requirements:

- strict
- strictNullChecks
- noImplicitAny
- noImplicitOverride
- noUncheckedIndexedAccess
- exactOptionalPropertyTypes

Never disable strict mode to bypass compiler errors.

Fix the underlying issue instead.

---

# Type Safety

Prefer:

- explicit types when they improve readability
- inferred types where obvious
- unknown instead of any
- readonly wherever possible

Avoid:

- any
- unnecessary type assertions
- unsafe casting

---

# Naming

Interfaces

- PascalCase

Types

- PascalCase

Enums

- PascalCase

Variables

- camelCase

Constants

- UPPER_SNAKE_CASE only for true constants.

---

# Functions

Functions should:

- have a single responsibility
- be small
- have explicit return types for exported APIs
- avoid side effects whenever practical

---

# Objects

Prefer interfaces for public object contracts.

Use type aliases for:

- unions
- intersections
- utility types
- mapped types

---

# Null Handling

Never ignore null or undefined.

Handle both intentionally.

Do not silence compiler warnings.

---

# Error Handling

Throw meaningful errors.

Avoid returning multiple unrelated types.

Prefer Result-style patterns where appropriate.

---

# Imports

Prefer named imports.

Remove unused imports.

Separate type imports when appropriate.

---

# Anti-patterns

Never:

- disable strict mode
- use any without documented justification
- suppress compiler errors without explanation
- duplicate types
- create unnecessary abstractions

---

# Code Review Checklist

Before merging:

- Strict mode passes.
- No unnecessary any.
- No duplicated types.
- Naming follows conventions.
- Public APIs are typed.
- Null handling is explicit.
- Unused code is removed.
- Readability is maintained.

---

# Definition of Done

TypeScript code is considered complete when:

- it compiles without errors
- strict mode passes
- types accurately describe behavior
- exported APIs are documented
- code remains understandable
- no unnecessary unsafe operations exist