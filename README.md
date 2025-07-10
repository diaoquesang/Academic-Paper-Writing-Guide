# 💯 英文学术论文写作指南

> 注：本指南仅针对LaTex写作

## 如何在文中插入代码

一般而言，我们需要用到```hyperref```宏包来实现链接跳转

首先，在```\begin{document}```前加入```\usepackage{hyperref}```

其次，我们通常会在摘要的末尾加入代码链接

```
Our code is available at \href{跳转目标}{显示目标}.
```

即Our code is available at [显示目标](跳转目标).

一般而言，我们会将显示目标和跳转目标都设置为我们的代码链接

```
Our code is available at \href{跳转目标}{显示目标}.
```

即Our code is available at [显示目标](跳转目标).
