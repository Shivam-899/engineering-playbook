# Expo Standard

> Version: 1.0.0
>
> Status: Stable
>
> Last Updated: 2026-06-30

---

# Purpose

This standard defines how Expo projects should be created, configured, developed, tested, built, and released.

Its objective is to maintain consistency across every Expo application.

---

# Core Principles

Every Expo project should prioritize:

- simplicity
- maintainability
- upgradeability
- performance
- security
- developer experience

---

# Project Creation

New projects should:

- use the latest stable Expo SDK
- use TypeScript
- use Expo Router
- enable strict TypeScript
- use EAS Build

Avoid creating custom native code unless absolutely necessary.

---

# Routing

Expo Router is the default routing solution.

Routes should:

- remain predictable
- support deep linking
- avoid unnecessary nesting
- group related screens together

---

# Configuration

Project configuration should remain minimal.

Keep:

- app configuration
- build configuration
- environment configuration

well organized and separated.

---

# Environment Variables

Never commit secrets.

Use:

- development
- preview
- production

environments.

Only public client values should use the EXPO_PUBLIC_ prefix.

Sensitive credentials must never be bundled into the client application.

---

# Build System

Production builds should use EAS Build.

Build profiles should be clearly separated for:

- development
- preview
- production

Each profile should use the appropriate environment configuration.

---

# Updates

Prefer OTA updates only for changes that do not require native code updates.

Test updates before promoting them to production.

---

# Assets

Optimize:

- images
- fonts
- icons
- splash assets

Remove unused assets before release.

---

# Performance

Applications should:

- lazy load where appropriate
- minimize bundle size
- optimize images
- avoid unnecessary re-renders

Measure before optimizing.

---

# Security

Never expose:

- API secrets
- service credentials
- private keys
- tokens

Environment variables are configuration, not security.

Anything shipped inside the client application should be considered public.

---

# Project Structure

Projects should organize code by feature.

Avoid large global folders containing unrelated files.

---

# Dependencies

Keep dependencies:

- minimal
- maintained
- updated

Remove unused packages regularly.

---

# Release Process

Every release should verify:

- build succeeds
- tests pass
- environment variables are correct
- version numbers are updated
- changelog is updated

---

# Code Review Checklist

Before merging:

- Expo SDK is supported.
- Environment configuration is correct.
- Build profiles are reviewed.
- Assets are optimized.
- Navigation follows conventions.
- No secrets exist inside the project.
- Documentation is updated.

---

# Definition of Done

An Expo project is considered production-ready when:

- builds successfully with EAS
- passes type checking
- follows project architecture
- uses correct environments
- protects secrets
- performs acceptably
- is documented
- is ready for deployment