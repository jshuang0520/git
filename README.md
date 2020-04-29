# git

## workflow
![img1](https://miro.medium.com/proxy/0*psCSE-BxW3zn4Ya1.png)

---

## Notes
- [Git Manipulation](http://nbviewer.jupyter.org/github/jshuang0520/git/blob/master/git_manipulation.ipynb)

---

### switch role

> git config --global user.email "you@example.com"

> git config --global user.name "Your Name"

---

## Steps:

#### clone repositary
> git clone [the repository url]

#### change direction to the folder
> cd git

#### to make a new branch
> git branch practice_branch

#### switch to that branch
> git checkout practice_branch

#### check all the branches, and to ensure you switched to the branch
> git branch -al

#### check unsaved changes (not yet pushed to git)
> git status

#### the file you want to commit and push to git repository
> git add git_manipulation.ipynb

(git add .  --> means add all files in this folder)

[Difference between “git add -A” and “git add .”](https://stackoverflow.com/questions/572549/difference-between-git-add-a-and-git-add)

Summary:

- git add -A  : stages all changes

- git add .   : stages new files and modifications, without deletions

- git add -u  : stages modifications and deletions, without new files


#### commit with message
> git commit -m "message"

#### push to the branch
> git push origin -u practice_branch

(-u only for the first time)


--


#### What is the best (and safest) way to merge a Git branch into master?
> git checkout master

> git pull origin master

> git merge practice_branch

> git push origin master



--


#### co-work with others: 
[A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/)

[How can I visualize Git Flow branches?](https://superuser.com/questions/699094/how-can-i-visualize-git-flow-branches)
> $ git log --all --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
![img-visualize-git-flow-branches](https://i.stack.imgur.com/jbxOX.png)

[create make a new branch from another branch](https://stackoverflow.com/questions/4470523/create-a-branch-in-git-from-another-branch)

pattern: git checkout -b < derived-branch > < original-branch >

> $ git checkout -b plot/hotspot poc/neo4j

or just cd to your current original-branch, then: git checkout -b < derived-branch > 
> $ git checkout -b plot/hotspot

![img-create-branch-from another-branch](https://i.stack.imgur.com/6qEWk.jpg)


#### Visualize git branches
(Visualizing branch topology in Git)[https://stackoverflow.com/questions/1838873/visualizing-branch-topology-in-git/11594406]


#### git flow
[git flow](https://github.com/nvie/gitflow)

--


> cp ./pyenv_git.txt ../git

> git add .

> git commit -m "new version"

> git push origin -u practice_branch



---

#### (optional) undo 'git add' before commit

> git reset < file_name >

(git reset (this will reset all files added))

https://stackoverflow.com/questions/348170/how-do-i-undo-git-add-before-commit

--

#### (optional) reset previous commit

![img1](https://www.git-tower.com/learn/media/pages/git/faq/undo-last-commit/-885409906-1575572522/02-reset-concept.png)

To check every commit_id

> git log --oneline

> git reset ca4a800^  // --> means back to previous 1 commit(s) of this commit_id

(git reset ca4a800~5) // --> means back to previous 5 commit(s) of this commit_id

https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-local-commits-in-git

---

### (often) when collaborating with others (confronting any changes on git - different from your local side)
> git fetch origin practice_branch  // pattern ->  git fetch <repo_name> <branch_name>

> git merge practice_branch // pattern ->  git merge <branch_name>

### In its default mode, git pull is shorthand for git fetch followed by git merge FETCH_HEAD.

### git : pull = fetch + merge FETCH_HEAD

![img2](https://i.stack.imgur.com/zUInQ.png)
[What is the difference between 'git pull' and 'git fetch'?](https://stackoverflow.com/questions/292357/what-is-the-difference-between-git-pull-and-git-fetch)

### But this : [GIT: FETCH AND MERGE, DON’T PULL](https://longair.net/blog/2009/04/16/git-fetch-and-merge/)

---

Links

https://git-scm.com/docs

https://oawan.me/2016/all-about-git-command/

https://medium.com/@weilihmen/git-%E5%9F%BA%E6%9C%AC%E7%9F%A5%E8%AD%98-from-alpha-camp-5c9ef85cf825

https://gitbook.tw/chapters/using-git/reset-commit.html


---

### check current username & email in your local repo
> git config user.name

> git config user.email

or 
> git config --list

### [How to switch git user at terminal?](https://superuser.com/questions/1064197/how-to-switch-git-user-at-terminal)

#### Change username and email global
> git config --global user.name "Bob"

> git config --global user.email "bob@example.com"

#### Change username and email for current repo
> git config  user.name "Bob"

> git config  user.email "bob@example.com"

--

### [Git push results in “Authentication Failed”](https://stackoverflow.com/questions/17659206/git-push-results-in-authentication-failed)
> two-factor authentication enabled would encounter this issue

```
If you enabled two-factor authentication in your Github account you won't be able to push via HTTPS using your accounts password. Instead you need to generate a personal access token.


Or you encountered the following:
remote: Permission to ooo/xxx.git denied to <user.email>.
fatal: unable to access 'https://github.com/ooo/xxx.git/': The requested URL returned error: 403

do this:
$ git remote set-url origin < something cloned with SSH >
$ git remote set-url origin git@github.com:zkirkland/Random-Python-Tests.git

```


```
If you enabled two-factor authentication in your Github account 
you won't be able to push via HTTPS using your accounts password. 

Instead you need to generate a personal access token.
```
