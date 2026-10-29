# git-practical
Temporarily Store and Restore Uncommitted Changes Using git stash
commands:
cd git-practical
echo "Original content" > notes.txt
git add notes.txt
git commit -m "Add original notes"

echo "Temporary work" >> notes.txt
git stash push -m "Save temporary work"
git status
git stash pop
cat notes.txt

output:
[main xxxxxx] Add original notes
 1 file changed, 1 insertion(+)
 create mode 100644 notes.txt

Saved working directory and index state On main: Save temporary work

On branch main
nothing to commit, working tree clean

On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   notes.txt

no changes added to commit (use "git add" and/or "git commit -a")

Original content
Temporary work
