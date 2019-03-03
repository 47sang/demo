# 提交到远程仓库

- 接下来如果你直接提交会发现提交不了, 说远端做了更改需要先pull一下, 如果pull那就又回到最新版本了，相当于没回退。

- 思路：我们可以新建一个分支temp，然后把回退后的代码提交到temp分支上暂存，然后删除master主分支，新建一个master分支，提交现有代码到master上。

```
/*1.新建分支*/
git checkout -b temp              //新建分支并切换到temp分支
git push origin temp:temp         //将代码push到temp分支
/*2.删除主分支*/
git push origin --delete master   //删除远端主分支
git branch -d master              //删除本地主分支
/*3.新建主分支*/
git checkout -b master            //新建主分支并切换到主分支
git push origin master            //提交主分支
/*4.删除暂存分支*/
git branch -d temp
git push origin --delete temp
```