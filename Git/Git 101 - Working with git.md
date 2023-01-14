Using git in your projects can help you with the organization of the project, collaborating with others and backtracking to an older version. 
There are many ways to make use of git inside of your project, including the tools.
My personal set up of choice is [Github Desktop](https://desktop.github.com/) to have an easy to use GUI that keeps things simple, alongside with [git bash](https://git-scm.com/downloads) when I need to do more advanced operations and finally [Visual Studio Code](https://code.visualstudio.com/) to help with diagnosing merge conflicts.
I encourage you to try and experiment with tools to find the right fit for you.

In order to use git effectively, you should approach it by seeing what you do in units of work; for example, creating a script file that makes a player move is a unit of work. 
Adding a function to it to allow the player to jump can be seen as another unit of work. 
Git can track all these units of work in its history and even allows for branching in this history.

Here is an example of how part of a remote's history might look:
![git example](https://user-images.githubusercontent.com/22686676/211849571-c0037ff2-2e12-4303-866d-3e3004c03f53.svg)
It has multiple branches that are worked on simultaniously.

Branches are used to work separately from the main project, this makes it easier for you to focus on a singular feature at a time. 
Effectively, when using branches this way, you can see them as a small collection of units of work.
In order to use branches effectively you want your branches to be straight to the point and to wrap them up quickly to avoid drifting out of sync with the main branch.

Multiple people can work on the same project at once, separated from each other. However, when two people work on the same file at the same time, it is possible to create a merge conflict. This means that git cannot reliably decide how it will fit in the git history.
In order to solve this conflict, you must look at the changes made by both sides and decide what will happen, this can take some time and you might have to involve the other person in order to solve the merge conflict without breaking things.
The best advice is to avoid merge conflicts in general. \
'An Ounce of Prevention Is Worth a Pound of Cure'

Finally, I want to talk about pull requests, pull requests are used in a team when you want to have your branch merged to the main, but be inspected first. 
They allow you to have systems and other people in your team check your work for any faults and discussion points. Just like branches, you don't want to fatten up your pull requests with unnecessary work.

As a bonus, here is a list of useful terminology that you might come across:
* git - A system for keeping track of changes in a project.
* repository - The place where your project gets tracked by git.
* commit - A point in the git history containing a set of changes.
* changes - a change made to a file, for example fixing a spelling mistake.
* main branch - The default branch of your git repository. Sometimes, people use 'default' or 'master' instead.
* feature branches - a branch made to create a single feature for your project that has not yet been added to the main branch.
* merge conflict - A problem where multiple changes cannot be merged automatically.

When collaborating on open source projects, I use the following flow chart as guideline for how I iterate with git:
![git flow chart](https://user-images.githubusercontent.com/22686676/211849557-a58530f5-e043-4778-9df8-62d417e4259b.svg)

