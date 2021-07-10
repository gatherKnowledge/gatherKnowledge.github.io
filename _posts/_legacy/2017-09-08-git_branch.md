---
layout: post
title: git branch 관련 명령
categories: [git]
tags: [CVS, git]
fullview: true
comments: true
published: true
---
### git branch command
#### 브런치 생성
```gitbash
$ git branch <BranchName>
$ git checkout <BranchName>

    [master]
        |
        |
    O---O
        |
        O
        |
        |
    [newBranch]
```

#### 브런치 병합
```gitbash
$ git checkout <Master>
$ git merge <Slave>  

            [master]
                |
                |
    O---O-------O
        |     /
        O---O
            |
            |
        [branch]
```
