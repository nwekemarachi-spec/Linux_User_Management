# Linux User Management & Filesystem Practical

**Assessment:** Linux User Management & Filesystem Practical  
**Focus:** Linux command line, user context, Filesystem Hierarchy Standard (FHS), files, search, and permissions  
**Estimated duration:** 90–120 minutes

## 1. Purpose

This repository is the submission workspace for the Linux practical assessment. It provides a place to document the commands used, record meaningful terminal output, save screenshots, and reflect on the results.

> **Important:** Complete the practical on a Linux virtual machine or dedicated lab computer. Do not run it on a production server. Do not include passwords in screenshots, command logs, or GitHub commits.

## 2. Assessment tasks

Complete the tasks in order, following your instructor's approved username format.

1. **Create a user and switch identity:** Create a local account with `sudo adduser <student_username>`, then start a login shell with `su - <student_username>`. Verify with `whoami`, `id`, `pwd`, and `echo $HOME`.
2. **Explore the FHS:** Visit `/`, `/home`, `/etc`, `/var`, `/tmp`, `/usr`, and `/bin`. Record each path and its typical purpose. Use `pwd` and `ls`; do not modify system contents.
3. **Inspect files and hidden entries:** Run `ls`, `ls -l`, and `ls -a` in your home directory. Create `~/.lab-notes` and verify it appears with `ls -a`.
4. **Build a workspace:** Create `~/linux-practical/` with `config/`, `documents/`, `backups/`, and `evidence/`. Use `nano` to create `documents/overview.txt` (at least four lines) and `documents/checklist.txt` (at least three task items).
5. **Create and edit configuration:** Use `nano` to create `config/app.conf` with the required settings below. Reopen it, change `LOG_LEVEL` to `debug`, add `CONTACT=student`, and verify with `cat` or `less`.
6. **Copy, move, and remove:** Copy `overview.txt` and `app.conf` into `backups/`; rename `checklist.txt` to `tasks.txt`; create and then remove only `remove-me.txt`.
7. **Search:** Use `find` to locate `app.conf`. Use `grep -n` to search `overview.txt` for a word you actually included and to search `app.conf` for `LOG_LEVEL`.
8. **Permissions:** Set `app.conf` to `644` and `tasks.txt` to `600`. Verify with `ls -l`, then explain the values and the output of `id`.
9. **Final verification:** Run `find ~/linux-practical -maxdepth 2 -print` and `ls -la ~/linux-practical`. Save appropriate evidence.

### Required initial `app.conf` content

Replace `<student_username>` with the account you created:

```ini
APP_NAME=LinuxPractical
OWNER=<student_username>
ENVIRONMENT=training
LOG_LEVEL=info
BACKUP_ENABLED=true
```

After reopening the file in `nano`, the final version must have `LOG_LEVEL=debug` and an additional `CONTACT=student` line.

## 3. Safety rules

- Use a Linux VM or dedicated lab workstation.
- Use an account with `sudo` privileges only for the initial account-creation step.
- Complete the practical tasks from the newly created user's login shell.
- Work inside your own home directory unless the task explicitly says otherwise.
- Do not delete, rename, or change permissions on system directories or files.
- Do not use recursive permission changes such as `chmod -R`.
- Never record or commit passwords, private keys, tokens, or other secrets.

## 4. Repository structure

```text
linux-user-management-fhs-practical/
├── README.md
├── .gitignore
├── GITHUB_GITBASH_GUIDE.md
├── SUBMISSION_CHECKLIST.md
├── commands/
│   └── command-log-template.md
├── evidence/
│   ├── evidence-log.md
│   └── README.md
├── screenshots/
│   └── README.md
└── workspace-template/
    ├── config/
    │   └── app.conf.example
    ├── documents/
    │   ├── overview.txt
    │   └── checklist.txt
    ├── backups/
    │   └── README.md
    └── evidence/
        └── README.md
```

The `workspace-template/` folder is a documentation/template representation of the Linux workspace you will create in your Linux home directory. It is not a substitute for performing the practical in the VM.

## 5. Evidence to capture

Save genuine screenshots or terminal captures in `screenshots/`. Suggested filenames:

- `01-user-creation-and-identity.png`
- `02-fhs-navigation.png`
- `03-ls-and-hidden-directory.png`
- `04-workspace-and-text-files.png`
- `05-final-app-config.png`
- `06-copy-move-remove.png`
- `07-find-and-grep.png`
- `08-permissions-and-id.png`
- `09-final-directory-tree.png`

Capture readable terminal output. Make sure no password or secret is visible. Record what each screenshot demonstrates in `evidence/evidence-log.md`.

## 6. Completion and submission

- [ ] All nine practical tasks completed in the Linux VM.
- [ ] New account verified with `whoami`, `id`, `pwd`, and `$HOME`.
- [ ] FHS locations and purposes documented.
- [ ] `ls`, `ls -l`, and `ls -a` demonstrated.
- [ ] Hidden `.lab-notes` directory created and verified.
- [ ] Required workspace and text files created using `nano`.
- [ ] Final `app.conf` content verified.
- [ ] Copy, rename, and remove operations verified.
- [ ] `find` and `grep` searches recorded.
- [ ] Permissions `644` and `600` applied and verified.
- [ ] Reflection questions answered.
- [ ] Screenshots and evidence log reviewed for secrets.
- [ ] Repository pushed to GitHub.

See [GITHUB_GITBASH_GUIDE.md](GITHUB_GITBASH_GUIDE.md) for the Git Bash upload steps.

## 7. Reflection questions

Answer these in `evidence/evidence-log.md` using your own words:

1. Why is it important to use a separate user account instead of performing everyday work as root?
2. What is one practical difference between `/etc` and `/var`?
3. Why might a hidden file or directory not appear in a normal `ls` listing?
4. What is the difference between `find` and `grep`?
5. Why should you verify permissions after running `chmod`?
