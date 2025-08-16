# Contributing Guidelines

Thank you for contributing to this project!  
To maintain a production-grade workflow, please follow the branch strategy and rules below.

---

## 🔹 Branch Strategy

- `main` → Production-ready branch (protected)
- `develop` → Integration branch (protected)
- `feature/*` → New features
- `release/*` → Pre-production release preparation
- `hotfix/*` → Critical fixes applied directly to production

---

## 🔹 Branch Protection Rules

The following rules are applied to `main` and `develop` branches:

1. **No Direct Pushes**  
   - Direct pushes to `main` and `develop` are **disallowed**.  
   - All changes must go through Pull Requests (PRs).  

2. **Pull Request Requirements**  
   - ✅ PRs must be reviewed and approved before merging.  
   - ✅ PRs must pass CI/CD checks (Jenkins, SonarQube, Trivy, etc.).  
   - ✅ Branch must be up-to-date with the base branch before merging.  

3. **Approvals**  
   - At least **1 reviewer approval** is required (adjustable per team size).  

4. **Merging Strategy**  
   - Use **Squash and Merge** for feature branches.  
   - Use **Merge Commit** for release/hotfix branches.  

5. **Release Flow**  
   - Features → `feature/*` → merged into `develop`.  
   - Releases → `develop` → `release/*` → merged into `main`.  
   - Hotfixes → `main` → `hotfix/*` → merged into both `main` and `develop`.  

---

## 🔹 Commit Message Format

Follow conventional commits for clarity:

- `feat:` → new feature  
- `fix:` → bug fix  
- `docs:` → documentation changes  
- `ci:` → CI/CD related changes  
- `chore:` → maintenance  

Example:  
    feat(auth-service): add JWT-based login
    fix(frontend): correct booking form validation

---

## 🔹 Code Review Best Practices

- Ensure code is **tested and linted**.  
- Keep PRs small and focused.  
- Provide clear descriptions in PRs.  
- Link related Jira/GitHub issue IDs in the PR description.  

---

By following these rules, we ensure stability, quality, and collaboration across the team 🚀
