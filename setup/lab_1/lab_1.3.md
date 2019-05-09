### 实验二：

安装Git(仅供课下练习使用，课上只需从配置用户名和邮箱开始执行)

* Ubuntu安装

  ```
  sudo apt-get install git
  ```
* Windows安装https://git-scm.com/downloads

  ```
  https://git-scm.com/downloads
  ```

  

安装完成后，在开始菜单里找到“Git”->“Git Bash”，跳出一个类似命令行窗口的东西，就说明Git安装成功！
从这里开始输入你的命令
先打开一个GIt镜像

![pic4](https://github.com/tianyichow/DaSE_lab/raw/master/setup/pic/pic4.png)

1. 配置用户名和邮箱先
```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```
_小提示：use.name和“Your Name”之间有空格，Email同上。请把引号里的名字和邮箱替换成自己的_

2. 创建仓库（Repository）

	* 建立待上传python文件```vi test.py```

	* 在python文件中输入实验一的代码，先按住```"shift"+":"```退出编辑格式，然后在输入```"wq"```保存文件,按Enter退出。

	* 查看文件是否内容是否一致
```cat test.py```
	* 初始化仓库
```git init```

3. 将文件添加到本地仓库
 	* 把文件添加到本地仓库，输入命令：
```git add test.py```

 	* 确认提交，输入命令：
```git commit -m "written test.py"```

	_注释：-m命令后面表示本次提交的说明信息，可以任意指定，但一般是有意义的信息。_

4. 将本地仓库文件同步到Github
	* 在Github创建账号，网址：https://github.com, 在右上角找到“Create a new repo”按钮，创建一个新的仓库：
![pic4](https://github.com/tianyichow/DaSE_lab/raw/master/setup/pic/pic5.png)
在Repository name填入GitRepo，其他保持默认设置，点击“Create repository”按钮，就成功地创建了一个新的Git仓库。
	* 在本地GitRepo下运行命令，将本地和GitHub关联;
```git remote add origin https://github.com/github账户名/GitRepo```

	* 上传本地项目到GitHub;```git push -u origin master```
	
	_注释：-u,不仅把本地master分支上传到GitHub，还把本地和GitHub的master关联起来，以后不需要再加。origin是指向GitHub仓库的一个指针。过程中会提示输入账号和密码，输入注册时的账号和密码即可。_
	
	* 推送成功后在GitHub刷新即可看到本地上传文件;
	* 本地后续更新再上传只要输入
```git push origin master```

