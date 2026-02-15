# .github - a hidden gem in repository management

All github meta files are stored here and automatically linked from all repositories in [nexus-module](https://github.com/nexus-module/).

You can read more about this feature and its supported functionality [here](https://docs.github.com/en/github/building-a-strong-community/creating-a-default-community-health-file#supported-file-types).

## Steps for cleaning up commit history with `git rebase`

This process uses an interactive rebase to clean up your commit history by combining, editing, or removing commits, followed by a force push to update the remote repository with the cleaned history. Be cautious when using git push --force as it overwrites the commit history on the remote branch.

1. Clone repository
2. Start an Interactive Rebase
    Begin an interactive rebase for the last 10 commits (or adjust the number as needed):

    ```bash
    git rebase -i HEAD~1
    ```

3. Edit commits in the editor
    The editor will open with a list of commits. Use the following commands to clean up the commits:
      * `pick`: Keep the commit as is.
      * `reword`: Change the commit message.
      * `edit`: Amend the commit.
      * `squash`: Combine this commit with the previous one.
      * `fixup`: Like squash, but discard this commit’s message.
      * `drop`: Remove the commit.
    Example to squash and reword:

    ```bash
    pick e1c2f34 Commit message 1
    squash d2c3e45 Commit message 2
    reword f3d4e56 Commit message 3
    ```

4. Save and Close the Editor
    After making your changes, save and close the editor. Git will apply the changes.

5. Resolve Any Conflicts
    If there are conflicts, Git will pause and prompt you to resolve them:

    ```bash
    # Edit the files to resolve conflicts
    git add <resolved_files>
    git rebase --continue
    ```

    Repeat until the rebase completes.

6. Force Push the Cleaned History
    Finally, force push the changes to the remote repository:

    ```bash
    git push origin main --force
    ```

## File structure

The file structure of the repository is as follows:

```console
.
├── .github
│   ├── ISSUE_TEMPLATE
│   │   ├── bug-report.yaml
│   │   └── feature-request.yaml
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── stale.yaml
├── CODEOWNERS
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── GUIDELINES.md
├── LICENSE
└── README.md
```

### File explanations

* **CODEOWNERS**: Defines code owners to ensure the right people are notified for code reviews.
* **CODE_OF_CONDUCT.md**: Contains the code of conduct for the project, specifying the standards of behavior expected from contributors.
* **CONTRIBUTING.md**: Contains guidelines for contributing to the project, including the process for submitting pull requests and creating issues.
* **GUIDELINES.md**: Provides additional guidelines that contributors should follow, such as coding conventions and quality standards.
* **LICENSE**: The project's license file, specifying the terms under which the code can be used and distributed.
* **README.md**: The file you are currently reading, providing an overview of the project and its structure.

## .github directory configuration

The `.github` directory contains GitHub-specific configurations, such as templates for issues and pull requests, as well as GitHub Actions workflows:

* **ISSUE_TEMPLATE**
  * `bug-report.yaml`: Template for reporting bugs.
  * `feature-request.yaml`: Template for requesting new features.
* `PULL_REQUEST_TEMPLATE.md`: Template for pull request descriptions, helping standardize the information provided in each PR.
* `stale.yaml`: Template for issues configuration.

## Contributing

We welcome your contributions! Please read the `CONTRIBUTING.md` file for details on the contribution process and guidelines you should follow.

## License

This project is licensed under the terms specified in the `LICENSE` file.
