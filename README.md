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

#### commit
> git commit

#### push to the branch
> git push -u practice_branch


#### What is the best (and safest) way to merge a Git branch into master?
> git checkout master

> git pull origin master

> git merge test

> git push origin master



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

