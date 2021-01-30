---
layout: single
classes: wide
title: LaTeXについてのメモ
author_profile: false
permalink: false
tags:
- LaTeX
---
<link rel="stylesheet" href="http://wwww.watan.tokyo/default.css">
<script src="http://www.watan.tokyo/highlight.pack.js"></script>
<script>
hljs.initHighlightingOnLoad();
</script>



## プリアンブル（\documentclass{...}から\begin{document}の間）

<pre>
 <code class="latex">
\documentclass[dvipdfmx,12pt,oneside]{jsbook}　　%文書の形式（jsarticleなど）
\setlength{\textwidth}{\fullwidth}  %本文の幅(textwidth)を全体の幅(=ヘッダ部の幅)にそろえる
\addtolength{\fullwidth}{-5truemm}
\setlength{\evensidemargin}{\oddsidemargin} %偶数ページの余白と奇数ページの余白をそろえる

\usepackage[bottom=35truemm,left=30truemm,right=20truemm]{geometry}　%余白の設定
\usepackage{graphicx}  %図の挿入
\usepackage{natbib}　%引用のためのパッケージ
\usepackage{epigraph}  %エピグラフの挿入
\setlength{\epigraphwidth}{.6\textwidth}
\setlength{\epigraphrule}{0pt}
\usepackage{multirow}
\usepackage{diagbox}
\usepackage[hyphens]{url}
\usepackage{pxrubrica} %圏点

\usepackage{type1ec} %ロシア語入力のため
\usepackage[OT2,T1]{fontenc}	% ロシア語入力のためのおまじない
\usepackage[japanese,russian]{babel}　%ロシア語入力のため
</code>
</pre>

## 本文
