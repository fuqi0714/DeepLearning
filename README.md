# DeepLearning

深度学习的学习笔记库

# 准备

Github账户(将用户名发给我)

下载GitHub Desktop或Git GUI对仓库进行代码管理

# 参与人员

目前内容包括研一同学推送学习文档笔记和实践测试

# 要求

此仓库不定期更新，为确保推送拉取操作不产生冲突，在上传学习笔记前先执行```git pull``` 获取***当前分支***在远程仓库更新后的状态

使用git指令拉取本仓库后，切换到属于自己的分支，根据[实际使用情况进行对应的操作](#git控制仓库的工具和部分指令)

常规操作指令

	添加修改后的文件 git add .									
	批注此次修改更新的信息 git commit -a "   "							
	将此次更新推送到远程仓库 git push									



## 学习书籍

[书籍链接](https://github.com/XiangLinPro/IT_book)

解压密码x20200427


## 学习任务

任务文档格式

推荐学习使用[markdown格式](https://www.markdownguide.org/basic-syntax)编辑长文本，也是常见的开源程序中readme文档的书写格式

任务内容

该仓库的[projects](https://github.com/orgs/HuiGulab/projects/2)更新学习任务信息并按照要求执行，并且指定参与成员。[issues](https://github.com/HuiGulab/DeepLearning/issues)板块同步说明




## 文件夹结构

先通过git拉取仓库，之后执行创建个人分支的操作，在[创建的新分支](https://github.com/HuiGulab/DeepLearning#git%E6%8E%A7%E5%88%B6%E4%BB%93%E5%BA%93%E7%9A%84%E5%B7%A5%E5%85%B7%E5%92%8C%E9%83%A8%E5%88%86%E6%8C%87%E4%BB%A4)内文件夹结构如下。括号内的中文字符仅做说明示例，可省略

例

	├── git
	├── GuoxuSheng
		├── DiveIntoDeepLearning(深度学习电子书)
			├── Chapter2
				├── 2预备知识.ipynb
			├── Chapter3
				├── 3线性神经网络.ipynb
				······
			├── Chapter15
				├── 15自然语言处理.ipynb
		├── DL&ML(天池实践测试)
		├── Task(学习任务文件)
			├── Task001-关于mediapipe卡尔曼滤波算法的问题
				├── 关于mediapipe卡尔曼滤波算法的问题.md(解答类问题可直接在源文件上作答)
				├── Ans
					├── CodeFiles(相关的代码文件)
					├── OtherFiles(其他文件，例如readme文件中插入的说明图片或其他)
					

# 开发工具
## Git控制仓库的工具和部分指令

[相关说明文档](https://docs.github.com/cn)

### GitHub Desktop

可通过点击```current branch```的下拉菜单切换分支

### Git Bash

查看所有分支```git branch -a```并根据显示的remote/origin/姓名，新建本地分支并同步远程分支。例如```git checkout -b GuoxuSheng origin/GuoxuSheng```即可

如从main分支切换到其他分支时遇到```error: Your local changes to the following files would be overwritten by checkout:```，依次执行

	git add .
	git commit -a "commit message"

将main分支修改的文件暂存到缓存区，即可正常切换分支

## 常用开发工具

了解以下开发工具，并根据实际情况熟练掌握一类
### Conda
其特点在于可创建多个不同版本的python环境实现互相独立的多环境管理；缺点在于多个虚拟环境的创建将占用大量硬盘空间，并且当涉及其他需要额外进行编译操作的程序时，操作处理起来略微繁琐
- [Anaconda](https://www.anaconda.com/)/[Minconda](https://docs.conda.io/en/latest/miniconda.html)，作用类似，前者相比后者集成了其他开发工具和可视化界面的操作；后者仅包括精简的命令行窗口功能
	- [英文文档](https://docs.conda.io/projects/conda/en/latest/user-guide/index.html)/[中文文档](https://anaconda.org.cn/anaconda/user-guide/getting-started/)
- 包含git代码管理功能

Conda移植虚拟环境到其他设备的[操作方法](https://blog.csdn.net/buweifeng/article/details/124733123?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_baidulandingword~default-1-124733123-blog-115385868.t0_layer_searchtargeting_sa&spm=1001.2101.3001.4242.2&utm_relevant_index=3)

	#安装打包资源库
	conda install -c conda-forge conda-pack
	#当前虚拟环境导出包
	conda pack -n anaconda3
	#登陆需要安装环境的机器
	cd yourpath
	# 解压
	tar zxf target_file.tar.gz
	# 激活环境
	conda activate /yourpath/bin/activate 
	# 查看python的路径
	which python


### Pycharm
常用的Python语言IDE
- [说明文档](https://pycharm.iswbm.com/)
- 包含git代码管理功能
### Visual Studio
微软IDE
- 包含git代码管理功能

### Google Colab

[谷歌云平台](https://zhuanlan.zhihu.com/p/386162610)，linux操作环境。适用于学习阶段电脑性能不佳时的替代选择

