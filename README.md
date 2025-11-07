# Backport Test Repository

This repository is set up to test the automated backport workflow.

## How to Use

1. Create a pull request targeting the main branch
2. Add a label like `backport production` or `backport staging` to specify which branch to backport to
3. Merge the pull request
4. The backport action will automatically:
   - Create a new PR with the changes cherry-picked to the target branch
   - Comment on the original PR if conflicts occur with instructions to resolve manually

## Multiple Backports

You can add multiple backport labels (e.g., `backport production` and `backport staging`) and the action will create separate PRs for each target branch.

## Testing

To test this workflow:
1. Create a branch called `production` or `staging`
2. Create a test PR to `main`
3. Add the backport label
4. Merge and watch the action run
