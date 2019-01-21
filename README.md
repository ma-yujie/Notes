# 欢迎使用 Cmd Markdown 编辑阅读器

------
[TOC]

```latex
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% 文件名 :     Homework-templete.tex       % %交作业时命名为：学号 姓名
%                                          %
% 课程:        专业外语                    %
%                                          %
% 单位:        西南大学数学与统计学院      %
%                                          %
% 创建于:      2018年9月6日                %
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\documentclass[11pt]{article}
%=======================Include  Packages=============================================%
\usepackage{array}
\usepackage{CJK}
\usepackage{slashbox}
\usepackage[centertags]{amsmath}
\usepackage{amsfonts}
\usepackage{amssymb}
\usepackage{amsthm}
\usepackage{booktabs,color}
\usepackage{epsfig}
\usepackage{fancyhdr}
\usepackage{listings}
\usepackage{xcolor}
\usepackage{hyperref}
\usepackage{mathrsfs}
\allowdisplaybreaks[4]
%=======================图形与表格的平行排列=========================================%
\makeatletter
\newcommand\figcaption{\def\@captype{figure}\caption}
\newcommand\tabcaption{\def\@captype{table}\caption}
\makeatother

%========================长宽的设计==================================================%
\textwidth=16cm \textheight=23cm \topmargin=-0.7in
\oddsidemargin=0.cm \baselineskip=7.0mm

% %%%%%%%%%%%%%%%%%%%style: list typesetting%%%%%%%%%%%%%%%%%%%
%=======================自定义命令==================================================%
%此处可以定义你需要的新命令
\newtheorem{exercise}{\textcolor[rgb]{1.00,0.00,0.00}{Exercise}\,}
\def\proof{{\bf \textcolor[rgb]{0.00,1.00,0.00}{Proof.}}\,}
\newtheorem{example}{\textcolor[rgb]{1.00,0.00,0.00}{Example}\,}
\newtheorem{lemma}{Lemma}
\def\P{\operatorname*{\mathbb{P}}}
\def\R{\operatorname*{\mathbb{R}}}
\def\E{\operatorname*{\mathbf{E}}}
\allowdisplaybreaks[4]
\usepackage{setspace}
\doublespacing
%=======================正文开始====================================================%
%前面设计不改变

\begin{document}
%=======================正文=======================================================%
\title{Homework(II)}%I代表第一次作业
\author{{ MaYujie \qquad 222017314210051}\\%填写姓名和学号
{\small School of Mathematics and Statistics, Southwest University}}
\date{}
\maketitle

%%==============作业===========================================
%===第1题
\begin{exercise}
If the events $ A_1,...,A_n $ are independent,so are the events $ A_1',...,A_n' $,where $ A_j'$ is either $ A_j or A_j^c $, j=1....n.
\end{exercise}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\noindent\begin{proof} %%==格式
 The proof is done by (a double) induction.\\
 For n=2,we have to show that $ P( A_1'A_2')=P(A_1')P(A_2') $.Indeed,let $ A_1'=A_1,A_2=A_2^c $ \\
 Then $ P( A_1'A_2')=P(A_1A_2^c)=P(A_1(S-A_2^c))=P(A_1-(A_1\cap A_2))=P(A_1)-P(A_1)P(A_2)=P(A_1)(1-P(A_2))=P(A_1)P(A_2^c)=P(A_1')P(A_2')$\\
 Similarly if $A_1'=A_1^c,A_2'=A_2$ ,and the same as above, $ P( A_1'A_2')=P(A_1')P(A_2') $\\
 Next,assume the assertion to be true for k events and show it to be true for k+1 events .That is,we suppose that $P(A_1'\cap ...\cap A_k')=P(A_1')...P(A_k')$,and we shall show that $P(A_1'\cap...\cap A_{k+1}')=P(A_1')...P(A_{k+1}')$.First assume that $A_{k+1}'=A_{k+1}$,and we have to show that
 \begin{eqnarray*}
 P(A_1'\cap...\cap A_{k+1}')=P(A_1'\cap...\cap A_k\cap A_{k+1})=P(A_1')...P(A_k')P(A_{k+1})
 \end{eqnarray*}
 This relationship is established also by induction as follows:If $A_1'=A_1^c$ and $A_i'=A_i,i=2,...,k$,then\\
 $P(A_1^c\cap A_2\cap ...\cap A_k\cap A_{k+1})=P[(S-A_1)\cap A_2\cap ...\cap A_k\cap A_{k+1}]\\
 =P( A_2\cap ...\cap A_k\cap A_{k+1}-A_1\cap A_2\cap ...\cap A_k\cap A_{k+1})\\
 =P( A_2\cap ...\cap A_k\cap A_{k+1})-P （A_1\cap A_2\cap ...\cap A_k\cap A_{k+1})\\
 =P(A_2)...P(A_k)P(A_{k+1})-P(A_1)P(A_2)...P(A_k)P(A_{k+1})\\
 =P(A_2)...P(A_k)P(A_{k+1})[1-P(A_1)]=P(A_1^c)P(A_2)...P(A_k)P(A_{k+1})$\\
 This is,clearly,true if $A_1^c$ is replace by any other $A_i^c,i=2,...,k $.Now,for l<k,assume that \\
 $P(A_1^c\cap...\cap A_l^c\cap A_{l+1}\cap...\cap A_{k+1})=P(A_1^c)...(A_l^c) P(A_{l+1})...P(A_{k+1})$\\
 and we need show that\\
 $P(A_1^c\cap...\cap A_l^c\cap A_{l+1}^c\cap A_{l+2}\cap...\cap A_{k+1})=P(A_1^c)...P(A_l^c)P(A_{l+1}^c)P( A_{l+2})... P(A_{k+1})$


\end{proof}%%==格式
\qed

%===============================
%===第2题
\begin{exercise}
P is subaddiitive;that is,$P(\bigcup_{i=1}^\infty A_i)$ $\leq \sum_{i=1}^\infty P(A_i) $ and also $P(\bigcup_{i=1}^n A_i)$ $\leq \sum_{i=1}^n P(A_i) $
\end{exercise}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\noindent\begin{proof}\\
when k=2,
\begin{eqnarray*}
P(A_1\bigcup A_2)\leq P(A_1)+P(A_2)
\end{eqnarray*}
Suppose k=n-1 time of establishment:
\begin{eqnarray*}
P(\bigcup_{i=1}^{n-1} A_i) \leq \sum_{i=1}^{n-1} P(A_i)
\end{eqnarray*}
so that when k=n:
\begin{eqnarray*}
P(\bigcup_{i=1}^{n-1} A_i)+P(A_n) \leq \sum_{i=1}^{n-1} P(A_i)+P(A_n)
\end{eqnarray*}
and
\begin{eqnarray*}
P(\bigcup_{i=1}^nA_i)=P(\bigcup_{i=1}^{n-1}A_i\bigcup A_n) \leq \bigcup_{i=1}^{n-1}+ A_n
\end{eqnarray*}
so by Mathematical induction proof:
\begin{eqnarray*}
P(\bigcup_{i=1}^n A_i) \leq \sum_{i=1}^n P(A_i)
\end{eqnarray*}
Let
\begin{eqnarray*}
B_1=A_1,B_2=A_2A_1^c,B_3=A_3A_2^cA_1^c,...,B_n=A_nA_{n-1}^c...A_1^c (B_i\subset A_i)
\end{eqnarray*}
\begin{eqnarray*}
\sum _{i=1}^\infty B_i=\bigcup_ {i=1}^\infty A_i, B_iB_j=\varnothing (i\neq j)
\end{eqnarray*}
so
\begin{eqnarray*}
P(\bigcup _{i=1}^\infty A_i)=P(\sum _{i=1}^\infty B_i)=\sum _{i=1}^\infty P(B_i)\leq \sum _{i=1}^\infty P(A_i)
\end{eqnarray*}
\end{proof}
\qed
%=============================
%===第3题
\begin{exercise}
(Additive Theorem)For any finite number of events,we have\\
$P(\bigcup_{j=1}^n A_j)=\sum_{j=1}^n P(A_j)-\sum_{1\leq j_1< j_2\leq n}P(A_{j_1}\cap A_{j_2}+\sum_{1\leq j_1< j_2\leq n}P(A_{j_1}\cap A_{j_2}\cap A_{j_3})-...+(-1)^{n+1}P(A_1\cap A_2\cap...\cap A_n). $
Proofing this theorem.
\end{exercise}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\begin{proof}
We have\\
\begin{eqnarray*}
P(\bigcup_{j=1}^{k+1} A_j)=P((\bigcup_{j=1}^kA_j)\cup A_{k+1})
\end{eqnarray*}
\begin{eqnarray*}
=P(\bigcup_{j=1}^k A_j)+P(A_{k+1})-P((\bigcup_{j=1}^kA_j)\cap A_{k+1})
\end{eqnarray*}
\begin{eqnarray*}
=[\sum _{j_1}^k P(A_j)-\sum_{1\leq j_1< j_2\leq k}P(A_{j_1}\cap A_{j-2})
\end{eqnarray*}
\begin{eqnarray*}
+\sum_{1\leq j_1< j_2\leq k}P(A_{j_1}\cap A_{j_2}\cap A_{j_3})
\end{eqnarray*}
\begin{eqnarray*}
-...+(-1)^{k+1}P(A_1\cap A_2\cap ...\cap A_k)]
\end{eqnarray*}
\begin{eqnarray*}
+P(A_{k+1})-P(\bigcup_{j=1}^k(A_j\cap A_{k+1}))
\end{eqnarray*}
\begin{eqnarray*}
=\sum _{j=1}^{k+1} P(A_j)-\sum_{1\leq j_1< j_2\leq k}P(A_{j_1}\cap A_{j_2})
\end{eqnarray*}
\begin{eqnarray*}
+\sum_{1\leq j_1< j_2\leq k}P(A_{j_1}\cap A_{j_2}\cap A_{j_3})
\end{eqnarray*}
\begin{eqnarray*}
-...+(-1)^{k+1}P(A_1\cap A_2\cap ...\cap A_k)-P(\bigcup_{j=1}^k(A_j\cap A_{k+1}))
\end{eqnarray*}
But\\
\begin{eqnarray*}
P(\bigcup_{j=1}^k(A_j\cap A_{k+1}))=\sum _{j=1}^k P(A_j\cap A_{k+1})
\end{eqnarray*}
\begin{eqnarray*}
-\sum_{1\leq j_1< j_2\leq k}  P(A_{j_1}\cap A_{j-2}\cap A_{k+1})
\end{eqnarray*}
\begin{eqnarray*}
+\sum_{1\leq j_1< j_2\leq k}P(A_{j_1}\cap A_{j_2}\cap A_{j_3}\cap A_{k+1})
\end{eqnarray*}
\begin{eqnarray*}
-...+(-1)^k\sum_{1\leq j_1< j_2<...j_{k-1}\leq k}P(A_{j_1}\cap ...\cap A_{j{k-1}}\cap A_{k+1})
\end{eqnarray*}
\begin{eqnarray*}
+(-1)^{k+1}P(A_1\cap ...\cap A_k\cap A_{k+1}).
\end{eqnarray*}
Replacing this in (1).We get \\
\begin{eqnarray*}
P(\bigcup_{j=1}^{k+1}P(A-j)-[\sum_{1\leq j_1< j_2\leq k}P(A_{j_1}\cap A_{j_2})
\end{eqnarray*}
\begin{eqnarray*}
+\sum_{j=1}^kP(A_j\cap A_{k+1})]+[\sum_{1\leq j_1< j_2<j-3\leq k}P(A_{j_1}\cap A_{j_2}\cap A_{j_3})
\end{eqnarray*}
\begin{eqnarray*}
+\sum_{1\leq j_1< j_2< j_3\leq k } P(A_{j_1}\cap A_{j_2}\cap A_{k+1})]
\end{eqnarray*}
\begin{eqnarray*}
-...+(-1)^{k+1}[P(A_1\cap ...\cap A_k)
\end{eqnarray*}
\begin{eqnarray*}
+\sum_{1\leq j_1< j_2<...j_{k-1}\leq k}P(A_{j_1}\cap ...\cap A_{j{k-1}}\cap A_{k+1})]
\end{eqnarray*}
\begin{eqnarray*}
+(-1)^{k+2}P(A_1\cap...\cap A_k\cap A_{k+1})
\end{eqnarray*}
\begin{eqnarray*}
=\sum_{j=1}^{k+1} P(A_j)-\sum_{1\leq j_1< j_2\leq {k+1}}P(A_{j_1}\cap A_{j_2}
\end{eqnarray*}
\begin{eqnarray*}
+\sum_{1\leq j_1< j_2\leq {k+1}}P(A_{j_1}\cap A_{j_2}\cap A_{j_3})
\end{eqnarray*}
\begin{eqnarray*}
-...+(-1)^{k+2}P(A_1\cap A_2\cap...\cap A_{k+1}).
\end{eqnarray*}
The proof is complete.
\end{proof}

%=============================
%===第4题
\begin{exercise}
Cheek $P(.$\big |$ A) is a probability (measure)$
\end{exercise}
\noindent\begin{proof}
By probability' s definition:
\begin{itemize}
\item[(i).]~for $ P(B$\big |$ A)=\frac{P(AB)}{P(A)}$ and $P(A)>0,P(AB)\geq 0$\\
so that $P(B$\big |$ A)\geq 0$
\item[(ii).]~since $ P(B$\big |$ A)=\frac{P(AB)}{P(A)}$ for every $ B\in F(F is a \sigma-field)$ ,so P(S)=1
\item[(iii).]~$<\sigma-additivity>$\\
let $C_1,C_2,...,C_n,... B_1,B_2,...B_n,...$ be mutually disjoint events,then proof
\begin{eqnarray*}
P(\sum_{i=1}^\infty C_i)=\sum_{i=1}^\infty P(C_i)
\end{eqnarray*}
Easy to know:
\begin{eqnarray*}
 P( C_1+C_2)=\frac{P(A(B_1\cup B_2)}{P(A)}=\frac{P(AB_1+ AB_2)}{P(A)}=P(C_1)+P(C_2)
\end{eqnarray*}
By Mathematical induction proof:
\begin{eqnarray*}
P(\sum_{i=1}^\infty C_i)=\sum_{i=1}^\infty P(C_i)
\end{eqnarray*}
The proof is complete.
\end{itemize}
\end{proof}
%=============================
%===第5题
\begin{exercise}
Show that:$A\in \mathscr{F},\mathscr{F} is a \sigma-field ,A\cap \mathscr{F}=\{A\cap B,B\in \mathscr{F}\}$,$ A\cap \mathscr{F}$ is a $\sigma-field $.
\end{exercise}
\noindent\begin{proof}
Assume $\mathscr{A}=A\cap \mathscr{F}$
\begin{itemize}
\item[(i).]~for $A\in \mathscr{F}$,and easy to know that $S\in \mathscr{A} $
\item[(ii).]~$A^c\in \mathscr{F},B^c\in \mathscr{F}$ ,implies $A^c\cup B^c \in \mathscr{F}$,and $A\cap \mathscr{F}=A\cap B$ for every $ B \in \mathscr{F}$ ,and $ (A\cap B)^c=A^c\cup B^c$ so that $(A\cap B)^c\in \mathscr{A}$
\item[(iii).]~Assume $B=B_1+B_2+...+B_n+...$\\
so $A\cap B=A\cap (B_1+B_2+...+B_n+...) =(A\cap B_1)+(A\cap B_2)+...+(A\cap B_n)+...$\\
when $A\cap B_i \in \mathscr{A} i=1,2...$ \\
    Proof
\begin{eqnarray*}
 \bigcup_{i=1}^\infty A\cap B_i \in \mathscr{A}
 \end{eqnarray*}
    since
    \begin{eqnarray*}
    A\cap B_i \in \mathscr{A},and A\in \mathscr{F},B\in \mathscr{F} ,so A\cap B_i\in \mathscr{F},
    \end{eqnarray*}
    then
    \begin{eqnarray*}
     \bigcup_{i=1}^\infty A\cap B_i\in \mathscr{F}
     \end{eqnarray*}
     so
     \begin{eqnarray*}
      \bigcup_{i=1}^\infty A\cap B_i \in \mathscr{A}
    \end{eqnarray*}
\end{itemize}
\end{proof}
\end{document}

```

> FWEFWFWWEF
> FWEFWEF WFEWF

![MY](https://avatars0.githubusercontent.com/u/46896490?s=460&v=4)

[FWFWFEFW](FWEFWEW)

我们理解您需要更便捷更高效的工具记录思想，整理笔记、知识，并将其中承载的价值传播给他人，**Cmd Markdown** 是我们给出的答案 —— 我们为记录思想和分享知识提供更专业的工具。 您可以使用 Cmd Markdown：

> * 整理知识，学习笔记
> * 发布日记，杂文，所见所想
> * 撰写发布技术文稿（代码支持）
> * 撰写发布学术论文（LaTeX 公式支持）

![cmd-markdown-logo](https://www.zybuluo.com/static/img/logo.png)

除了您现在看到的这个 Cmd Markdown 在线版本，您还可以前往以下网址下载：

### [Windows/Mac/Linux 全平台客户端](https://www.zybuluo.com/cmd/)

> 请保留此份 Cmd Markdown 的欢迎稿兼使用说明，如需撰写新稿件，点击顶部工具栏右侧的 <i class="icon-file"></i> **新文稿** 或者使用快捷键 `Ctrl+Alt+N`。

------

## 什么是 Markdown

Markdown 是一种方便记忆、书写的纯文本标记语言，用户可以使用这些标记符号以最小的输入代价生成极富表现力的文档：譬如您正在阅读的这份文档。它使用简单的符号标记不同的标题，分割不同的段落，**粗体** 或者 *斜体* 某些文字，更棒的是，它还可以

### 1. 制作一份待办事宜 [Todo 列表](https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown#13-待办事宜-todo-列表)

- [ ] 支持以 PDF 格式导出文稿
- [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
- [x] 新增 Todo 列表功能
- [x] 修复 LaTex 公式渲染问题
- [x] 新增 LaTex 公式编号功能

### 2. 书写一个质能守恒公式[^LaTeX]

$$E=mc^2$$

### 3. 高亮一段代码[^code]

```python
@requires_authorization
class SomeClass:
    pass

if __name__ == '__main__':
    # A comment
    print 'hello world'
```

### 4. 高效绘制 [流程图](https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown#7-流程图)

```flow
st=>start: Start
op=>operation: Your Operation
cond=>condition: Yes or No?
e=>end

st->op->cond
cond(yes)->e
cond(no)->op
```

### 5. 高效绘制 [序列图](https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown#8-序列图)

```seq
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```

### 6. 高效绘制 [甘特图](https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown#9-甘特图)

```gantt
    title 项目开发流程
    section 项目确定
        需求分析       :a1, 2016-06-22, 3d
        可行性报告     :after a1, 5d
        概念验证       : 5d
    section 项目实施
        概要设计      :2016-07-05  , 5d
        详细设计      :2016-07-08, 10d
        编码          :2016-07-15, 10d
        测试          :2016-07-22, 5d
    section 发布验收
        发布: 2d
        验收: 3d
```

### 7. 绘制表格

| 项目        | 价格   |  数量  |
| --------   | -----:  | :----:  |
| 计算机     | \$1600 |   5     |
| 手机        |   \$12   |   12   |
| 管线        |    \$1    |  234  |

### 8. 更详细语法说明

想要查看更详细的语法说明，可以参考我们准备的 [Cmd Markdown 简明语法手册][1]，进阶用户可以参考 [Cmd Markdown 高阶语法手册][2] 了解更多高级功能。

总而言之，不同于其它 *所见即所得* 的编辑器：你只需使用键盘专注于书写文本内容，就可以生成印刷级的排版格式，省却在键盘和工具栏之间来回切换，调整内容和格式的麻烦。**Markdown 在流畅的书写和印刷级的阅读体验之间找到了平衡。** 目前它已经成为世界上最大的技术分享网站 GitHub 和 技术问答网站 StackOverFlow 的御用书写格式。

---

## 什么是 Cmd Markdown

您可以使用很多工具书写 Markdown，但是 Cmd Markdown 是这个星球上我们已知的、最好的 Markdown 工具——没有之一 ：）因为深信文字的力量，所以我们和你一样，对流畅书写，分享思想和知识，以及阅读体验有极致的追求，我们把对于这些诉求的回应整合在 Cmd Markdown，并且一次，两次，三次，乃至无数次地提升这个工具的体验，最终将它演化成一个 **编辑/发布/阅读** Markdown 的在线平台——您可以在任何地方，任何系统/设备上管理这里的文字。

### 1. 实时同步预览

我们将 Cmd Markdown 的主界面一分为二，左边为**编辑区**，右边为**预览区**，在编辑区的操作会实时地渲染到预览区方便查看最终的版面效果，并且如果你在其中一个区拖动滚动条，我们有一个巧妙的算法把另一个区的滚动条同步到等价的位置，超酷！

### 2. 编辑工具栏

也许您还是一个 Markdown 语法的新手，在您完全熟悉它之前，我们在 **编辑区** 的顶部放置了一个如下图所示的工具栏，您可以使用鼠标在工具栏上调整格式，不过我们仍旧鼓励你使用键盘标记格式，提高书写的流畅度。

![tool-editor](https://www.zybuluo.com/static/img/toolbar-editor.png)

### 3. 编辑模式

完全心无旁骛的方式编辑文字：点击 **编辑工具栏** 最右侧的拉伸按钮或者按下 `Ctrl + M`，将 Cmd Markdown 切换到独立的编辑模式，这是一个极度简洁的写作环境，所有可能会引起分心的元素都已经被挪除，超清爽！

### 4. 实时的云端文稿

为了保障数据安全，Cmd Markdown 会将您每一次击键的内容保存至云端，同时在 **编辑工具栏** 的最右侧提示 `已保存` 的字样。无需担心浏览器崩溃，机器掉电或者地震，海啸——在编辑的过程中随时关闭浏览器或者机器，下一次回到 Cmd Markdown 的时候继续写作。

### 5. 离线模式

在网络环境不稳定的情况下记录文字一样很安全！在您写作的时候，如果电脑突然失去网络连接，Cmd Markdown 会智能切换至离线模式，将您后续键入的文字保存在本地，直到网络恢复再将他们传送至云端，即使在网络恢复前关闭浏览器或者电脑，一样没有问题，等到下次开启 Cmd Markdown 的时候，她会提醒您将离线保存的文字传送至云端。简而言之，我们尽最大的努力保障您文字的安全。

### 6. 管理工具栏

为了便于管理您的文稿，在 **预览区** 的顶部放置了如下所示的 **管理工具栏**：

![tool-manager](https://www.zybuluo.com/static/img/toolbar-manager.jpg)

通过管理工具栏可以：

<i class="icon-share"></i> 发布：将当前的文稿生成固定链接，在网络上发布，分享
<i class="icon-file"></i> 新建：开始撰写一篇新的文稿
<i class="icon-trash"></i> 删除：删除当前的文稿
<i class="icon-cloud"></i> 导出：将当前的文稿转化为 Markdown 文本或者 Html 格式，并导出到本地
<i class="icon-reorder"></i> 列表：所有新增和过往的文稿都可以在这里查看、操作
<i class="icon-pencil"></i> 模式：切换 普通/Vim/Emacs 编辑模式

### 7. 阅读工具栏

![tool-manager](https://www.zybuluo.com/static/img/toolbar-reader.jpg)

通过 **预览区** 右上角的 **阅读工具栏**，可以查看当前文稿的目录并增强阅读体验。

工具栏上的五个图标依次为：

<i class="icon-list"></i> 目录：快速导航当前文稿的目录结构以跳转到感兴趣的段落
<i class="icon-chevron-sign-left"></i> 视图：互换左边编辑区和右边预览区的位置
<i class="icon-adjust"></i> 主题：内置了黑白两种模式的主题，试试 **黑色主题**，超炫！
<i class="icon-desktop"></i> 阅读：心无旁骛的阅读模式提供超一流的阅读体验
<i class="icon-fullscreen"></i> 全屏：简洁，简洁，再简洁，一个完全沉浸式的写作和阅读环境

### 8. 阅读模式

在 **阅读工具栏** 点击 <i class="icon-desktop"></i> 或者按下 `Ctrl+Alt+M` 随即进入独立的阅读模式界面，我们在版面渲染上的每一个细节：字体，字号，行间距，前背景色都倾注了大量的时间，努力提升阅读的体验和品质。

### 9. 标签、分类和搜索

在编辑区任意行首位置输入以下格式的文字可以标签当前文档：

标签： 未分类

标签以后的文稿在【文件列表】（Ctrl+Alt+F）里会按照标签分类，用户可以同时使用键盘或者鼠标浏览查看，或者在【文件列表】的搜索文本框内搜索标题关键字过滤文稿，如下图所示：

![file-list](https://www.zybuluo.com/static/img/file-list.png)

### 10. 文稿发布和分享

在您使用 Cmd Markdown 记录，创作，整理，阅读文稿的同时，我们不仅希望它是一个有力的工具，更希望您的思想和知识通过这个平台，连同优质的阅读体验，将他们分享给有相同志趣的人，进而鼓励更多的人来到这里记录分享他们的思想和知识，尝试点击 <i class="icon-share"></i> (Ctrl+Alt+P) 发布这份文档给好友吧！

------

再一次感谢您花费时间阅读这份欢迎稿，点击 <i class="icon-file"></i> (Ctrl+Alt+N) 开始撰写新的文稿吧！祝您在这里记录、阅读、分享愉快！

作者 [@ghosert][3]     
2016 年 07月 07日    

[^LaTeX]: 支持 **LaTeX** 编辑显示支持，例如：$\sum_{i=1}^n a_i=0$， 访问 [MathJax][4] 参考更多使用方法。

[^code]: 代码高亮功能支持包括 Java, Python, JavaScript 在内的，**四十一**种主流编程语言。

[1]: https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown
[2]: https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown#cmd-markdown-高阶语法手册
[3]: http://weibo.com/ghosert
[4]: http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference

