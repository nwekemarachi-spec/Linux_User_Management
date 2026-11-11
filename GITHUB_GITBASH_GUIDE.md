# Push this practical to GitHub using Git Bash

These steps assume you have Git installed, a GitHub account, and have created an **empty** repository on GitHub. Do not add a README on GitHub if you are pushing this folder's existing README.

## 1. Extract the ZIP

Extract `linux-user-management-fhs-practical.zip` to a location you can find, for example:

`C:\Users\YourName\Documents\linux-user-management-fhs-practical`

## 2. Open Git Bash in the project folder

In File Explorer, open the extracted folder, right-click inside it, and choose **Git Bash Here**.

Alternatively, open Git Bash and navigate to the folder. Example (adjust the path to your own computer):

```bash
cd ~/Documents/linux-user-management-fhs-practical
```

Check that you are in the correct folder:

```bash
pwd
ls -la
```

You should see `README.md`, `GITHUB_GITBASH_GUIDE.md`, `screenshots/`, and `evidence/`.

## 3. Configure Git identity (if not already configured)

Use the name and email associated with your GitHub commits:

```bash
git config --global user.name "Your GitHub Name"
git config --global user.email "your-email@example.com"
```

## 4. Initialize and commit

Run these commands one at a time:

```bash
git init
git add .
git status
git commit -m "Add Linux user management and FHS practical"
```

Review `git status` before committing. Confirm that no passwords, access tokens, private keys, or other secrets are staged.

## 5. Connect your GitHub repository

On GitHub, create a new repository named:

`linux-user-management-fhs-practical`

Copy its HTTPS URL. It will look like:

`https://github.com/YOUR-USERNAME/linux-user-management-fhs-practical.git`

Then run (replace the example URL with your actual repository URL):

```bash
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/linux-user-management-fhs-practical.git
git remote -v
git push -u origin main
```

GitHub may prompt you to authenticate through a browser or credential manager. Do not put your password or personal access token directly into the repository or a script.

## 6. Verify the upload

Refresh your GitHub repository page. Confirm that the README and folders are visible.

For later updates, use:

```bash
git add .
git status
git commit -m "Add practical evidence"
git push
```

## Troubleshooting

- **`remote origin already exists`:** Run `git remote -v`. If the URL is wrong, update it with `git remote set-url origin https://github.com/YOUR-USERNAME/linux-user-management-fhs-practical.git`.
- **`src refspec main does not match any`:** Make sure you have created a commit before pushing.
- **Authentication failed:** Complete GitHub's browser/credential-manager sign-in. GitHub account passwords are not accepted for Git HTTPS authentication.
- **Nothing to commit:** There may be no new changes since the last commit. Check `git status`.

## Important

Pushing this starter repository does not perform the Linux practical for you. Complete the commands in your Linux VM, save your own screenshots and outputs, update the evidence log, and push those genuine results in a later commit.
