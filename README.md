# TpGit_Devops

**Objectives:**
- Familiarize yourself with Git, a commonly employed decentralized version control system..
- Learn how to manage projects, collaborate with other developers, and utilize advanced Git features.

## Creating a New Project

1. Create a new project.
   - Under the name ame "TpGit_Devops".
   - Note the project's URL, which is needed for the following steps.

2. Clone the project using the SSH URL noted in step 1.
   ```
   git clone YOUR_URL
   ```

## Git Basics

1. Create an `index.html` file in your project.
   ```
   touch index.html
   echo "Your file's content" > index.html
   ```

2. Add the file to the index and commit your first change.
   ```
   git add index.html
   git commit -m "First commit: adding index.html"
   ```

## Commit History

- View the commit history with the following command:
   ```
   git log
   ```

## Branch Management

1. Create a new branch to work on a specific feature of your project.
   ```
   git branch ma-fonctionnalite
   git checkout ma-fonctionnalite
   ```

2. Make changes, stage them, commit, and push the changes to the remote repository.
   ```
   git add .
   git commit -m "Modifying ma-fonctionnalite"
   git push origin ma-fonctionnalite
   ```

3. Simulate a conflict by editing the same line in two different branches. Then, merge the branches and resolve the conflict.
   ```
   git checkout ma-fonctionnalite
   git commit -am "Change in ma-fonctionnalite"
   git checkout main
   git commit -am "Change in main"
   git merge ma-fonctionnalite
   git add .
   git commit -m "Conflict resolution"
   ```

4. After resolving the conflict, you'll earn the "Pull Shark" badge.

## Using GitFlow

1. Initialize GitFlow:
   ```
   git flow init
   ```

2. Create a new feature:
   ```
   git flow feature start ma-fonctionnalite
   ```

3. Create a new release:
   ```
   git flow release start my-version
   ```

4. When you're done, merge the feature branch into the development branch using GitFlow:
   ```
   git flow feature finish ma-fonctionnalite
   ```

5. Create a hotfix:
   ```
   git flow hotfix start my-fix
   ```

