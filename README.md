# Notes Helps

针对学习和工作中使用 $\LaTeX$ 与`Markdown`的使用帮助清单，已在`Linux(Ubuntu 22.04)`、`Linux(Wsl-Ubuntu 22.04)`、`Windows 11`实现部署与验证。

## Latex

$\LaTeX$ 是一个文档准备系统 (Document Preparing System)，它非常适用于生成高印刷质量的科技类和数学类文档。它也能够生成所有其他种类的文档，小到简单的信件，大到完整的书籍。 $\LaTeX$ 使用 $\TeX$ 作为它的排版引擎，学习 $\LaTeX$ 是一个漫长而痛苦的过程，我们应该充分利用已知的资料，来尽量完成我们的需求。

本仓库使用的 $\TeX$ 版本：

```shell
TeX 3.141592653 (TeX Live 2022/dev/Debian)
kpathsea version 6.3.4/dev
Copyright 2021 D.E. Knuth.
```

### 安装

安装方法：参照[TeX Live](https://tug.org/texlive/) 中选择对应`OS`的安装方法即可，下面给出`Linux(Ubuntu)`中的安装方法。

`Linux(Ubuntu)`安装方法（建议）：

```shell
sudo apt update
sudo apt upgrade
sudo apt install texlive-full
```

### 基础教程

本仓库不提供具体教程，新手可以阅读 [Ishort-zh-cn](https://mirror-hk.koddos.net/CTAN/info/lshort/chinese/lshort-zh-cn.pdf) 入门，这几乎是最好的入门教程。

### 字体设置

由于 $\LaTeX$ 默认只有英文输出，因此对于国内 $\LaTeX$ 新手而言，如何输出中文是第一大坑。

#### 英文字体

英文字体的简单自定义可以使用如下代码：

```tex
\setmainfont{Times New Roman} % 设置主字体为新罗马体
```

#### 中文字体

目前，$\LaTeX$ 主流中文文档类支持是通过`ctex`宏包，使用`xelatex + ctex`编译方案，其中底层宏包为`xeCJK`。

![img](./assets/v2-e4cf970e43c99612d27491fe9fe7b2d2_720w.png)

上图可以看出，在`Linux`平台中`ctex`默认字体为`Fandol`，而`Windows`平台默认字体为**中易字库与微软雅黑**。

而诸如`Unubtu`等发行版并不自带`Fandol`字库，本仓库已上传至[Fonts](https://github.com/3000ye/Notes-tools/tree/main/Fonts)。或者访问[作者网页](https://www.ctan.org/pkg/fandol)获取。

#### 字体使用

如果使用`ctex`默认字体，则只需在导言区加入如下代码：

```tex
% 字体设置
\usepackage[UTF8]{ctex}
\usepackage{fontspec} % 设置字体
```



## Markdown







