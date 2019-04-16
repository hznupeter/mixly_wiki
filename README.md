# mixly wiki 

## Mixly wiki 编写准备
### 注册github账号
https://github.com/join?source=header-home
### 安装github同步软件github-desktop 
https://desktop.github.com/
### 安装文本编辑器sublime
http://www.sublimetext.com/
### 克隆项目到本地
* 打开github-desktop 软件，依次点击：File-Clone a Repository-URL，在URL中输入https://github.com/hznupeter/mixly_wiki.git
* 设置项目本地存储地址

![](images/clone_repo.png)

## 编写项目
* 打开github-desktop 软件，依次点击Repository-open in sublime Text,用sublime打开该项目进行编辑。
![](images/sublime.png)

## 项目目录说明
```
|--doc
   |--build  /*生成目录*/
      |--doctrees
      |--gettext
      |--html
   |--source /*源文件目录*/
      |--_static /*静态html文件目录*/
      |--_templates /*自定义模板目录*/
      |--arduino /*arduino部分wiki目录*/
         |--images /*arduino引用图片*/
            |--02  /*02.XXX.rst 文件引用的图片目录*/
               |-- analogRead.png /*所有图片都用png格式，文件命名格式为该函数名*/
               |-- analogRead-example.png /*模块使用范例截图*/
               |-- analogRead.en.png /*analogRead.png对应的英文图片*/
               |-- analogRead-example.en.png /*analogRead-example.png对应的英文图片*/
      |--basic /*软件基础部分wiki目录*/
      |--locale /*多语言目录*/
      |--MicroPython /*micropython部分wiki目录*/
      |--Python /*python部分wiki目录*/

```
以 arduino为例进行目录说明，arduino目录中包含多个rst文件，rst为wiki的核心文件，通过编辑该类文件创建wiki。

## arduino 语法参考
http://www.cnblogs.com/xczr/p/7832015.html

https://www.arduino.cc/reference/en/

## Sphinx语法说明

语法参考https://www.cnblogs.com/zzqcn/p/5096876.html#_label7


## 提交代码

修改文本后，按照下图操作提交代码。
![](images/commit.png)

## 本地预览
* 安装python3.x
* 打开cmd，输入以下命令，配置基础环境
```
pip install -U Sphinx
pip install sphinx_rtd_theme
pip install --upgrade recommonmark
```
* 跳转到本地项目路径，执行生成命令
```
cd Documents\GitHub\mixly_wiki\doc
make html
```
![](images/cmd.png)
* 打开build/html/index.html本地预览。

## 在线预览
在提交代码之后，浏览https://mixly-wiki-test.readthedocs.io/zh_CN/latest/
