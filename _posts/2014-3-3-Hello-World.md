---
layout: post
title: The very basics of Git and GitHub
---

In this post, I will discribe the very basics of git and GitHub and where you can go to find out more.

First, what are git and GitHub? Git is a program that can track versions of your files, such that you can effectively "undo" changes to your files, or store and switch between saveral versions of your files at once. GitHub is a website that allows you to store your git tracked files online, and share them with other people (think Google Docs but for coders). 

Git is a super powerful and interesting tool, but it can be quite intimidating to use when you are just starting out. My advice is to start with these 3 steps (in this order):

1)Memorize the very basic git commands:

* Clone:
    * Lets say you would like to start working on some code that is already on GitHub (because, say, your brother started a project and invited you to start helping him out!). First, go to the repository on GitHub that you would like to start working on. Click on the friendly grean button that says "Clone or Download" and then copy the url (or click on the clipboard icon). 
    * Then go to your terminal and cd (change directory) to the folder that you would like to put your new project in. Then type `git clone https://github.com/kurrels/blog.git` (replacing the url with your copied url of course).
    * When you do this, git will clone your code to into your current repository.
* Status
    * 'Status' just gives you some information about your git repository.
    For example, after you have changed some files, you can type `git status`, and git will tell you which files you have changed. Notice here that I made a change to _posts/2014-3-3-Hello-World.md.
    
![git_status_example.png]({{ site.baseurl }}/images/git_status_example.png "git_status_example.png")

* Add and Commit
    * Making a commit is like taking a snapshot of your files. At first, don't worry too much about what a commit is. Just trust me that if you want make your changes show up on GitHub (and not just stay local to your computer), you'll first have to make at least one commit. 
    * But before you commit your files, you must first "add" them. When you type `git add example_file.txt` you add the file to the 'staging area'. If you then type `git status` again, git will reflect this change.
    ![]({{ site.baseurl }}/images/git_add_example.png "")
    * You can 'git add' as many files as you like before you make a commit. Then when you make a commit, git takes all the files that are in the 'staging area' (again, don't worry too much about what this means) and records that changes have been made to those files (git will not commit files that are not in the staging area).
    * When you make a commit, you must label the commit with a message. People generally use that message to discribe what changes they made in that commit. To make a commit type `git commit -m "updates first blog post"` (with your own message of course).
    
![git_commit_example.png]({{ site.baseurl }}/images/git_commit_example.png "git_commit_example.png")

* Push
    * Once you have made at least one commit, you can then 'push' your changes to GitHub. This assumes, however, that you have the correct permisions to the project on GitHub. Chances are, if you didn't set up the project yourself, or were added to the project by someone else, you don't have permission to directly make pushes to that project. If that is the case, I suggest you look into forking a repository, and making pull requests (see the second link in the next section)
    * But if you do have the correct permisions, updating the project on GitHub is as easy as typing `git push origin head`. Again, don't worry too much about what "origin" or "head" mean at first. Just understand that this command will take the changes that you made locally, and apply them to the project on GitHub.

![git_push_example.png]({{ site.baseurl }}/images/git_push_example.png "git_push_example.png")

* Pull 
    * Lets say your friend has made some changes and 'pushed' their changes to the project on GitHub. You can get those latest changes by 'pulling.' From within the correct directory, you can type `git pull`. This will download your friends changes and let you view them on your computer.

![git_pull_example.png]({{ site.baseurl }}/images/git_pull_example.png "git_pull_example.png")
    * If you try to push to GitHub without first 'pulling' the changes that were made since the last time you pulled, git will complain. If it does, simply `git pull` the latest changes, then try `git push origin head` again. That usually will work.
    
![git_push_fail_example.png]({{ site.baseurl }}/images/git_push_fail_example.png "git_push_fail_example.png")

2)Learn more about git and github, both from a theoretical perspective, and by learning more about what can be done with git. I recomend the following following resources (in this order):

1) http://gitimmersion.com/lab_01.html (do the first 20 or 30 slides or so at least.)
Even if you don't understand or remember all of this, just working through it will help you later because you will at least have a better idea of what to google in the future when you are trying to figure out how to do something in git.

2) https://www.youtube.com/watch?v=75_UrC2unv4&feature=youtu.be
This video will help you see how to collaberate on open source projects on GitHub

3)when you don't remember a command, or don't understand an error, just google it. In general, you'll get higher quality hits by restricting your search to stackoverflow like this: "how to undo a commit site:stackoverflow.com". In general, you'll get higher quality hits by restricting your search to stackoverflow.

4)in the end, if you completely mess everything up, there's always this: https://xkcd.com/1597/

Let me know if you have any questions or proposed modifications to this post.
