**VIM**


Steps 4-9


4) **Log into ieng6**


I typed all of this out `ssh c2trinh@ieng6-201.ucsd.edu`
![insert](lab4_step_4.png)


5) **Clone your fork of the repository from your Github account (using the SSH URL)**


I copy and pasted this `git clone https://github.com/Charlitoes/lab7`
![insert](lab4_step_5.png)


6) **Run the tests, demonstrating that they fail**


```
cd l<tab>
bash t<tab>
```
![insert](lab4_step_6.png)


7) **Edit the code file to fix the failing test**


```
vim Li<tab>.java
```
![insert](lab4_step_7p2.png)


*inside vim*


</index1><enter><n><n><n><n><n><n><n><n><n><l><l><l><l><l><r><2><:wq>


![insert](lab4_step_7.png)


8) **Run the tests, demonstrating that they now succeed**


<up><up><up><enter>
![insert](lab4_step_8.png)


9) **Commit and push the resulting change to your Github account (you can pick any commit message!)**


In all the codeblocks i typed it all out by hand with no special shortcuts


```
git init
git status
```
![insert](lab4_step_9p1.png)


```
git add ListExamples.java
git status
```
![insert](lab4_step_9p2.png)


```
git commit -m "changed index in ListExamples.java"
git push origin main
```
![insert](lab4_step_9p3.png)



An image of the changed index in GitHub
![insert](lab4_step_9p4.png)






