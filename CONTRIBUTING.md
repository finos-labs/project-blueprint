# Contributing to {project name}

{project name} is [Apache 2.0 licensed](LICENSE) and accepts contributions via git pull requests. 

## Developer Certificate of Origin (DCO)

All contributions to this project must be accompanied by a **Developer Certificate of Origin**
sign-off. This is a FINOS requirement that certifies you have the right to submit
the contribution under the project's license. 

>[!IMPORTANT]
>**All commits must be signed with a DCO signature to avoid being flagged by the DCO Bot.**
>The DCO check will fail if even a single commit in your branch is missing the Signed-off-by line.

This sign-off means you agree the commit satisfies the [Developer Certificate of Origin (DCO).](https://developercertificate.org/)

> Pull requests that contain unsigned commits will not be merged.

This means that your commit log message must contain a line that looks like the following one, with your actual name and email address:

```
Signed-off-by: John Doe <john.doe@example.com>
```

### Configuring Git to sign off 

```bash
git config --global user.name  "Your Name"
git config --global user.email "your.email@example.com"
# Then use: git commit -s -m "your message"
```
>[!NOTE]
>The email must match with the email linked to your GitHub profile (and must be set to public, see https://github.com/settings/emails to configure your email and for special configurations if keeping your email private).

Adding the -s flag to your git commit `git commit -s` will add that line automatically. You can also add it manually as part of your commit log message or add it afterwards with git commit --amend -s.

To avoid having to remember the -s flag every time, you can configure Git to sign every commit automatically on your workstation (make sure you configured your name and email correctly):

```
git config --global format.signoff true
```

### How to fix a failing DCO check

If the DCO bot flags your PR, you don't need to start over or re-open the PR. It is likely one or more of the commits inside your PR was not properly signed. You can bulk-sign your previous commits using an interactive rebase:

1. Start the rebase (Replace 'X' with the number of commits in your PR)

  ```git rebase -i HEAD~X --signoff```

2. An editor will open listing your commits. Simply save and close it without making changes.

3. Force push the corrected commits to your branch:

  ```git push --force```

### Helpful DCO Resources
- [Git Tools - Signing Your Work](https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work)
- [Signing commits
](https://docs.github.com/en/github/authenticating-to-github/signing-commits)

## Contributing Issues

### Prerequisites

* [ ] Have you [searched for duplicates](https://github.com/finos-labs/{project-slug}/issues?utf8=%E2%9C%93&q=)?  A simple search for exception error messages or a summary of the unexpected behaviour should suffice.
* [ ] Are you running the latest version?
* [ ] Are you sure this is a bug or missing capability?

### Raising an Issue
* Create your issue [here](https://github.com/finos-labs/{project name}/issues/new).
* New issues contain two templates in the description: bug report and enhancement request. Please pick the most appropriate for your issue, **then delete the other**.
  * Please also tag the new issue with either "Bug" or "Enhancement".
* Please use [Markdown formatting](https://help.github.com/categories/writing-on-github/)
liberally to assist in readability.
  * [Code fences](https://help.github.com/articles/creating-and-highlighting-code-blocks/) for exception stack traces and log entries, for example, massively improve readability.

## Contributing Pull Requests (Code & Docs)
To make review of PRs easier, please:

 * Please make sure your PRs will merge cleanly - PRs that don't are unlikely to be accepted.
 * For code contributions, follow the existing code layout.
 * For documentation contributions, follow the general structure, language, and tone of the [existing docs](https://github.com/finos-labs/{project-slug}/wiki).
 * Keep commits small and cohesive - if you have multiple contributions, please submit them as independent commits (and ideally as independent PRs too).
 * Reference issues if your PR has anything to do with an issue (even if it doesn't address it).
 * Minimise non-functional changes (e.g. whitespace).
 * Ensure all new files include a header comment block containing the [Apache License v2.0 and your copyright information](http://www.apache.org/licenses/LICENSE-2.0#apply).
 * If necessary (e.g. due to 3rd party dependency licensing requirements), update the [NOTICE file](https://github.com/finos/{project name}/blob/master/NOTICE) with any new attribution or other notices


### Commit and PR Messages

* **Reference issues, wiki pages, and pull requests liberally!**
* Use the present tense ("Add feature" not "Added feature")
* Use the imperative mood ("Move button left..." not "Moves button left...")
* Limit the first line to 72 characters or less
