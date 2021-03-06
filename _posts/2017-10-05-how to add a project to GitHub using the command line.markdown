---
layout: post
title:  how to add a project to GitHub using the command line
date:   2017-10-05 08:40:00
description: add an existing project to your Github
comments: true
---

#### Assumptions

- You have a GitHub account
- You have a project on your local computer you want to add to your GitHub
- You are working on a Mac

#### Steps

- <b>Create a repository on GitHub</b>

<blockquote>
To avoid errors, do not initialize the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub.
	—<a href="https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/">GitHub Help</a>
</blockquote>

- <b>Run these commands in your terminal</b>

{% highlight ruby %}

cd YourProjectFolderName
git init 
git add .
git commit -m "first commit" # -m <msg> flag
git remote add origin https://github.com/YourGithubUsername/RepositoryName.git 
git push -u origin master # -u[<mode>] flag (untracked files)

{% endhighlight %}

If you're using HTTPS, your command will look like `https://github.com/YourGithubUsername/RepositoryName.git`. 

If you're using SSH, it will look like `git@github.com:YourGithubUsername/RepositoryName.git`.

If the `push` command fails, it might be caused by a change in your remote repository after the `init` command eg. you added a README. Try the following command `git push —f origin master` as your last command. Be cautious. This is the only time I would ever recommend using the `--force` command. Find further details <a href="https://developer.atlassian.com/blog/2015/04/force-with-lease/">here</a>.

<blockquote>
Git's push --force is destructive because it unconditionally overwrites the remote repository with whatever you have locally
	—<a href="https://developer.atlassian.com/blog/2015/04/force-with-lease/">Atlassian Developer</a>
</blockquote>

#### References 

<a href="https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/">GitHub Help</a>
<br /> 
<a href="https://developer.atlassian.com/blog/2015/04/force-with-lease/">Atlassian Developer</a>
