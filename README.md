# 使用安装教程

## 安装

### 文本的编辑

编辑器：任意

书写方式：markdown

文本保存格式：.md 文件

### 文本的呈现（将方便书写的 ”.md” 文件自动转换为更方便阅读的 ”.rtf” 文件）

工具：Pandoc

下载地址：<https://github.com/jgm/pandoc/releases/tag/2.2.1>

iOS 系统点击 “……-macOS.pkg” 下载后安装

### Latex—MacTex

iOS 下载地址：<http://www.tug.org/mactex/>

To download, click MacTeX Download. 

文件约3GB 下载后安装

### 操作 (Terminal，Git)

尝试在 Terminal 输入 git help 回车

如果显示找不到 git 命令就在以下地址下载安装 git

<https://git-scm.com/download/mac>

## 使用

git clone https://github.com/juzikong/You-Plus.git

cd You-Plus/

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
