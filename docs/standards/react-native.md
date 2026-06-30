# React Native Standard

> Version: 1.0.0
>
> Status: Stable
>
> Last Updated: 2026-06-30

---

# Purpose

This standard defines how React Native applications should be designed, organized, and maintained across all projects.

The goal is to build applications that remain scalable, performant, maintainable, and easy to upgrade throughout their lifecycle.

---

# Core Principles

React Native applications should prioritize:

- maintainability
- consistency
- performance
- accessibility
- type safety
- modularity

Features should never compromise long-term maintainability.

---

# Technology Stack

Every new project should use:

- React Native
- TypeScript
- Expo
- Expo Router
- NativeWind
- Zustand
- TanStack Query
- React Hook Form
- Zod
- React Native Reanimated

Avoid introducing additional libraries unless they solve a clear problem.

---

# Project Structure

Organize projects by feature instead of file type whenever practical.

Each feature should own its:

- components
- hooks
- services
- types
- validation
- tests

Avoid creating large shared folders containing unrelated code.

---

# Components

Components should:

- have a single responsibility
- remain reusable
- remain small
- avoid unnecessary business logic

Separate presentation from business logic whenever practical.

---

# State Management

Use local state for local concerns.

Use Zustand for shared application state.

Use TanStack Query for server state.

Avoid storing remote server data inside global stores.

---

# Navigation

Use Expo Router for new Expo projects.

Navigation should:

- remain predictable
- support deep linking
- avoid unnecessary nesting
- keep routes organized

---

# Performance

Prefer:

- FlatList
- SectionList
- FlashList when appropriate

Avoid:

- unnecessary re-renders
- inline object creation
- unnecessary anonymous functions
- heavy work during rendering

Measure performance before optimizing.

---

# Styling

Use NativeWind as the default styling solution.

Design should follow:

- consistent spacing
- reusable components
- design tokens
- dark mode support
- accessibility

Avoid large inline style objects.

---

# Accessibility

Every screen should support:

- screen readers
- scalable text
- accessible touch targets
- meaningful labels

Accessibility is required, not optional.

---

# Error Handling

Every feature should define:

- loading state
- empty state
- error state
- success state

Unexpected failures should fail gracefully.

---

# Offline Considerations

Applications should:

- tolerate unstable networks
- cache data where appropriate
- retry failed requests intelligently

Offline behaviour should be intentional.

---

# Testing

Critical functionality should include:

- unit tests
- integration tests
- end-to-end tests where appropriate

Testing should focus on user behaviour rather than implementation details.

---

# Code Review Checklist

Before merging:

- Feature structure is consistent.
- Components are reusable.
- Navigation follows project conventions.
- Performance concerns are reviewed.
- Accessibility has been considered.
- Error states exist.
- Loading states exist.
- Types are correct.
- Tests are updated.

---

# Definition of Done

A React Native feature is complete when:

- it satisfies functional requirements
- follows project architecture
- passes type checking
- handles loading, empty, success, and error states
- considers accessibility
- performs acceptably
- includes appropriate tests
- updates documentation when necessary