# git

## workflow
![img1](https://miro.medium.com/proxy/0*psCSE-BxW3zn4Ya1.png)

---

## Notes
- [Git Manipulation](http://nbviewer.jupyter.org/github/jshuang0520/git/blob/master/git_manipulation.ipynb)

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

#### add the file you want to commit and push to git repository
> git add git_manipulation.ipynb
(Git add . #means add all files in this folder)

#### commit with message
git commit -m "message"

#### push to the branch
> git push origin -u practice_branch


#### What is the best (and safest) way to merge a Git branch into master?
> git checkout master

> git pull origin master

> git merge practice_branch

> git push origin master



--


#### co-work with others: 
[create make a new branch from another branch](https://stackoverflow.com/questions/4470523/create-a-branch-in-git-from-another-branch)

pattern: git checkout -b <derived-branch> <original-branch>
git checkout -b plot/hotspot poc/neo4j

or just cd to your current original-branch, then: git checkout -b <derived-branch> 
> git checkout -b plot/hotspot

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

Links

https://git-scm.com/docs

https://oawan.me/2016/all-about-git-command/

https://medium.com/@weilihmen/git-%E5%9F%BA%E6%9C%AC%E7%9F%A5%E8%AD%98-from-alpha-camp-5c9ef85cf825

