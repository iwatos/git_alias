# git_alias
```
[alias]
    s = status
    
    #コミットログ
    comlog = log --date=short --no-merges --pretty=format:'%cd %s %h (@%cn)'
    
    #現在のブランチ名
    brname = symbolic-ref --short HEAD
    
    #現在のブランチ名から"feature/"を除いたもの
    brname2 = !"git symbolic-ref --short HEAD | sed -e 's#feature/##g'"
    
    #add,status,commit
    mycommit = "!f() { git add -A && git s && git commit -m \"`git brname2`【mycommit】$1\";}; f"
```
