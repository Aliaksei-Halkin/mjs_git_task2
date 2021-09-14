### Task 2

#### Part 1
We are going to practice some skills obtained in the previous task. If you come across something you still don’t know, please use links provided in the descriptions, internet search, other mentees and you mentor as sources of knowledge and help.
For this task you will create two separate branches ***git\_1*** and ***git\_2*** in your remote repository and local <span class="underline">tracked</span> branches with same names. Both these branches should be made of the ***git\_task*** branch.
1. ***git\_1***: Add and commit *firstFile.txt* file with 10 lines.
2. ***git\_1***: Add and commit *secondFile.txt* file with 10 lines.
3. Merge branch ***git\_1*** to ***git\_2***
4. ***git\_2*:** Update and commit any **two** lines in *secondFile.txt*.
5. ***git\_1*:** Update and commit **the same** 2 lines with the different info in *secondFile.txt*
6. Merge branch ***git\_2*** to ***git\_1*,** resolve conflict. Left **all** (4) modified lines. Commit.
7. ***git\_1***: Update and commit 1.txt file, modify two lines.
8. ***git\_1***: Update and commit 1.txt file, modify **another** two lines.
9. Transfer changes of commit from <span class="underline">Step 7 only</span> to ***git\_2*,** using **format patch**.
10. Transfer changes of commit from <span class="underline">Step 8 only</span> to ***git\_2*,** using **cherrypick** command.
11. ***git\_2*:** Concatenate the last two commits using ***reset** + **commit*** commands.
12. ***git\_2*:** Change date, author and message of the last commit and add non-empty *thirdFile.txt* file to it.
13. ***git\_2***: Create a **new** commit that *reverts* changes of the last one.
14. ***git\_2*:** Create and commit *thirdFile.txt* file.
15. ***git\_2***: Run command that removes all changes of the last two commits.
16. Synchronize ***git\_1*** and ***git\_2*** with a remote repository.
17. Clone your project to another folder.
18. **folder2: *git\_1*:** Change two lines in *firstFile.txt*. **Commit** + **Push**.
19. **folder1: *git\_1*:** Change **another** two lines in *firstFile.txt*.
20. **folder1: *git\_1*:*   
    * Change **another** line in *firstFile.txt* (not the same as in 18, 19).
    * **Merge** changes from Step 18 (pull) **without** committing changes from Step 19 and any additional commits.
    * **Push**.
    * Return local state of Step 19. (***stash***)

#### Part 2
For this task you should learn how to use **interactive rebase**, thus other ways of achieving the same are prohibited. Show the following steps to your mentor during the demo:
1. Create ***git\_3*** branch from ***git\_task***. Checkout to ***git\_3***.
2. Add new empty file *doubtingFile.txt* and commit it.
3. Add a line to a file and commit changes. Do it 5 times. You should end up with 5 lines in a file and 6 commits: 1 for creating an empty file and 5 for adding a line.
4. Check you log and copy it somewhere.
5. Launch interactive rebase for 5 last commits, squash all the latest commits into the first one. Reword first commit. You should end up with 2 commits: 1 for creating an empty file and second for adding 5 lines. Second commit should have new commit message.
6. Check you log and compare it with the previous one. Look at the hash, date, commit message. Explain what changed and why.
7. Check you reflog. Explain to you mentor what you can see and why.