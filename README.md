# 使用安装教程

## 安装

### 文本的编辑

工具：任意编辑器

书写方式：markdown。本文本的书写方式就是markdown，参照模仿即可。

文本保存格式：.md 文件

本项目中的 .md 文件是基本编辑完成的文件，在该基础上修缮即可。

其中 metadata.yaml 与 chap1/2/3.md 文件是对 You-Plus.md 文件的拆分（You-Plus.md与前4个文件总和的内容相同），用于生成电子书格式。

### 文本的呈现（将方便书写的 ”.md” 文件自动转换为更方便阅读的 ”.rtf” 文件）

工具：Pandoc

下载地址：<https://github.com/jgm/pandoc/releases/tag/2.2.1>

iOS 系统点击 “……-macOS.pkg” 下载后安装

### PDF格式的编辑器（Latex—MacTex）

iOS 下载地址：<http://www.tug.org/mactex/>

To download, click MacTeX Download. 下载后安装

* **文件约3GB *推荐先下载安装本文件再学习其他部分***

### 保存与分享 (Git)

尝试在 Terminal 输入 git help 回车

如果显示找不到 git 命令就在以下地址下载安装 git

<https://git-scm.com/download/mac>

## 使用

### 首先在 Terminal 进入本地电脑的合适地址（cd命令），再通过以下命令下载本项目全部文件到该地址：

git clone https://github.com/juzikong/You-Plus.git

### 进入本项目文件夹：

cd You-Plus/

### 使用 pandoc 进行任意格式的转换：

* rtf:

pandoc You-Plus.md -s -o test.rtf

* Word文档：

pandoc You-Plus.md -s -o test.docx

* 电子书：

pandoc chap1.md chap2.md chap3.md metadata.yaml -s -o book.epub

* PDF：

pandoc You-Plus/You-Plus.md -o test.pdf -s --template=You-Plus/pm-template.latex --pdf-engine=xelatex -V mainfont='STHeiti'

* 如果 Latex 无中文尝试以下命令—

$sudo tlmgr install titling

$sudo tlmgr install lastpage
