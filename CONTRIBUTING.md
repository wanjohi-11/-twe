# Contributing to TWE

TWE is maintained as a production product rather than an experimental codebase.

## Branches

Use short-lived branches:

- `feature/<name>` for product functionality
- `fix/<name>` for defects
- `content/<name>` for content-system changes
- `chore/<name>` for maintenance

## Before merge

- no production secrets
- no `.env`
- no customer database dumps
- PHP syntax checks pass
- affected routes are tested
- mobile UI is checked where relevant
- Control Centre authorization is verified
- database/environment changes are documented

## UI direction

TWE should remain editorial, minimal, light by default, mobile-first and restrained in its use of gold.
