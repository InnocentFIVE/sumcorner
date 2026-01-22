人类从未知晓萨姆之角的真实样貌。

> 多年以后，翻开*The TeXbook*，你仍然将会回想起我带你去见识萨姆之角的那个遥远的下午。

# 萨姆之角

这是一个尝试，用来证明萨姆之角存在性的尝试，为此，我们大量地使用了幻影。除了在文档之中，我们很难意识到萨姆之角的存在性：这是一个非常微妙的细节问题。
为了阐明清楚这个概念，我们不得不从1991年开始说起。著名计算机科学家高德纳在他的著作*The TeXbook*中提出萨姆之角这一概念（事实上，是习题18.44），他将其视为一个难度等级为$2$的习题。
之后，他在同一本著作中，给出了如下论证：

```tex
\def\sumprime_#1{\setbox0=\hbox{$\scriptstyle{#1}$}
\setbox2=\hbox{$\displaystyle{\sum}$}
\setbox4=\hbox{${}'\mathsurround=0pt$}
\dimen0=.5\wd0 \advance\dimen0 by-.5\wd2
\ifdim\dimen0>0pt
\ifdim\dimen0>\wd4 \kern\wd4 \else\kern\dimen0\fi\fi
\mathop{{\sum}'}_{\kern-\wd4 #1}}
```

这个论证正是我们的雏形。

