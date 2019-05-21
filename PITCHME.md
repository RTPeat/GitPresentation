# Introduction to Git

---

## Why Are We Here?

@ul
- Development is being migrated away from internally hosted Team Foundation Servers to Azure DevOps
- On TFS we are using TFS Version Control, Azure DevOps uses Git for version control
- Git and TFSVC are different which can cause confusion
@ulend

---

## Outline

@ul
- A quick overview of Git
- A demo of Git
- A chance to experiment with Git in the Scratch environment
@ulend

---

@ul
- The underlying concept of Git is beautifully simple, based around the commit. 
- Each commit describing the changes from the previous commit.
- Whilst simple, this concept is also tremendously powerful.
@ulend

---

![Branch](assets/gitflow.png)

---

# But...

---

![GreatPower](assets/greatpower.jpg)

---

![Spaghetti](assets/branchspaghetti.gif)

---

@ul
- Git started life as a week long project of Linus Torvalds to replace the old version control system they were using to manage contributions to the Linux Kernel. The new system had to be:
    - Fast
    - Simple Design
    - Strong support for non-linear development (thousands of parallel branches)
    - Fully distributed
    - Able to handle large projects like the Linux kernel efficiently in both speed and size
- It has accomplished this and as a result it is now almost the defacto standard for version control systems.
- For a long while despite producing their own version control system for TFS, Microsoft teams were internally using Git
@ulend

