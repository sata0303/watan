---
layout: splash
classes: wide
sidebar: false
title: LaTeXについてのメモ
author_profile: false
permalink: false
tags:
- LaTeX
---
<link rel="stylesheet" href="../vs2015.css">
<script src="../highlight.pack.js"></script>
<script>
hljs.initHighlightingOnLoad();
</script>


## 導入
環境: Windows 10 / Dell Inspiron 3881</br>

・TeX Live のインストール</br>
・VSCode のインストール</br>
・VSCode の拡張機能のインストール</br>
・

## プリアンブル（\documentclass{...}から\begin{document}の間）
<font size = "3">
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
</font>

## 本文
<font size = "3">
<pre>
 <code class="latex">
\citep{bibkey}
\citet{bibkey}

\nocite{}　%参考文献一覧
\kenten{sentence}  %圏点を付す
\bibliographystyle{}  %引用スタイル（.bstの指定）
\biblipgraphy{}  %.bibの指定


</code>
</pre>
</font>


