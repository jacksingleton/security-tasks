# Task: Choose a tool to help keep secrets out of source control
**Description:**

Mistakes happen. People sometimes check secrets into source control without even
realizing it. The results can be serious, especially when the check-in is into a
publicly-accessible repository. To reduce the risk of this happening, we can
use a proactive tool to validate changes before they make it into source
control.

Some tools for git that work as pre-commit and pre-push hooks include:

* Talisman: https://thoughtworks.github.io/talisman/
* git-secrets: https://github.com/awslabs/git-secrets
* Git Hound: https://github.com/ezekg/git-hound

It is a good idea to encourage the entire team to use this tool for all of their
repositories, not just ones related to your project. There have been many
published cases of developers checking in their dot files to popular project
hosting sites and accidentally leaking their AWS keys or similar secrets.

**Acceptance criteria:**

* When a check-in has been made to the revision control system, then the tool
  should be run against the changes to validate them before they can be pushed a
  remote repository.
* When a check-in containing potentially sensitive information is identified,
  then the tool should stop the change from occurring and alert the user.
