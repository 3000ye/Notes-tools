# Latex

## 写在前面的话

Latex 是一个文档准备系统 (Document Preparing System)，它非常适用于生成高印刷质量的科技类和数学类文档。它也能够生成所有其他种类的文档，小到简单的信件，大到完整的书籍。 Latex 使用 tex 作为它的排版引擎。

学习 Latex 是一个漫长而痛苦的过程，我们应该充分利用已知的资料，来尽量完成我们的需求。

一些好的学习资料：

1. [lshort-zh-cn 文档](http://mirrors.ctan.org/info/lshort/chinese/lshort-zh-cn.pdf)
2. [Latex工作室](https://www.latexstudio.net/)
3. [CSDN帖子](https://blog.csdn.net/ye3000ye/article/details/119918658?spm=1001.2014.3001.5501)

# 模板

本模板编译时需要选择：`xelatex`编译模式。

## 基础设置

### 页面设置

```latex
\documentclass[12pt, a4paper]{article} % 字号：12，纸张：A4
\usepackage[top=2.54cm, bottom=2.54cm, left=3.18cm,right=3.18cm]{geometry} % 页边距设置
```

### 字体设置

由于latex在不同平台上的默认字体配置不同，所以为了统一字体配置，我们需要在加载宏包时指定`fontset=none`，然后自定义中文和英文字体。

```latex
\usepackage[UTF8, fontset=none]{ctex}
\usepackage{fontspec}  % 设置字体
\setCJKmainfont{SimSun}[AutoFakeBold=true, BoldFont={SimHei}, ItalicFont={KaiTi}]  % 正文字体
\setCJKsansfont[AutoFakeBold=3]{KaiTi} % 无衬线字体
\setCJKmonofont[AutoFakeBold=3]{SimHei} % 等宽字体
\setmainfont{Times New Roman} % 设置主字体为新罗马体
```

### 文本设置

```latex
\usepackage{enumerate} % 支持小标题编号
\linespread{1.5} % 行间距1.5倍
\usepackage{indentfirst}%首段缩进
\setlength{\parindent}{2em} % 首行缩进两字符
\usepackage[hidelinks]{hyperref} % 目录添加超链接
```

### 数学支持

```latex
\usepackage{amsmath} % 数学公式支持
\usepackage{amssymb} % 数学符号支持
\usepackage{bm} % 公式加粗
\usepackage{mathrsfs} % 花体字母
```

### 图片设置

```latex
\usepackage{caption} % 插入图片标题
\usepackage{float} % 控制图片位置
\usepackage{subfigure} % 图片并排
\usepackage{booktabs} % 插入表格
```

### 表格设置

```latex
\usepackage{multirow} % 表格自动换行
\usepackage{bigstrut} % 表格设置
\usepackage{rotating} % 表格设置
\usepackage{tabularx} % 表格设置
```

## 中文论文特殊设置

```latex
\renewcommand{\figurename}{图} % 将图片序号改为图
%\renewcommand{\thefigure}{\thesection.\arabic{figure}} % 将图片序号和章节链接起来
\renewcommand{\tablename}{表} % 将表格序号改为表
%\renewcommand{\thetable}{\thesection.\arabic{table}} % 将表格序号和章节链接起来
\renewcommand\thesection{\zhnum{section}} % 将章节的编号改为中文编号
\renewcommand \thesubsection {\arabic{section}.\arabic{subsection}} % 将子章节编号同步
\renewcommand{\refname}{参考文献} % 将参考文献改为中文
\renewcommand{\contentsname}{目录} % 将目录改为中文
\renewcommand{\abstractname}{摘要} % 将摘要改为中文
```
## 数学环境设置
```latex
\newtheorem{example}{例}             % 整体编号
\newtheorem{algorithm}{算法}
\newtheorem{theorem}{定理}[section]  % 按 section 编号
\newtheorem{definition}{定义}
\newtheorem{axiom}{公理}
\newtheorem{property}{性质}
\newtheorem{proposition}{命题}
\newtheorem{lemma}{引理}
\newtheorem{corollary}{推论}
\newtheorem{remark}{注解}
\newtheorem{condition}{条件}
\newtheorem{conclusion}{结论}
\newtheorem{assumption}{假设}
```

## 完整模板

```latex
% 页面设置
\documentclass[12pt, a4paper]{article} % 字号：12，纸张：A4
\usepackage[top=2.54cm, bottom=2.54cm, left=3.18cm,right=3.18cm]{geometry} % 页边距设置
% 字体设置
\usepackage[UTF8, fontset=none]{ctex}
\usepackage{fontspec}  % 设置字体
\setCJKmainfont{SimSun}[AutoFakeBold=true, BoldFont={SimHei}, ItalicFont={KaiTi}]  % 正文字体
\setCJKsansfont[AutoFakeBold=3]{KaiTi} % 无衬线字体
\setCJKmonofont[AutoFakeBold=3]{SimHei} % 等宽字体
\setmainfont{Times New Roman} % 设置主字体为新罗马体
% 文本设置
\usepackage{enumerate} % 支持小标题编号
\linespread{1.5} % 行间距1.5倍
\usepackage{indentfirst}%首段缩进
\setlength{\parindent}{2em} % 首行缩进两字符
\usepackage[hidelinks]{hyperref} % 目录添加超链接
\usepackage{zhnumber} % 章节标题中文显示
% 数学支持
\usepackage{amsmath} % 数学公式支持
\usepackage{amssymb} % 数学符号支持
\usepackage{bm} % 公式加粗
\usepackage{mathrsfs} % 花体字母
% 图片设置
\usepackage{caption} % 插入图片标题
\usepackage{float} % 控制图片位置
\usepackage{subfigure} % 图片并排
\usepackage{booktabs} % 插入表格
% 表格设置
\usepackage{multirow} % 表格自动换行
\usepackage{bigstrut} % 表格设置
\usepackage{rotating} % 表格设置
\usepackage{tabularx} % 表格设置

\title{XXXX} % 文章标题
\author{XXXX} % 文章作者
\date{XXXX} % 文章时间

\begin{document} % 文档从这里开始。
\maketitle % 按照预定的模板把上面那些信息排好。
\renewcommand{\figurename}{图} % 将图片序号改为图
%\renewcommand{\thefigure}{\thesection.\arabic{figure}} % 将图片序号和章节链接起来
\renewcommand{\tablename}{表} % 将表格序号改为表
%\renewcommand{\thetable}{\thesection.\arabic{table}} % 将表格序号和章节链接起来
\renewcommand\thesection{\zhnum{section}} % 将章节的编号改为中文编号
\renewcommand \thesubsection {\arabic{section}.\arabic{subsection}} % 将子章节编号同步
\renewcommand{\refname}{参考文献} % 将参考文献改为中文
\renewcommand{\contentsname}{目录} % 将目录改为中文
\renewcommand{\abstractname}{摘要} % 将摘要改为中文
\newtheorem{example}{例}             % 整体编号
\newtheorem{algorithm}{算法}
\newtheorem{theorem}{定理}[section]  % 按 section 编号
\newtheorem{definition}{定义}
\newtheorem{axiom}{公理}
\newtheorem{property}{性质}
\newtheorem{proposition}{命题}
\newtheorem{lemma}{引理}
\newtheorem{corollary}{推论}
\newtheorem{remark}{注解}
\newtheorem{condition}{条件}
\newtheorem{conclusion}{结论}
\newtheorem{assumption}{假设}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% 文章内容从此开始
\section{一级标题}

\subsection{二级标题}

\subsubsection{三级标题}
\subsubsection{三级标题}

\subsection{二级标题}

\subsubsection{三级标题}
\subsubsection{三级标题}


\section{一级标题}

\subsection{二级标题}

\subsubsection{三级标题}
\subsubsection{三级标题}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\end{document}
```

## 特殊模板

### 标题居中

```latex
{\centering\section{标题}}
```

### 无序列表

```latex
\begin{itemize}
  \item 无序列表1
  \item 无序列表2
  \item 无序列表3
\end{itemize}
```

### 有序列表

```latex
\begin{enumerate}[\hspace{2em} i.]
  \item 有序列表1
  \item 有序列表2
  \item 有序列表3
\end{enumerate}
```

### 数学公式

```latex
\begin{equation}\label{公式索引}
  公式
\end{equation}
```

### 表格模板

#### 单个表格
Latex中表格的输入非常麻烦，我们借助一个工具来完成：[ivankokan/Excel2LaTeX: The Excel add-in for creating LaTeX tables (github.com)](https://github.com/ivankokan/Excel2LaTeX)

在生成完表格后，记得手动修改为三线表格式。

#### 多表并排

其中表格的浮动格式可以设置：`c`，`t`，`b`
```latex
\begin{minipage}[c]{0.5\textwidth}
\centering
表格1
\end{minipage}
\begin{minipage}[c]{0.5\textwidth}
\centering
表格2
\end{minipage}
```

### 图片模板

在插入图片之前，需要知道图片的存储路径，一般建议在`*.tex*`文件目录下新建一个`fig`文件夹来存储图片。

#### 一张图片

```latex
\begin{figure}[H]
  \centering
  \includegraphics[width=0.8\textwidth]{图片路径}
  \caption{图片标题}
  \label{图片索引}
\end{figure}
```

#### 两张图片

```latex
\begin{figure}[H]
  \centering
  \begin{minipage}[c]{0.40\textwidth} %minipage使之保持同一行，0.2占这行的0.2
  \centering
  \includegraphics[width=170pt]{图片1路径}\\
  \caption{图片1标题}
  \end{minipage}
  \hspace{1cm}
  \begin{minipage}[c]{0.40\textwidth} %minipage使之保持同一行，0.2占这行的0.2
  \centering
  \includegraphics[width=170pt]{图片2路径}\\
  \caption{图片2标题}
  \end{minipage}
\end{figure}
```

### 参考文献

```latex
\begin{thebibliography}{文献数量}

\bibitem{RN1}文献1

\bibitem{RN2}文献2

\end{thebibliography}
```

### 超链接

#### 网页超链接

```latex
\href{网址}{显示文字}
```

#### 文章内部超链接

图片、表格、公式索引

```latex
\ref{索引}
```

参考文献索引：

```latex
\textsuperscript{\cite{参考文献序号}}
```