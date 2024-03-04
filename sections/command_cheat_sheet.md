

# Git commands

```sh
# Committing Staged Changes with a Message
git commit -m "Initial commit"

# Amend the Most Recent Commit
git commit --amend -m "Corrected commit message"

# Commit All Changes to Tracked Files (Staged and Unstaged)
git commit -a -m "Updated files with bug fixes"

# Add and Commit in One Step for Specific Files
git commit -am "Added new feature"

# Verbose Commit
git commit -v

# Interactively Select Changes to Commit
git commit -p

# Commit Using an External Editor
git commit

# Sign a Commit with GPG
git commit -S -m "Signed commit for security"

# Specify an Author for the Commit
git commit --author="Author Name <author@example.com>" -m "Commit on behalf of another author"

# Adding and Committing an Untracked File
git add <untracked-file>
git commit -m "Added new file"
```
