### Git常用命令

```git
mkdir git_demo 	新建文件夹
cd git_demo 	进入文件夹
pwd 			查看当前所在文件夹目录
ls				查看文件
ls -al			查看详细文件（包含git隐藏文件）
git init		初始化所在文件夹为git仓库
```

```git
全局配置 用户名 邮箱 还有local system
全局配置后 其他新建文件夹不用再配置了
git config --global user.name "wzd"	
git config --global user.email "839935667@qq.com" 	

查看配置
git config --global --list
```

```git
git status				查看 git 仓库当前状态
git add git_demo.html	添加新建和修改的文件
git add .				添加所有新建和修改的文件
git commit -m "web 1.0"	提交并添加描述
git log					查看 git 提交记录
```



### GitHub提交流程

头像旁边的 + 可以创建新仓库 New repository

填写仓库名称，其他均可默认

```git
git remote add origin git@github.com:hellowzd/git_demo.git 给本地仓库添加远程仓库
git remote		返回远程仓库的名称 origin 即成功

ssh-keygen -t rsa -C "839935667@qq.com"
回车
回车默认即可

切换到提示的 key 路径
cd /c/Users/wzd/.ssh

ls					// 显示两个文件 id_rsa（私钥） id_rsa.pub（公钥）
cat id_rsa.pub		// 打开公钥文件，复制
```

点击头像 进入 Settings

左边选项 进入SSH and GPG keys

点击 New SSH key 进入创建

Title 可以省略 将私钥 粘贴到 Key 栏内即可

点击 Add SSH key 创建

```git
测试本地 git 和 github 是否连接成功
ssh -T git@github.com

切换回 git 仓库
cd /c/Users/wzd/git_demo/

推送到 github
git push -u origin master

```

