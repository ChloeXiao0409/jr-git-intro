## Git ##

1. Suppose you had a file, called first.md, and you made a copy of this file, named it second.md and made some changes to it. Next, suppose you ran diff -u first.md second.md.Here is the content of the original first.md:
`A B C D E F` Here is the output of the diff command:
What is the content of second.md?

- Because + means some content second file has but first file doesn’t and – means first file has but the second file doesn’t, and others remain the same with sign before.
Therefore, the content of second.md as follows:
**`A B $ C # % E F`**

2.	(True or False) If you accidentally add a file to the staging area, you can remove it using git reset. For example, if you accidentally add thrid.md, but don’t want it to be committed yet, run git reset thrid.md and the file will be removed from the staging area, but it will still be in your working directory.

- **True**. Because this command line will just remove thrid.md from the staging area. Which means it won't be included in the next commit. And also it leaves the file untouched in the working directory, and the changes you made will still be present but just will not be committed.

3.	(True or False) The commands git reset and git revert can only be used to undo commits in the git repository.

- **False**:\
**git reset**: Can undo more than just commits. It also can: unstage files and modify the working directory (depending on the reset mode: --soft, --mixed, or --hard).\
**git revert**: Can only undo commits, it creates a new commit that reverses the changes made by a previous commit, and it does not affect the staging area or working directory.

4.	(True or False) The commands git checkout can be used to roll back to a certain commit hash (check the documentation if you are unsure).

- **True**. This moves your HEAD pointer to the specified commit, allowing you to inspect or work with that version of the repository.

5.	(True or False) We cannot commit changes in the working directory directly to the repo without adding it to the staging index first (read the documentation if you are unsure).

- **False**. Git provides an option by using the command line of git commit -a to bypass the staging area and commit changes in the working directory directly, but only for tracked files.

6.	(True or False) git log -p and git log will give you the same output.

- **False**. \
**git log** gives a high-level overview of the commit history, include Commit hash, Author name and email, Date, Commit message.\
**git log -p** includes more detailed changes (diffs) for each commit in addition to the standard git log output.

7.	(True or False) git log --oneline and git log --stat will give you the same output.

- **False**.\
**git log –oneline**: Displays a concise summary of the commit history. Show commit history as a single line with Commit hash (shortened) and Commit message.\
**git log --stat**: Displays the commit history with statistics about changes made in each commit. It Shows: Commit hash, author, and message with a summary of changes per file which shows Number of lines added and removed and Total number of files changed, and lines added/removed.

8.	(True or False) It is recommended that in most cases we should use git revert rather than git reset to undo commits because git revert is safer.

- **True**.\
**git revert** creates a new commit that undoes the changes made by a previous commit, preserving the history and ensuring that others are not affected by changes to the commit history.\
**git reset**, on the other hand, can alter the commit history, which can cause issues if others have already pulled or are working with those commits. It is more commonly used for local changes and should be used with caution in collaborative scenarios.
