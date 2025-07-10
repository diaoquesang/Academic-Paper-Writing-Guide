# 💯 Code-in-Paper-Guide 论文代码插入教程

<div align="center">
  

[![](https://img.shields.io/github/stars/diaoquesang/Code-in-Paper-Guide)](https://github.com/diaoquesang/Code-in-Paper-Guide)
[![](https://img.shields.io/github/forks/diaoquesang/Code-in-Paper-Guide)](https://github.com/diaoquesang/Code-in-Paper-Guide)
[![](https://img.shields.io/github/issues/diaoquesang/Code-in-Paper-Guide)](https://github.com/diaoquesang/Code-in-Paper-Guide/issues)
[![](https://img.shields.io/github/license/diaoquesang/Code-in-Paper-Guide)](https://github.com/diaoquesang/Code-in-Paper-Guide/blob/main/LICENSE) 
[![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fdiaoquesang%2FCode-in-Paper-Guide&label=visitors&countColor=%2337d67a&style=flat&labelStyle=none)](https://visitorbadge.io/status?path=https%3A%2F%2Fgithub.com%2Fdiaoquesang%2FCode-in-Paper-Guide)

</div>

> 注：本教程仅针对LaTex写作

## 🥸 使用```hyperref```宏包

一般而言，我们需要用到```hyperref```宏包来实现链接跳转

首先，在```\begin{document}```前加入```\usepackage{hyperref}```

其次，我们通常会在摘要的末尾加入代码链接

```
Our code is available at \href{跳转目标}{显示目标}.
```

即Our code is available at [显示目标](跳转目标).

一般而言，我们会将显示目标和跳转目标都设置为我们的代码链接

以本repo为例

```
Our code is available at \href{https://github.com/diaoquesang/Academic-Paper-Writing-Guide}{https://github.com/diaoquesang/Academic-Paper-Writing-Guide}.
```

即Our code is available at [https://github.com/diaoquesang/Academic-Paper-Writing-Guide](https://github.com/diaoquesang/Academic-Paper-Writing-Guide).

## 🚫 禁用```hyperref```宏包

特殊情况下，如[The 39th Annual AAAI Conference on Artificial Intelligence (AAAI 2025)](https://aaai.org/conference/aaai/aaai-25/)的模板中，```hyperref```宏包被禁用

```
% \usepackage{hyperref} -- This package is specifically forbidden
```

通常官方会给出替代方案，如AAAI 2025在模板中给出了

```
% Uncomment the following to link to your code, datasets, an extended version or similar.
% You must keep this block between (not within) the abstract and the main body of the paper.
% \begin{links}
%     \link{Code}{https://aaai.org/example/code}
%     \link{Datasets}{https://aaai.org/example/datasets}
%     \link{Extended version}{https://aaai.org/example/extended-version}
% \end{links}
```

以添加代码为例，我们只需在摘要```\end{abstract}```和正文```\section{xxx}```之间插入

```
\begin{links}
    \link{Code}{https://github.com/diaoquesang/Academic-Paper-Writing-Guide}
\end{links}
```

即可实现代码添加，显示为**Code** — https://github.com/diaoquesang/Academic-Paper-Writing-Guide

## 🎭 双盲？匿名！

对于双盲评审（Double Blind Review）论文的投稿，指向GitHub的代码链接可能被认为泄露身份信息而违反双盲原则，从而导致Desk Rejection

这种情况下，我们可以使用匿名GitHub链接来完成代码添加

我们通常使用[Anonymous GitHub](https://anonymous.4open.science/)来完成对GitHub repo的匿名化

![image](https://github.com/user-attachments/assets/1faa8d8b-fbb4-4dae-8f9c-649040f664a7)

首先，我们输入需要匿名的Github repo的链接，默认勾选```Auto update```以实现自动更新

随后，```commit```，即SHA，将会根据输入的链接自动生成

我们可以通过设置```Anonymize repository id```自定义我们的GitHub repo对应的匿名链接

此外，我们还可以通过设置```Terms to anonymize```来实现对内容的匿名化，不过这通常并不可靠，因为我们并不总能精准地列出所有可能和身份信息相关的词汇

更为可靠的是手动在GitHub repo中删除或匿名化身份信息，如```LICENSE```文件中通常会自动包含身份信息

```
Copyright (c) 2025 小帅
```

我们可以用XXX来代替

```
Copyright (c) 2025 XXX
```

为了方便，我们通常设置```Expiration strategy```为```Never expire```，即永不过期

构建完成后，我们可以通过访问[https://anonymous.4open.science/dashboard](https://anonymous.4open.science/dashboard)来查看所有已匿名化的repo

最后，我们在摘要的末尾加入匿名代码链接

```
Our code is available at \href{https://anonymous.4open.science/r/Academic-Paper-Writing-Guide}{https://anonymous.4open.science/r/Academic-Paper-Writing-Guide}.
```

即Our code is available at [https://anonymous.4open.science/r/Academic-Paper-Writing-Guide](https://anonymous.4open.science/r/Academic-Paper-Writing-Guide).

特殊情况不在此赘述


## 🥰 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=diaoquesang/Code-in-Paper-Guide&type=Date)](https://star-history.com/#diaoquesang/Code-in-Paper-Guide&Date)
