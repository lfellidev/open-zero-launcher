# Commit Standards 📜

According to the **[Conventional Commits](https://www.conventionalcommits.org)** documentation, semantic commits are a simple convention to use in commit messages. This convention defines a set of rules to create an explicit commit history, which facilitates the creation of automated tools.

These commits will help you and your team easily understand what changes were made in the committed code snippet.

This identification occurs through a word and emoji that identifies if that commit is a code change, package update, documentation, visual change, test...

## Type and Description 🦄

The semantic commit has the structural elements below (types), which inform the intention of your commit to the user of your code.

- `feat` - Commits of type feat indicate that your code snippet is including a **new feature** (relates to MINOR in semantic versioning).

- `fix` - Commits of type fix indicate that your committed code snippet is **solving a problem** (bug fix), (relates to PATCH in semantic versioning).

- `docs` - Commits of type docs indicate that there were **changes in documentation**, for example in the Readme of your repository. (Does not include code changes).

- `test` - Commits of type test are used when **changes in tests** are made, whether creating, altering, or deleting unit tests. (Does not include code changes)

- `build` - Commits of type build are used when modifications are made to **build files and dependencies**.

- `perf` - Commits of type perf serve to identify any code changes related to **performance**.

- `style` - Commits of type style indicate that there were changes related to **code formatting**, semicolons, trailing spaces, lint... (Does not include code changes).

- `refactor` - Commits of type refactor refer to changes due to **refactoring that does not alter its functionality**, for example, a change in the format how a certain part of the screen is processed, but maintained the same functionality, or performance improvements due to a code review.

- `chore` - Commits of type chore indicate **updates of tasks** of build, administrator configurations, packages... for example adding a package to gitignore. (Does not include code changes)

- `ci` - Commits of type ci indicate changes related to **continuous integration**.

- `raw` - Commits of type raw indicate changes related to configuration files, data, features, parameters.

- `cleanup` - Commits of type cleanup are used to remove commented code, unnecessary snippets, or any other form of source code cleaning, aiming to improve its readability and maintainability.

- `remove` - Commits of type remove indicate the deletion of obsolete or unused files, directories, or functionalities, reducing the size and complexity of the project and keeping it more organized.

## 🛠️ How to install the `commit-msg.sh` file to validate commit messages with conventional commits

### Step 1: Make sure Git is installed 🌟

First of all, check if Git is installed on your machine. Open the terminal and run:

```bash
git --version
```

If you receive a Git version as a response, everything is fine! Otherwise, download and install Git here: [Git Downloads](https://git-scm.com/downloads).

### Step 2: Locate the `commit-msg.sh` file 📂

The `commit-msg.sh` file should be available in your project's repository or in a specific directory. Make sure it is accessible. If not, download or clone the repository where it is located.

For example:

```bash
git clone https://github.com/your-repository/project.git
cd project
```

### Step 3: Create the `.git/hooks` directory (if it doesn't exist) 📁

Git hooks are in the `.git/hooks` directory. Check if it exists in your project:

```bash
ls -la .git/hooks
```

If the directory doesn't exist, create it:

```bash
mkdir -p .git/hooks
```

### Step 4: Copy the `commit-msg.sh` file to the `.git/hooks` directory 📋

Copy the `commit-msg.sh` file to the `.git/hooks` directory and rename it to `commit-msg` (without extension):

```bash
cp path/to/commit-msg.sh .git/hooks/commit-msg
```

> **Note:** Replace `path/to/commit-msg.sh` with the real path to the file.

### Step 5: Give execution permission to the script ✅

For Git to execute the script, you need to give execution permission:

```bash
chmod +x .git/hooks/commit-msg
```

### Step 6: Test the commit hook 💻

Now, try to make a commit in your project. For example:

```bash
git add .
git commit -m "feat: add xyz functionality"
```

If the commit message follows the **Conventional Commits** standard, the commit will be accepted. Otherwise, the hook will block the commit and display an error message.

### Step 7: Customize the script (optional) 🎨

If necessary, open the `.git/hooks/commit-msg` file in a text editor and customize the validation rules to meet your project's needs.

## Recommendations 🎉

- Add a type consistent with the content title.
- We recommend that the first line should have a maximum of 4 words.
- To describe in detail, use the commit description.
- Use an emoji at the beginning of the commit message representing the commit.
- Links need to be added in their most authentic form, that is: without link shorteners and affiliate links.

## Commit Complements 💻

- **Footer:** information about the reviewer and card number in Trello or Jira. Example: Reviewed-by: Elisandro Mello Refs #133
- **Body:** more precise descriptions of what is contained in the commit, presenting impacts and the reasons why the changes were employed in the code, as well as essential instructions for future interventions. Example: see the issue for details on typos fixed.
- **Descriptions:** a succinct description of the change. Example: correct minor typos in code

## Emoji Standards 💈

<table>
  <thead>
    <tr>
      <th>Commit Type</th>
      <th>Emoji</th>
      <th>Keyword</th>
    </tr>
  </thead>
 <tbody>
    <tr>
      <td>Accessibility</td>
      <td>♿ <code>:wheelchair:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Adding a test</td>
      <td>✅ <code>:white_check_mark:</code></td>
      <td><code>test</code></td>
    </tr>
    <tr>
      <td>Updating a submodule version</td>
      <td>⬆️ <code>:arrow_up:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Reverting a submodule version</td>
      <td>⬇️ <code>:arrow_down:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Adding a dependency</td>
      <td>➕ <code>:heavy_plus_sign:</code></td>
      <td><code>build</code></td>
    </tr>
    <tr>
      <td>Code review changes</td>
      <td>👌 <code>:ok_hand:</code></td>
      <td><code>style</code></td>
    </tr>
    <tr>
      <td>Animations and transitions</td>
      <td>💫 <code>:dizzy:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Bugfix</td>
      <td>🐛 <code>:bug:</code></td>
      <td><code>fix</code></td>
    </tr>
    <tr>
      <td>Comments</td>
      <td>💡 <code>:bulb:</code></td>
      <td><code>docs</code></td>
    </tr>
    <tr>
      <td>Initial commit</td>
      <td>🎉 <code>:tada:</code></td>
      <td><code>init</code></td>
    </tr>
    <tr>
      <td>Configuration</td>
      <td>🔧 <code>:wrench:</code></td>
      <td><code>chore</code></td>
    </tr>
    <tr>
      <td>Deploy</td>
      <td>🚀 <code>:rocket:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Documentation</td>
      <td>📚 <code>:books:</code></td>
      <td><code>docs</code></td>
    </tr>
    <tr>
      <td>In progress</td>
      <td>🚧 <code>:construction:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Interface styling</td>
      <td>💄 <code>:lipstick:</code></td>
      <td><code>feat</code></td>
    </tr>
    <tr>
      <td>Infrastructure</td>
      <td>🧱 <code>:bricks:</code></td>
      <td><code>ci</code></td>
    </tr>
    <tr>
      <td>Idea list (tasks)</td>
      <td>🔜 <code> :soon: </code></td>
      <td></td>
    </tr>
    <tr>
      <td>Move/Rename</td>
      <td>🚚 <code>:truck:</code></td>
      <td><code>chore</code></td>
    </tr>
    <tr>
      <td>New feature</td>
      <td>✨ <code>:sparkles:</code></td>
      <td><code>feat</code></td>
    </tr>
    <tr>
      <td>Package.json in JS</td>
      <td>📦 <code>:package:</code></td>
      <td><code>build</code></td>
    </tr>
    <tr>
      <td>Performance</td>
      <td>⚡ <code>:zap:</code></td>
      <td><code>perf</code></td>
    </tr>
    <tr>
        <td>Refactoring</td>
        <td>♻️ <code>:recycle:</code></td>
        <td><code>refactor</code></td>
    </tr>
    <tr>
      <td>Code Cleanup</td>
      <td>🧹 <code>:broom:</code></td>
      <td><code>cleanup</code></td>
    </tr>
    <tr>
      <td>Removing a file</td>
      <td>🗑️ <code>:wastebasket:</code></td>
      <td><code>remove</code></td>
    </tr>
    <tr>
      <td>Removing a dependency</td>
      <td>➖ <code>:heavy_minus_sign:</code></td>
      <td><code>build</code></td>
    </tr>
    <tr>
      <td>Responsiveness</td>
      <td>📱 <code>:iphone:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Reverting changes</td>
      <td>💥 <code>:boom:</code></td>
      <td><code>fix</code></td>
    </tr>
    <tr>
      <td>Security</td>
      <td>🔒️ <code>:lock:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>SEO</td>
      <td>🔍️ <code>:mag:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Version tag</td>
      <td>🔖 <code>:bookmark:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Approval test</td>
      <td>✔️ <code>:heavy_check_mark:</code></td>
      <td><code>test</code></td>
    </tr>
    <tr>
      <td>Tests</td>
      <td>🧪 <code>:test_tube:</code></td>
      <td><code>test</code></td>
    </tr>
    <tr>
      <td>Text</td>
      <td>📝 <code>:pencil:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Typing</td>
      <td>🏷️ <code>:label:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Error handling</td>
      <td>🥅 <code>:goal_net:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Data</td>
      <td>🗃️ <code>:card_file_box:</code></td>
      <td><code>raw</code></td>
    </tr>
  </tbody>
</table>

## 💻 Examples

<table>
  <thead>
    <tr>
      <th>Git Command</th>
      <th>Result on GitHub</th>
    </tr>
  </thead>
 <tbody>
    <tr>
      <td>
        <code>git commit -m ":tada: Initial commit"</code>
      </td>
      <td>🎉 Initial commit</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":books: docs: README update"</code>
      </td>
      <td>📚 docs: README update</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":bug: fix: Infinite loop on line 50"</code>
      </td>
      <td>🐛 fix: Infinite loop on line 50</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":sparkles: feat: Login page"</code>
      </td>
      <td>✨ feat: Login page</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":bricks: ci: Dockerfile modification"</code>
      </td>
      <td>🧱 ci: Dockerfile modification</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":recycle: refactor: Switching to arrow functions"</code>
      </td>
      <td>♻️ refactor: Switching to arrow functions</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":zap: perf: Response time improvement"</code>
      </td>
      <td>⚡ perf: Response time improvement</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":boom: fix: Reverting inefficient changes"</code>
      </td>
      <td>💥 fix: Reverting inefficient changes</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":lipstick: feat: CSS styling for form"</code>
      </td>
      <td>💄 feat: CSS styling for form</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":test_tube: test: Creating new test"</code>
      </td>
      <td>🧪 test: Creating new test</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":bulb: docs: Comments about LoremIpsum() function"</code>
      </td>
      <td>💡 docs: Comments about LoremIpsum() function</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":card_file_box: raw: RAW Data for year aaaa"</code>
      </td>
      <td>🗃️ raw: RAW Data for year aaaa</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":broom: cleanup: Removing commented code blocks and unused variables in form validation function"</code>
      </td>
      <td>🧹 cleanup: Removing commented code blocks and unused variables in form validation function</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":wastebasket: remove: Removing unused files from project to maintain organization and continuous update"</code>
      </td>
      <td>🗑️ remove: Removing unused files from project to maintain organization and continuous update</td>
    </tr>
  </tbody>
</table>

## 📋 Git Commands

- `git clone repository-url-on-github` - Clones an existing remote repository on GitHub to your local environment.

- `git init` - Initializes a new Git repository in the current directory.

- `git add .` - Adds all files and changes in the current directory to the staging area (preparing them for commit).

- `git commit -m "commit message"` - Records the changes added to the staging area with a descriptive message about what was modified.

- `git branch -M main` - Renames the current branch (master) to main. The -M is used to force the renaming, moving the branch if necessary.

- `git remote add origin https://github.com/user/repository-name.git` - Adds a remote repository called origin to the local repository. Use `https://github.com/user` to configure the remote repository with HTTPS or `git@github.com:user` to configure with SSH.

- `git push -u origin main` - Sends the commits from the local main branch to the remote origin repository and sets main as the default branch for future push and pull. The -u (or --set-upstream) configures the upstream branch to facilitate future git push and git pull commands and eliminates the need to specify the branch.

- `git remote add origin git@github.com:user/project.git` `git branch -M main` `git push -u origin main` - When you already have a local repository and want to connect it to a remote repository on GitHub, add the remote repository, rename the main branch to main, and send the initial commits.

- `git fetch` - Fetches all updates from the remote repository without integrating them into the current branch. This updates the remote references.

- `git pull origin main` - Updates the local main branch with changes from the remote origin repository. Combines git fetch and git merge.

- `git push --force-with-lease` - A safer way to force push local changes to the remote repository. Checks if no changes have been made by other collaborators since your last local update, avoiding accidentally overwriting others' work.

- `git revert commit_id_to_be_reverted` - Creates a new commit that undoes the changes made by the specified commit, preserving the history. Useful for undoing changes safely without rewriting history.

- `git reset --hard commit_id_before_the_one_to_be_deleted` - Resets the repository to the state of the specified commit, deleting all changes made after that commit. Ideal for local use. To sync remotely, use `git push --force-with-lease` afterwards.

- `git commit --amend -m "rewritten_message"` - Changes the message of the last commit. After using this command, sync remotely with `git push --force-with-lease`.

- `git cherry-pick COMMIT_HASH` - Used to get a specific commit. Usage example: Imagine you have two branches (main) and (develop) and in the second you have 3 commits but want to get only the first commit from it, with cherry-pick you can.

- `git switch <branch>` - Switches to a different branch in the local repository. Use `git switch -c <branch>` to create and switch to a new branch.

## 📚 Glossary

- `fork` - Copy of a repository to your own account on GitHub. This creates a new repository in your account that is independent of the original, allowing you to make changes without affecting the original repository.

- `issues` - Tool used to manage tasks, requests for new features, and bug fixes in open source projects. Issues should be described and listed, allowing collaborators to discuss and track their progress.

- `pull request` - Mechanism used to submit proposed changes to the original repository. A pull request is a request for the project maintainers to review and potentially incorporate the changes. The pull request will go through an evaluation process and can be accepted or rejected.

- `gist` - Tool that allows sharing code snippets without the need to create a full repository. Gists can be shared publicly or privately.


