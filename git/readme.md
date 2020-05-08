# 清除历史大文件
* git filter-branch --force --index-filter 'git rm -r --cached --ignore-unmatch {target/}' --prune-empty --tag-name-filter cat -- --all  
 {target/} 代表本地文件路径
* rm -rf .git/refs/original/
* git reflog expire --expire=now --all
* git gc --prune=now
* git gc --aggressive --prune=now
* git push --force --all

## 远程需要赋权限 chmod 777 -R ./


# git log中文乱码问题
 ```
 git config --global i18n.commitencoding utf-8
 git config --global i18n.logoutputencoding utf-8
 export LESSCHARSET=utf-8
 ```
