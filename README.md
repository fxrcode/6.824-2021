# 6.824-2021
* Can I finish it in 1 month as in Nanodegree Cloud-Developer?


# 快速拉取最新代码
0. `git clone git://g.csail.mit.edu/6.824-golabs-2021 6.824-2021`
* 拉取6.824最新2021代码，到本地directory: `6.824-2021`

1. 通过git remote -v查看是否有源头仓库的别名和地址。
```
$ git remote -v
# fxrc @ popos in ~/Projects/6.824-2021 on git:master x [0:07:20] 
$ git remote -v
origin  git://g.csail.mit.edu/6.824-golabs-2021 (fetch)
origin  git://g.csail.mit.edu/6.824-golabs-2021 (push)
```

2. 设置upstream repo为官方repo
```
# fxrc @ popos in ~/Projects/6.824-2021 on git:master x [0:07:28] 
$ git remote add upstream git://g.csail.mit.edu/6.824-golabs-2021    
```

3. pull upstream的最新代码
```
# fxrc @ popos in ~/Projects/6.824-2021 on git:master x [0:08:24] C:1
$ git pull upstream master
From git://g.csail.mit.edu/6.824-golabs-2021
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> upstream/master
Already up to date.
```

4. 设置origin repo为我的repo
```
# fxrc @ popos in ~/Projects/6.824-2021 on git:master x [0:08:27]
$ git remote add origin git@github.com:fxrcode/6.824-2021.git
fatal: remote origin already exists.
(base)
# fxrc @ popos in ~/Projects/6.824-2021 on git:master x [0:09:09] C:128
$ git remote set-url origin git@github.com:fxrcode/6.824-2021.git
(base)
# fxrc @ popos in ~/Projects/6.824-2021 on git:master x [0:09:28]
$ git remote -v
origin  git@github.com:fxrcode/6.824-2021.git (fetch)
origin  git@github.com:fxrcode/6.824-2021.git (push)
upstream        git://g.csail.mit.edu/6.824-golabs-2021 (fetch)
upstream        git://g.csail.mit.edu/6.824-golabs-2021 (push)
(base)
```


4. 将从源头仓库更新后的代码推送到你自己的github仓库
```
# fxrc @ popos in ~/Projects/6.824-2021 on git:master x [0:09:32]
$ git branch -M main
(base)
# fxrc @ popos in ~/Projects/6.824-2021 on git:main x [0:09:38]
$ git push -u origin main
Enumerating objects: 148, done.
Counting objects: 100% (148/148), done.
Delta compression using up to 4 threads
Compressing objects: 100% (110/110), done.
Writing objects: 100% (148/148), 1.26 MiB | 39.24 MiB/s, done.
Total 148 (delta 51), reused 112 (delta 33)
remote: Resolving deltas: 100% (51/51), done.
To github.com:fxrcode/6.824-2021.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```