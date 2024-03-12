# logging into ```ieng6```
![image](https://github.com/apalecki/cse15l-lab-reports/assets/104041328/b8bae894-0db0-48af-b127-6ff0a619d11e)
I used `ssh` to login to `apalecki@ieng6.ucsd.edu` and then clicked the  `<enter>` key.

# `clone` repo
![image](https://github.com/apalecki/cse15l-lab-reports/assets/104041328/6cbdcaec-327f-4e37-a4ed-8eb548299069)
I cloned my fork of the `lab7` repo, using my `ssh` url. I did this by typing `git clone git@github.com:apalecki/lab7.git` and pressing `<enter>`

# Testing code
![image](https://github.com/apalecki/cse15l-lab-reports/assets/104041328/8a01bebe-310e-4d88-9eba-d2389062636a)
After cloning the `lab7` repo, i did `cd lab7` and pressed `<enter>`, then ran the tests by typing `bash test.sh` and pressing `<enter>`.

# Fixing code
![image](https://github.com/apalecki/cse15l-lab-reports/assets/104041328/dcda9be2-724c-4042-b40b-a68012be6b1a)
By typing `vim ListExamples.java` I was able to enter the editor. My cursor started over the top line so i did `<down>` 44 times then `<right>` 11 times to hover over the `index1` I needed to change to `index2`.
I fixed it my deleting the 1 by pressing `x` and then inserting a 2 by pressing `i` then `2` on the keyboard to insert the 2. I then pressed `<esc>` and typed `:wq` and hit `<enter>` to exit and save file.

# Retesting code
![image](https://github.com/apalecki/cse15l-lab-reports/assets/104041328/088026f0-d894-40b7-97af-3264c96ceb0e)
I ran the `test.sh` script again to check if my changes worked and they did. I did this by typing `bash test.sh` and clicking `<enter>` to get the output above.

# Comit to git
![image](https://github.com/apalecki/cse15l-lab-reports/assets/104041328/3e399a74-b4ac-4ba2-a87c-afabaa287741)
I commited my changes to my fork on github by typing `git add ListExamples.java` and clicked `<enter>`, then I typed `git commit -m "Lab Report"`. Next, I typed `git push origin` and clicked `<enter>` which finally pushed all of my changes to the git repo.
