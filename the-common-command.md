```
git init
git config --system/--global/--local  --list
git config --global user.name   "wangliang"
git config --global user.email  "1010882388@qq.com"

## 使用git config命令编辑配置文件
仓库级的config   git config –local -e
全局级的config   git config –global -e
系统级的config   git config –system -e
## 增加一个配置项
格式: git config [–local|–global|–system] –add section.key value(默认是添加在local配置中)  
     git config --add my.name wangliang
     git config --get my.name
## 删除一个配置项
格式：git config [–local|–global|–system] –unset section.key
     git config --unset my.name

git remote add wlgit git@github.com:fight-for-future-and-family/git-note.git

git add file
git commit -m "the changes of this time"

git status
git branch
git log
```
---
#### the file is ~/.gitconfig
```
[alias]
        lg1 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all
        lg2 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n''          %C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all
        lg = !"git lg1"
```
---
```
git checkout master/bugFix/wl
git checkout C1
git branch wl
git checkout -b wl
git branch -f new-branch C9

git rebase master
git cherry-pick   C3 C8 C10
git rebase -i C5 C3 C2 C4            /      git rebase -i HEAD~6

## local
git reset bugFix          
## remote
git revert bugFix
```