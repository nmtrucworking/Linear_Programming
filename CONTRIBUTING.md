# Contributing Guide

## Branching

- Create a feature branch from `main`.
- Keep each pull request focused on one topic.

## Commit Messages

Use clear and scoped commit messages, for example:

- `docs: update chapter 2 explanation`
- `fix: correct simplex notation in chapter 3`
- `build: refine LaTeX workflow`

## Style Rules

- Keep LaTeX formatting consistent within each file.
- Prefer meaningful section labels and comments when needed.
- Do not commit generated build artifacts (`.aux`, `.log`, `.toc`, `.pdf`, etc.).

## Pull Request Checklist

- Build succeeds locally with `pdflatex`.
- References and table of contents render correctly.
- Changes are limited to intended files.
- PR description explains what changed and why.
