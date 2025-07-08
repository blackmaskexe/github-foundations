# Merge Conflicts

- Merge conflicts happen when Git can’t automatically combine changes from different branches.
- Most common when two people edit the same line, or when a file is changed in two branches in ways that can’t be merged cleanly.
	  - for example, Bob and Bill both have the job of manually updating user data in a file database.txt
	  - Bob accidentally updated the information for a user that Bill was responsible for updating
	  - Now, but Bob and Bill have updated information for the same user in the file database.txt, whose version will be considered in the final output after merging?
	  - the answer is: NONE, there will be a merge conflict that would ne required to manually resolve

## How do you know you have a merge conflict?
- You’ll see a message in your terminal after a merge attempt:  
  `CONFLICT (content): Merge conflict in <filename>`
## How to resolve a merge conflict:
1. **Open the conflicted file(s)**  
 - Look for `<<<<<<<`, `=======`, `>>>>>>>` markers.
 - Decide which changes to keep (yours, theirs, or a mix).
 - Edit the file to remove the markers and keep only what you want.

2. **Mark as resolved**  
 - After editing, stage the resolved file:
   ```bash
   git add <filename>
   ```

3. **Complete the merge**  
 - If all conflicts are resolved and staged, finish the merge:
   ```bash
   git commit
   ```
 - (If you were in the middle of a merge, Git may auto-create the commit.)

## Pro tips:
- Use a merge tool for easier conflict resolution:
```bash
git mergetool
```

