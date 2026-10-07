# GitHub Flow Practice

This repository is a personal practice environment based on the Ooloo GitHub
Flow course. You are both the learner and the repository maintainer.

## Practice loop

1. Update local `main` before starting a task.
2. Create exactly one task branch: `header`, `footer`, `content-container`,
   `top-section`, or `bottom-section`.
3. Make small, purposeful commits and push the branch to `origin`.
4. Open a pull request into `main` and complete the pull request template.
5. Let GitHub Copilot review the pull request. Read every comment and decide
   whether the feedback is correct before changing the code.
6. Push fixes to the same branch. Ask for a re-review when needed.
7. After the AI review is approved and the checks pass, squash and merge the
   pull request yourself as the maintainer.
8. Delete the merged branch, then update local `main` before the next task.

The maintainer action is intentionally kept in the loop to match the original
course. Do not use auto-merge during the first pass through the exercises.

## Useful commands

```bash
git switch main
git pull --ff-only origin main
git switch -c header

git add src/index.html src/styles.css
git commit -m "Implement header"
git push -u origin header
```

Create the pull request with the GitHub web interface or with `gh pr create`.
After a merge, run:

```bash
git switch main
git pull --ff-only origin main
git branch -d header
git push origin --delete header
```
