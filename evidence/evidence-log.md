# Evidence log

**Student name:**  
**Date:**  
**Linux distribution/version:**  
**Linux username created for this assessment:**  

## Task 1 - User creation and identity

Commands actually run:

```bash
# Paste commands here, excluding any password.
```

Observed output / notes:

- `whoami`:
- `id`:
- `pwd`:
- `$HOME`:

Screenshot(s):

## Task 2 - FHS navigation

| Path | Typical purpose (in your own words) | How you verified it |
|---|---|---|
| `/` | | |
| `/home` | | |
| `/etc` | | |
| `/var` | | |
| `/tmp` | | |
| `/usr` | | |
| `/bin` | | |

## Task 3 - Listings and hidden directory

Difference observed between `ls`, `ls -l`, and `ls -a`:

How `.lab-notes` was verified:

Screenshot(s):

## Task 4 - Workspace and documents

Describe the created directory structure:

What did you write in `overview.txt` and `checklist.txt`?

Screenshot(s):

## Task 5 - Configuration file

Paste the final `app.conf` contents below (ensure the OWNER value is your lab username and no secret is included):

```ini
# Paste final contents here
```

How did you verify it?

Screenshot(s):

## Task 6 - Copy, move, and remove

Record each operation and how you verified it:

- `overview.txt` copied to backups:
- `app.conf` copied to backups:
- `checklist.txt` renamed to `tasks.txt`:
- `remove-me.txt` created and removed:

Screenshot(s):

## Task 7 - Search

- `find` command and matching output:
- `grep` command for overview text and matching output:
- `grep` command for `LOG_LEVEL` and matching output:

Screenshot(s):

## Task 8 - Permissions and identity

- `app.conf` permission shown by `ls -l`:
- `tasks.txt` permission shown by `ls -l`:
- Meaning of permission value `644`:
- Meaning of permission value `600`:
- What `id` displays about the current user and groups:

Screenshot(s):

## Task 9 - Final verification

Paste or summarize the output of:

```bash
find ~/linux-practical -maxdepth 2 -print
ls -la ~/linux-practical
```

Screenshot(s):

## Reflection questions

1. Why is it important to use a separate user account instead of performing everyday work as root?

2. What is one practical difference between `/etc` and `/var`?

3. Why might a hidden file or directory not appear in a normal `ls` listing?

4. What is the difference between `find` and `grep`?

5. Why should you verify permissions after running `chmod`?

## Final notes / distribution differences

Record any command unavailable on your distribution, what alternative you used, and why.
