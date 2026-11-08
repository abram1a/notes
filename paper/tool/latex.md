# latex

优势：

排版和内容区分开来，类似HTML与CSS的关系。

使用：

​	不适用与排版要求不怎么高的没必要使用。



## 格式

```tex
\命令名{参数}
\documentclass[utf8]{artical}
```

documentclass代表文件类型，参数artical代表普通的文章，还有book，report，beamer（幻灯片），cetart支持中文英文混写。

UTF8代表编码类型，默认编码也是UTF8

```tex
\begin{document}
```

所有位于这个命令之前的都被成为前言（preamble)

```tex
\end{document}
```

介于这两个命令之间的叫做正文（body）



## 在前言中

```tex
\title{文章的标题}
```

```tex
\author{abram}
```

```tex
\data{日期}
```

分别用来设置标题和作者名，文章的修改日期，可以在参数里使用

/today命令，自动生成当天的日期。

```tex
\usepackage{graphicx}
```

使用图片要在前言引用这个包

## 在正文中

```tex
\maketitle
```

显示前言的信息

```tex
\textbf{}
```

加粗文字,加粗的为参数

```tex
\textit{}
```

斜体

```tex
\underline
```

下划线

换行需要两个换行符

```tex
\section{}
```

开启一个新的章节

```tex
\subsection{}
```

子章节下的内容

```tex
\subsubsection
```

三级章节

```tex
\includegraphics[width=0.5\textwidth]{文件名}
```

\textwidth当前文本区域的宽度

如果要添加标题

```tex
\begin{figure}
\centering
\includegraphics[width=0.5\textwidth]{head}
\caption{标题名}
\end{figure}
```

必须将它包起来，然后使用\caption命令

\centering命令居中显示

> 这个\begin{}...\end{}称为**环境**

同一个环境共享文字格式

### 列表

```tex
\begin{itemize}
\item 列表项1
\item 列表项2
\end{itemize}
```

这个环境名还真不是随便起的

带数字列表

```tex
\begin{enumerate}
\itme 列表项1
\end{enumerate}
```

###　公式

```tex
$...$
```

如果喜欢写在单独的一行

```tex
\begin{equation}
公式
\end{equation}
```

简化版本

```tex
\[
公式
\]
```



[在线公式编辑器](https://latex.codecogs.com/eqneditor/editor.php)

### 表格

```tex
\begin{table}
\center
\begin{tabular}{|p{2cm}| c| c|}
\hline
单元格&单元格&单元格\\
\hline
\end{tabular}
\caption{}
\end{table}
```

c:centering,表示居中对其

l左对齐

r右对齐

|||表示为表格添加竖直方向的边框

\hline表示添加水平方向的边框

\hline\hline表示添加双横线

三个c代表三列

p{长度}表示数据的列宽

p意思是paragraph

加标题:

加环境，加caption，加centering

##　深化

［good](https://github.com/CTeX-org/lshort-zh-cn)

