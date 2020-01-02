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

#### add the file you want to commit and push to git repository
> git add git_manipulation.ipynb

(Git add . #means add all files in this folder)

--

#### (optional) undo 'git add' before commit

> git reset < file_name >

(git reset (this will reset all files added))

https://stackoverflow.com/questions/348170/how-do-i-undo-git-add-before-commit

--

#### commit with message
> git commit -m "message"

--

#### (optional) reset previous commit

![img1](https://www.git-tower.com/learn/media/pages/git/faq/undo-last-commit/-885409906-1575572522/02-reset-concept.png)

To check every commit_id

> git log --oneline

> git reset ca4a800^  --> means back to previous 1 commit(s) of this commit_id

(git reset ca4a800~5) --> means back to previous 5 commit(s) of this commit_id

https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-local-commits-in-git

--

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


> cp ./pyenv_git.txt ../git

> git add .

> git commit -m "new version"

> git push origin -u practice_branch



---

Links

https://git-scm.com/docs

https://oawan.me/2016/all-about-git-command/

https://medium.com/@weilihmen/git-%E5%9F%BA%E6%9C%AC%E7%9F%A5%E8%AD%98-from-alpha-camp-5c9ef85cf825

https://gitbook.tw/chapters/using-git/reset-commit.html
