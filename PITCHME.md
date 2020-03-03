# Introduction to Git with Visual Studio

---

## Why Are We Here?

@ul
- Development is being migrated away from internally hosted Team Foundation Servers to Azure DevOps
- On TFS we are using TFS Version Control, on Azure DevOps we're using Git for version control
- Git and TFSVC are different which can cause confusion
- We're using Visual Studio internal Git support so have updated the introduction
@ulend

---

## Outline

@ul
- A quick overview of Git
- A chance to experiment with Git in the Scratch environment
@ulend

---

## Simple But Powerful

@ul
- The underlying concept of Git is beautifully simple, based around the commit 
- Each commit describing the changes from the previous commit
- Whilst simple, this concept is also tremendously powerful
@ulend

---

![Branch](assets/gitflow.png)

---

# But...

---

![GreatPower](assets/greatpower.jpg)

---

# Defenestrate Regularly

---

![Spaghetti](assets/branchspaghetti.gif)

---

## Beginnings

@ul
- Git started life as a week long project to replace the version control system managing contributions to the Linux Kernel 
- It had to be:
    - Fast
    - Simple Design
    - Strong support for non-linear development
    - Fully distributed
    - Able to handle large projects efficiently
@ulend

---

## Beginnings

@ul
- It is now almost the defacto standard for version control systems
- For a long while despite producing their own version control system for TFS, Microsoft teams were internally using Git
@ulend

---

## Top Tip

@ul
- When learning to use Git, try to *not* think about it in the same way as you do for TFS Version Control 
- Git stores and handles information differently from TFSVC and it can get confusing
@ulend

---

## Snapshots not Differences 

@ul
- Many other version control systems store information as details of changes to files
- Git thinks of its data more like a set of snapshots of a miniature file system, called commits 
- It uses links for unchanged files saving space
- It only stores the changes not complete files
- The git miniature file system can ignore files so you can keep binaries and temporary VS files out of the repo 
@ulend

---

## Nearly every operation is local 

@ul
- Git is designed to operate in a distributed way so has the entire history of a project locally
- If you need to go back to an old version of the file, Git can regenerate it locally 
- If a server repository fails or is corrupted the server can be built from local repositories
- When you want to share work with the team you push it up to Azure DevOps
@ulend

---

## Git has integrity

@ul
- Everything in Git is check-summed before it is stored
- Internally everything is referred to by that checksum, not a filename 
- You can't lose information in transit or have a file corrupt without Git knowing about it
@ulend

---

## Git generally only adds data

@ul
- It is very hard to get Git to remove or erase data from its internal database 
- Removing files *adds* a snapshot
- This makes it straightforward to step back on problems
@ulend

---

## Git vs TFS

|TFS Version Control|Git|
|---|---|
|Workspace|Repository / Repo|
|Get Latest  (First time)|Clone|
|Get Latest|Pull|
|Check in|Commit + Push|
|Check out|(just start typing)|

---

## Git vs TFS

|TFS Version Control|Git|
|---|---|
|Branch|Branch|
|Merge|Merge (or Rebase instead)|
|Code Review|“pull request”|
|Shelveset|Stash|
|Label|Tag|

---

## Git Tools

You don't have to use the tools in Visual Studio 

@ul
- Some complicated operations may require an external tool or command line
- Free clients like Atlassian SourceTree, Tortoise Git, Git for Windows
- Paid for clients like Git Kraken, Smart Git or Tower
@ulend

---

## Git Resources

Lots of Git resources and support around:

@ul
- Pro Git - Whole book is available for free online at [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
- Several Pluralsight courses can teach you the basics, or take a deep dive into how Git works
- Atlassian Git Cheat Sheet [https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)
@ulend

---

## Try it Yourself

Git is built in to Visual Studio but you can download and install the full git install from:

[https://gitforwindows.org/](https://gitforwindows.org/)

@ul
- In Visual Studio Installer you can also find **Git for Windows** under Individual Components.
- Visual Studio Code also had git support built in.
@ulend

---

## Try it Yourself

From a command line or Powershell run the following exactly - *do not substitute [user] with your username*:

```sh
> git config --global 
    http.proxy http://[user]@cseproxy.emea.cshare.net:8080
> git config --global credential.helper wincred
> git config --global http.proxyAuthMethod ntlm
```

---

## Try it Yourself

Clone the demo repository and create your branch:

- In VS2019 use the **Clone or check out code** option from the welcome page
- Our demo repo is at `https://CTS-GD@dev.azure.com/CTS-GD/Scratch/_git/gitdemo` or browse to find it
- In VS2019 create yourself a branch by going to **Team Explorer**, then **Branches** and **New Branch**

Now make some changes, for example edit `README.md`

---

## Try it Yourself

Add your changes and push them to the central repository:

- In VS2019 go to the **Team Explorer**, then **Changes**
- Describe your changes and then commit the changes to your local repo
- Once committed, click on **Sync** to share your changes with the server
- Click **Push** to push your new branch

---

## Try it Yourself

Create a pull request for your branch

- In a browser go to `https://dev.azure.com/CTS-GD/Scratch/_git/gitdemo/pullrequests`
- Azure DevOps should highlight your new branch - press **Create a pull request**
- Fill in the pull request form and add some reviewers

---

## Any Questions?

---