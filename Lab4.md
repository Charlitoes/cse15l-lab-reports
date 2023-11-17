**VIM**


Steps 4-9


4) **Log into ieng6**


I typed all of this out `ssh c2trinh@ieng6-201.ucsd.edu`
![insert](lab4_step_4.png)


**Step4 Summary**


I entered into my ieng6 account by using the ssh command with my ieng6 account.


5) **Clone your fork of the repository from your Github account (using the SSH URL)**


I copy and pasted (using `<ctrl+c><ctrl+v>`) this `git clone https://github.com/Charlitoes/lab7`
![insert](lab4_step_5.png)


**Step5 Summary**


I copy and pasted the repository we wanted to `git clone` in which was a forked version of the lab7 repository. This is the reason why in the github link, it has my username in the URL instead of cloning the original one which has ucsd-cse15l-s23 in the URL.


6) **Run the tests, demonstrating that they fail**


```
cd l<tab>
bash t<tab>
```
![insert](lab4_step_6.png)


**Step6 Summary**


I started to use shortcuts such as `<tab>` so it would autofill the file I am trying to either cd into or bash with. I first cd into the `lab7` directory after it got cloned into my ieng6 account. Then I ran the bash script `test.sh` to see that the tests failed.



7) **Edit the code file to fix the failing test**


```
vim Li<tab>.java
```
![insert](lab4_step_7p2.png)


*Inside VIM*


```
/index1 <enter> n (pressed 9 times) l (pressed 5 times) r 2 :wq
```


![insert](lab4_step_7.png)


**Step7 Summary**


In this step, I fixed the bug that was causing the tests to fail by using vim to edit the `.java` file. I first used the command `vim` and then typed out `Li<tab>` which auto-filled it to `ListExamples` (it didn't auto-fill the whole thing because we have another similar file named `ListExamplesTests` which is the reason why it shorted the auto correct. Since it shorted it I just typed out the rest of the characters for the java file I wanted to edit. The finished command looked like this, `ListExamples.java`. Then I executed this command and now we are in VIM. Inside VIM, I searched for `index1` since we knew that `index1` had a bug. So I typed out `/index1<enter>` which is basically the equivalent to ctrl+f in a Chrome tab to search for specific words in a document. I pressed n 9 times to look through every iteration of `index1` until I found the bugged one. I then pressed l 5 times to move my curser under the 1 in `index1` since we know that it should be index2 instead. Then when the curser was under the 1 I pressed `r 2` which would replace the character that my curser is under and pressing 2 is what it is replacing it with. Lastly, to save the change I made I use `:wq` which means to save (the w) and then quit (the q).


8) **Run the tests, demonstrating that they now succeed**

```
<up><up><up><enter>
```

![insert](lab4_step_8.png)


**Step8 Summary** 


We are now back to the regular terminal and I want to test `ListExamples` again so since I already ran the command a little while ago I pressed `<up>` 3 times and then pressed `<enter>` to execute the bash script `test.sh`.


9) **Commit and push the resulting change to your GitHub account (you can pick any commit message!)**


In all the code blocks I typed it all out by hand with no special shortcuts


```
git init
git status
```
![insert](lab4_step_9p1.png)


```
git add ListExamples.java
git status
git commit -m "changed index in ListExamples.java"
```
![insert](lab4_step_9p2.png)


```
git push origin main
```
![insert](lab4_step_9p3.png)



An image of the changed index in GitHub


![insert](lab4_step_9p4.png)


**Step9 Summary**


Now, to commit and push the changes we made to our repository, first I had to initialize a new git repo in the current directory by using the command `git init`. This would allow us to see what files can be committed and pushed to Git Hub. I then used `git status` to see the status of what has been changed, is staged, or isn't staged. I then used the `git add` command to stage the changed file which was `ListExamples.java` so the whole command would look like this `git add ListExamples.java`. I also checked the status once more to see that when it is staged the text color changed from red to green indicating that it is ready to get committed. To commit the staged file we could use the `git commit` command I also used `-m` here as well to include a message telling whoever is looking at this repo what I changed. The whole command would look like this `git commit -m "changed index in ListExamples.java"`. Lastly, I need to push the committed file by using the `git push` command then I put `origin main` in as well to indicate that I want to put the change in the origin repository in the main branch. The command looked like this `git push origin main`. I also included an image on GitHub in my repo that shows the changed index, which was changed from index1 to index2, fixing the file allowing the tests to pass.






