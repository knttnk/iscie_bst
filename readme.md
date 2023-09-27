# sci.bst

ISCIEの[論文誌，学会誌](https://www.iscie.or.jp/pub/journal)に発行するときに， bibtex を使えるようにする目的で作成した非公式のbstファイルです．

使用中に問題を発見した場合は， [GitHub](https://github.com/knttnk/sci_bst) で issue を建ててください．

# Install
TODO: 書く

# Example
```tex
\documentclass[J]{jsarticle}

\begin{document}

\bibliographystyle{sci}
\bibliography{bibtex}

\end{document}

```

# Trouble shooting
### 日本語論文で，著者の名字が表示されない．
お使いの.bibファイルの方で，
```bib
@article{example,
  author = {山田 太郎 and 山田 花子},
}
```
のように，著者を `姓 名 and 姓2 名2 and ...` のように修正してください．

### Shun-ichi が S.-i. と表記される
ローマ字で「しゅんいち」と「しゅにち」を区別するために`Shun-ichi`と書くことがあります．しかし，.bibファイルでもこう書いてしまうと`S.-i.`と表示されてしまうので，`Shun'ichi`といった表記に修正してください．
