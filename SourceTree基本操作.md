# SourceTree的基本操作
## 1. 克隆仓库
可以选择浏览本地仓库或者通过登录远程账号来访问远程仓库，也可以直接选择克隆（clone），在“源路径/URL”中输入远程仓库地址，“目标路径”中填写要克隆到的本地仓库路径、名称，点击“克隆”将远程仓库克隆到本地。

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/898dcaec6c3cdc90e21b6f4d08c6b123.png)

## 2. 创建分支
如果本地只有一个master分支，建议可以开一个develop分支用于开发，先在左边栏选择到master分支，再点击上方的分支，

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/878807a3f00910c9f316abcad748c53d.png)

在出来的分支页面中填写新分支的名称“develop”，点击“创建分支”，即可在现有master分支的基础上开出一个新的develop分支用于开发。

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/934212aabacfd15a5a8e7198aec4e1e1.png)

## 3. 提交
在左边栏的“分支”选项下，双击“develop”切换到develop分支，点击右上角的“资源管理器”可以方便地打开本地仓库。

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/93aca39096a1f85730f963654948ee6e.png)

在做完项目后，可以在下方看到文件变动，点击左上角的“提交”即可来到提交界面，

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/7d01a88e565c26477032578dd142f96a.png)

在提交界面中，下方可以看到文件变动，可以点击对应文件右边的“+”号来将文件提交到“已暂存文件”区，也可以通过点击“暂存所有”将所有改动的文件添加到“已暂存文件”区。

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/ac4ab6e513abd0f0246346f87ea08a90.png)

最后在下方输入栏输入所作出的改动，点击“提交”即可将改动添加到本地仓库。

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/eeddcc70652949640bdb991b6b863113.png)

## 4. 合并分支
最后在develop分支中确认所有工作已完成后，双击左边栏“分支”下的“master”切换到master分支。现在有两种方法可以将develop分支合并到master分支，这边分别介绍。
* 第一种是点击上方的“合并”按钮，

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/28a6d6c3360c07d1046ca00e97baaf51.png)

在出现的合并界面中，选择最上方develop分支所作出的改动，点击右下方的确认，即可合并分支。

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/424d2d573e1569af487b206300951a9e.png)

* 第二种是在左边栏“develop”分支处右键，选择“合并develop至当前分支”，点击确定即可合并分支。

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/de3e679eb3173ee18117dae79761262e.png)

## 5. 拉取与推送
完成所有工作后，需要将本地仓库做所的改动推送到远程仓库。此时可以看到上方“推送”按钮上有数字出现，

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/8168d4b71f30d21c20b561efe3152846.png)

数字1代表将会推送一个改动，为了确保本地仓库与远程仓库的一致，建议先点击上方“推送”按钮左边的“拉取”，再次做一次同步，确保没有冲突后，再按推送按钮进行推送。点击“推送”即可完成推送。

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/6306c8be71317651e083f486600200fe.png)
