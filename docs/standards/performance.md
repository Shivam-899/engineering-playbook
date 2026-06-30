# Performance Standard

> Version: 1.0.0
>
> Status: Stable
>
> Last Updated: 2026-06-30

---

# Purpose

This standard defines how application performance should be designed, measured, optimized, and monitored.

Performance is a product quality attribute, not a post-release activity.

---

# Core Principles

Every project should prioritize:

- responsiveness
- efficient resource usage
- predictable performance
- measurable improvements
- continuous monitoring

Never optimize based on assumptions.

Measure first.

---

# Performance Mindset

Performance work should focus on user experience.

Optimize the experience users actually perceive rather than synthetic numbers alone.

Every optimization should have measurable impact.

---

# Performance Budgets

Projects should define measurable performance budgets.

Examples include:

- application startup time
- bundle size
- memory usage
- network requests
- rendering time

Budgets should be reviewed throughout development.

---

# Measurement

Measure performance using appropriate tooling.

Collect both:

- development measurements
- production telemetry

Performance improvements should always be verified with data.

---

# Rendering

Rendering should remain predictable.

Avoid:

- unnecessary re-renders
- expensive computations during rendering
- deeply nested component trees
- unnecessary state updates

Prefer memoization only when profiling demonstrates benefit.

---

# Lists

Large collections should use virtualization.

Examples include:

- FlatList
- SectionList
- FlashList

Avoid rendering large datasets simultaneously.

---

# Images

Optimize all images.

Prefer:

- appropriate dimensions
- modern formats where supported
- lazy loading when appropriate
- compression without visible quality loss

Remove unused assets.

---

# Network

Reduce unnecessary network activity.

Prefer:

- request caching
- batching where appropriate
- pagination
- background refresh
- request deduplication

Avoid duplicate API requests.

---

# Memory

Applications should:

- release unused resources
- avoid memory leaks
- minimize retained objects
- monitor long-running sessions

Memory growth should be investigated.

---

# Lazy Loading

Load functionality only when required.

Consider lazy loading for:

- screens
- feature modules
- heavy assets
- optional functionality

---

# Dependencies

Every dependency increases startup cost.

Projects should:

- minimize dependencies
- remove unused packages
- monitor bundle growth
- review large libraries before adoption

---

# Monitoring

Production applications should collect:

- crashes
- startup performance
- slow operations
- rendering performance
- network latency

Monitoring should support continuous improvement.

---

# Profiling

Profile before optimizing.

Use platform profiling tools to identify actual bottlenecks.

Avoid speculative optimizations.

---

# Accessibility

Performance improvements must never reduce accessibility.

Fast software should also remain usable.

---

# Code Review Checklist

Before merging:

- Performance impact considered.
- No unnecessary re-renders.
- Images optimized.
- Network requests reviewed.
- Large lists virtualized.
- Bundle impact acceptable.
- Performance measurements recorded where appropriate.

---

# Definition of Done

A feature is performance-ready when:

- performance has been measured
- no obvious bottlenecks remain
- unnecessary rendering is removed
- network usage is efficient
- assets are optimized
- monitoring supports future improvements
- user experience remains responsive