<a id="anchor"></a>

# Working with Git
---

git config --global user.name "Yevhen Rudyk" <br>
git config --global user.email mr.yrudyk@gmail.com <br>
git config --global core.editor nano <br>

---
git init <br>
mkdir m1/task1.1 <br>
touch m1/task1.1/readme.txt <br>
git add . <br>
git commit -m "Init commit" <br>
git checkout -b develop 
touch m1/task1.1/index.html <br>
git add . <br>
git commit -a -m "Create .html file" <br>
git checkout -b images <br>
mkdir m1/task1.1/images #add images <br>
git add . <br>
git commit -m "Add images" <br>
nano m1/task1.1/index.html <br>
git add . <br>
git commit -m "Add images link to html file" <br>
git checkout develop <br>
git checkout -b styles <br>
touch m1/task1.1/styles/styles.css <br>
git add . <br>
git commit -m "Add styles file" <br>
nano m1/task1.1/index.html <br>
git add . <br>
git commit -m "Add link to html" <br>
git checkout develop <br>
git merge images <br>
git merge styles <br>
git add . <br>
git commit -m "Resolve conflict" <br>
git checkout master <br>
git merge develop <br>
git push origin --all <br>

#_[Git log](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task1.1/task1.1_GIT.txt)_

---

# Who are you devops
DevOps is a methodology (state of mind). Methodology - automation, continuous code delivery. It embodies all the best qualities from a developer, tester, system administrator. He is the link between them. Devops - automates everything that moves and what does not move, moves and automates.

[Up](#anchor)
