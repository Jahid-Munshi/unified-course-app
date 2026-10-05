# Contributor Guidelines for Unified Course App

Welcome to the **Unified Course App** team repository! To maintain clean code quality and smooth collaboration among **Jahid**, **Aishwarya**, and **Saima**, please follow these workflow standards.

---

## 1. Branch Naming Standards
- Feature branches: `feature/<short-description>` (e.g., `feature/bengali-search-parser`, `feature/course-comparison-tray`)
- Bugfix branches: `bugfix/<issue-description>` (e.g., `bugfix/filter-reset-crash`)
- Release branches: `release/vX.Y.Z`

---

## 2. Commit Message Convention
Follow the Conventional Commits style:
- `feat: add dynamic multi-criteria filter drawer`
- `fix: resolve Bengali transliteration tokenization bug`
- `docs: update API schema in README`
- `style: format course card grid using Tailwind CSS`
- `refactor: optimize PostgreSQL query for rating averages`

---

## 3. Pull Request (PR) Workflow
1. Never push directly to `main` or `develop`.
2. Branch out from `develop`.
3. Create a Pull Request targeting `develop`.
4. Ensure all linters and typechecks pass.
5. Obtain at least **1 code review approval** before merging.
