# iscie.bst

ISCIEの[論文誌，学会誌](https://www.iscie.or.jp/pub/journal)に発行するときに， bibtex を使えるようにする目的で作成した非公式のbstファイルです．

使用中に問題を発見した場合は， [GitHub](https://github.com/knttnk/sci_bst) で issue を建ててください．

# Set up

1. bibファイルを用意してください．Google Scholar から取ってきた場合は，書籍も`@article`になっていることがありますので，注意してください．
2. リリースにある iscie.bst というファイルをダウンロードし，テキストエディタで開いてつぎの設定をしてください．
   17行目，用意したbibファイルの書き方に応じて設定をします．
   ```bst
   FUNCTION {bib.first.comma.last}
   { #1 }	  % (default) zoteroやGoogle Scholarの書き方 → author = {山田, 太郎} or author = {太郎 山田} 
   % { #0 }    % 昔からの書き方 → author = {山田 太郎} or author = {太郎, 山田}
   ```
   25行目，Vol, No, ppの見た目の設定をします．
   ```bst
   FUNCTION {max.tilde.length}
   { #11 }	  % (default)
   % { #0 }
   ```
3. iscie.bst を配置します．フォルダごと提出しなければならない場合など，別PCでも環境を再現したい場合は，texファイルと同じ場所に置いてください．PDFファイルだけを作成したり提出したりしたい場合は，`[home]/texmf/bibtex/bst`に配置すると，毎回この作業をすることなく iscie.bst が使えます．

# Example
`test/test.tex` をご覧ください．

# Trouble shooting
### 日本語論文で，著者の名字が表示されない．
Set upの2をご覧ください．

### Shun-ichi が S.-i. と表記される
ローマ字で「しゅんいち」と「しゅにち」を区別するために`Shun-ichi`と書くことがあります．しかし，.bibファイルでもこう書いてしまうと`S.-i.`と表示されてしまうので，`Shun'ichi`といった表記に変更してください．
