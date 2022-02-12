<a id="anchor"></a>

# Working with Git
---

###### git config --global user.name "Yevhen Rudyk"
###### git config --global user.email mr.yrudyk@gmail.com
###### git config --global core.editor nano

---
###### git init
###### mkdir m1/task1.1
###### touch m1/task1.1/readme.txt
###### git add .
###### git commit -m "Init commit"
###### git checkout -b develop 
###### touch m1/task1.1/index.html
###### git add .
###### git commit -a -m "Create .html file"
###### git checkout -b images 
###### mkdir m1/task1.1/images #add images
###### git add .
###### git commit -m "Add images" 
###### nano m1/task1.1/index.html
###### git add .
###### git commit -m "Add images link to html file" 
###### git checkout develop
###### git checkout -b styles 
###### mkdir m1/task1.1/styles
###### touch m1/task1.1/styles/styles.css
###### git add .
###### git commit -m "Add styles file" 
###### nano m1/task1.1/index.html
###### git add .
###### git commit -m "Add link to html"
###### git checkout develop
###### git merge images
###### git merge styles
###### git add .
###### git commit -m "Resolve conflict"
###### git checkout master
###### git merge develop
###### git push origin --all

#_[Git log](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task1.1/task1.1_GIT.txt)_

---

# Who are you devops
DevOps is a methodology (a state of mind and soul). It embodies all the best qualities from a developer, tester, system administrator. He is the link between them and his work that prevents them from killing each other. Devops - automates everything that moves and what does not move, it moves and automates.

[Up](#anchor)
