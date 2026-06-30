# Engineering Playbook Style Guide

Version: 1.0

---

# Purpose

This guide defines how documentation should be written throughout this repository.

Every document must follow these rules.

---

# Language

- Use US English.
- Keep sentences short.
- Avoid unnecessary jargon.
- Prefer active voice.
- Write for engineers.

---

# Tone

Documentation should be:

- professional
- practical
- concise
- implementation focused

Never write marketing language.

---

# Headings

Always use:

# Title

## Major Section

### Subsection

Do not skip heading levels.

---

# Lists

Use bullets when order doesn't matter.

Use numbered lists for procedures.

---

# Code Blocks

Always specify language.

Good:

```ts
const app = createApp();
```

Bad:

```
const app = createApp();
```

---

# Examples

Every important concept should include at least one example whenever practical.

---

# File Names

Use:

UPPER_SNAKE_CASE.md

Examples:

README_TEMPLATE.md

ARCHITECTURE_TEMPLATE.md

Never use spaces.

---

# Links

Prefer relative links.

---

# Terminology

Use these RFC words correctly.

MUST

SHOULD

MAY

MUST NOT

SHOULD NOT

---

# Markdown

Keep line length readable.

Avoid excessive nesting.

Use tables only when comparison improves readability.

---

# Images

Store images under

docs/assets/

Never embed large screenshots.

---

# Versioning

Every major document begins with:

Version

Status

Last Updated

---

# Review Checklist

Before committing:

✓ Grammar checked

✓ Formatting checked

✓ Links verified

✓ Examples correct

✓ No duplicated information

✓ Matches repository style