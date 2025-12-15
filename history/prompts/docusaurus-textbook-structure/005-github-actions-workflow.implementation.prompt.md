---
id: 005
title: GitHub Actions Workflow
stage: general
date: 2025-12-15
surface: agent
model: claude-opus-4-5-20251101
feature: docusaurus-textbook-structure
branch: 001-docusaurus-textbook-structure
user: Claude Code User
command: /sp.implement
labels: [deployment, github-actions, workflow, docusaurus]
links:
  spec: specs/001-docusaurus-textbook-structure/spec.md
  ticket: null
  adr: null
  pr: null
files:
 - .github/workflows/deploy.yml
tests:
 - none
---

## Prompt

# Directive: Deployment Infrastructure
Please create the GitHub Actions workflow file.

## File Location Requirement (Critical)
- **Path:** `.github/workflows/deploy.yml`
- **Location:** This file must be in the **PROJECT ROOT** directory.
- **Do NOT** place it inside the `website/` folder.
- **Folder Structure Check:**
  - ✅ Correct: `my-project/.github/workflows/deploy.yml`
  - ❌ Wrong: `my-project/website/.github/workflows/deploy.yml`

## File Content
Paste the following code into `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches:
      - main
    paths-ignore:
      - '.gitignore'
      - 'README.md'

permissions:
  contents: write

jobs:
  deploy:
    name: Deploy to GitHub Pages
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: actions/setup-node@v4
        with:
          node-version: 18
          cache: npm
          cache-dependency-path: website/package-lock.json

      - name: Install dependencies
        run: npm install
        working-directory: website

      - name: Build website
        run: npm run build
        working-directory: website

      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./website/build
          user_name: github-actions[bot]
          user_email: github-actions[bot]@users.noreply.github.com
```

## Response snapshot

Successfully created the GitHub Actions workflow file at `.github/workflows/deploy.yml` with the exact content specified. The workflow is configured to deploy the Docusaurus website to GitHub Pages when changes are pushed to the main branch. It includes steps for checking out the code, setting up Node.js, installing dependencies, building the website, and deploying to GitHub Pages using the peaceiris/actions-gh-pages action.

## Outcome

- ✅ Impact: Created deployment infrastructure for automated GitHub Pages deployment
- 🧪 Tests: No tests required for workflow file
- 📁 Files: Created .github/workflows/deploy.yml in project root
- 🔁 Next prompts: Ready to commit and push for deployment
- 🧠 Reflection: Workflow properly configured with correct paths and permissions

## Evaluation notes (flywheel)

- Failure modes observed: None
- Graders run and results (PASS/FAIL): N/A
- Prompt variant (if applicable): N/A
- Next experiment (smallest change to try): Test the deployment workflow