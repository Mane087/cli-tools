| **Command**                      | **What it does**                                                              |
| -------------------------------- | ----------------------------------------------------------------------------- |
| `gh auth login`                  | Authenticate GitHub CLI with your GitHub account.                             |
| `gh auth status`                 | Show the current authentication status.                                       |
| `gh repo clone owner/repository` | Clone a GitHub repository to your local machine.                              |
| `gh repo view`                   | Show information about the current repository.                                |
| `gh repo view --web`             | Open the current repository in your browser.                                  |
| `gh repo create`                 | Create a new GitHub repository interactively.                                 |
| `gh repo fork owner/repository`  | Fork a repository to your GitHub account.                                     |
| `gh pr list`                     | List pull requests in the current repository.                                 |
| `gh pr status`                   | Show pull requests relevant to your current branch or account.                |
| `gh pr view`                     | Show details about a pull request.                                            |
| `gh pr view 42`                  | Show details about pull request `#42`.                                        |
| `gh pr view --web`               | Open the current pull request in your browser.                                |
| `gh pr create`                   | Create a new pull request interactively.                                      |
| `gh pr create --fill`            | Create a pull request using commit information for the title and description. |
| `gh pr checkout 42`              | Check out pull request `#42` locally.                                         |
| `gh pr diff 42`                  | Show the changes introduced by pull request `#42`.                            |
| `gh pr checks 42`                | Show CI checks for pull request `#42`.                                        |
| `gh pr merge 42`                 | Merge pull request `#42`.                                                     |
| `gh issue list`                  | List issues in the current repository.                                        |
| `gh issue view 42`               | Show details about issue `#42`.                                               |
| `gh issue create`                | Create a new issue interactively.                                             |
| `gh issue close 42`              | Close issue `#42`.                                                            |
| `gh issue reopen 42`             | Reopen issue `#42`.                                                           |
| `gh workflow list`               | List GitHub Actions workflows.                                                |
| `gh workflow view`               | Show information about a workflow.                                            |
| `gh workflow run workflow.yml`   | Manually trigger a GitHub Actions workflow.                                   |
| `gh run list`                    | List recent GitHub Actions workflow runs.                                     |
| `gh run view`                    | Show details about a workflow run.                                            |
| `gh run watch`                   | Watch a workflow run until it finishes.                                       |
| `gh run rerun RUN_ID`            | Rerun a GitHub Actions workflow run.                                          |
| `gh run cancel RUN_ID`           | Cancel a running GitHub Actions workflow.                                     |
| `gh release list`                | List releases in the current repository.                                      |
| `gh release view v1.0.0`         | Show information about the `v1.0.0` release.                                  |
| `gh release create v1.0.0`       | Create a new GitHub release with the `v1.0.0` tag.                            |
| `gh release download v1.0.0`     | Download assets from the `v1.0.0` release.                                    |
| `gh api repos/OWNER/REPO`        | Make an authenticated request to the GitHub API.                              |
| `gh api user`                    | Retrieve information about the authenticated GitHub user.                     |
| `gh browse`                      | Open the current repository in your browser.                                  |
