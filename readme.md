# iscie.bst

ISCIEの[論文誌，学会誌](https://www.iscie.or.jp/pub/journal)に発行するときに， bibtex を使えるようにする目的で作成した非公式のbstファイルです．

使用中に問題を発見した場合は， [GitHub](https://github.com/knttnk/sci_bst) で issue を建ててください．

# Set up

1. フォルダごと提出しなければならない場合など，別PCでも環境を再現したい場合は，リリースの iscie.bst というファイルを，texファイルと同じ場所に置いてください．PDFファイルだけを作成したり提出したりしたい場合は，`[home]/texmf/bibtex/bst`に配置すると，毎回この作業をすることなく iscie.bst が使えます．
2. bibファイルを用意してください．Google Scholar から取ってきた場合は書籍も`@article`になっていることがありますので，注意してください．

# Example
`test/test.tex` をご覧ください．

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
