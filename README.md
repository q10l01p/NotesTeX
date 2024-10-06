<h1 align="center"><i>NotesTeX</i></h1>

<p align="center">
    <b>为学生设计的全能 LaTeX 笔记包。</b>
    <br>
    <i>NotesTeX</i> 是对原始 Jhep 期刊格式的修改，<br> 以满足大学生的需求。
    <br>
    <br>
    &middot;
    <b>NotesTeX v3.0</b>
    &middot;
    <br>
    &middot; 
     <a href="https://ctan.org/pkg/notestex"><strong>CTAN &raquo;</strong></a>
    &middot;
  </p>

## 目录

- [更新](#update)
- [预览](#preview)
- [安装](#installation)
- [使用](#usage)
- [文档](#documentation)
- [许可证](#license)
- [版本和联系信息](#version-and-contact)

## 更新 (v3.0)

**2021年10月23日**

1. 样式更新；修复了错误
2. 修复了边注、旁注与几何包之间的浮动问题
3. 为 AMSThm 环境集成了左栏
4. 移除了已弃用的字体和快捷方式

## 预览

|                    ```Jhep``` 格式化                     |                      目录                       |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| [![预览](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample0.png)](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample0.pdf) | [![预览](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample1.png)](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample1.pdf) |

|                         边注                         |                   ```amsthm``` 集成                   |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| [![预览](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample2.png)](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample2.pdf) | [![预览](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample3.png)](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample3.pdf) |

|                      图片集成                       |                  新的 ```part``` 格式化                   |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| [![预览](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample4.png)](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample4.pdf) | [![预览](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample5.png)](https://raw.githubusercontent.com/adhumunt/NotesTeX/master/Sample/Sample5.pdf) |

## 安装

安装只需要以下步骤：

1. **下载** [zip 压缩包](NotesTeXV3.zip)。
2. **编译** NotesTeX.tex 文件。编译应无问题，结果应与下方附带的 PDF 一致。
3. **移动** NotesTeXV3.sty 文件到你需要的地方，并让你的新笔记文件按照下面的示例调用它。

## 使用

以下是一个测试页面的示例：

```latex
\documentclass[10pt]{article}
\usepackage{/Path/to/package/NotesTeX} %应将 /Path/to/package 替换为包的实际路径
\usepackage{lipsum}

\title{{\Huge 测试页面标题}\\{\Large{测试页面副标题}}}
\author{作者姓名\footnote{\href{https://google.com/}{\textit{作者网站}}}}

\affiliation{作者单位}
\emailAdd{作者邮箱}
\begin{document}
  \maketitle
  \flushbottom
  \newpage
  \pagestyle{fancynotes}
  \part{测试部分 1}
  \lipsum[1]
  \section{子测试章节 1}
  这里有一些笔记。\sn{还有一些附加的旁注}
\end{document}
```

对于从右到左书写的语言，请在开始文档之前添加以下包和你的本地字体。下面是一个使用 [波斯语字体](https://fontlibrary.org/en/font/xb-niloofar) 的最小工作示例（MWE）。

```latex
\usepackage{xepersian}
\settextfont{XB Niloofar}
\setlatintextfont{Times New Roman}

\begin{document}
 ...
```

## 文档

该包的所有文档都在 [NotesTeXV3.pdf](NotesTeXV3/NotesTeX.pdf) 中，如果你有任何问题，请随时联系我。

## 许可证

此材料受 [LaTeX 项目公共许可证](LICENSE) 约束。

## 版本和联系信息

> NotesTeX v3.0.  
> 由 Aditya Dhumuntarao 创建。  
> 日期：2021年10月23日。  
> 如有意见和建议，请发送邮件至 adhumunt@gmail.com。