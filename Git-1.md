## Git講習 第一回
-----------
### 内容
- **Gitとは**
- **Gitのしくみ**
- **Gitの導入**
    - Windows
    - Mac
    - Linux
- **(まとめ)**  
*今日の内容はPro Git2 p7-22(一章)の内容です．*
-----------
### Gitとは
- バージョン管理システムの一つ
- Linuxの開発用に2005年に作られた
- 分散型のバージョン管理システム
----------
### Gitのしくみ
- "スナップショットで，差分ではない"  
    Gitはその他のバージョン管理システム(BitKeeperとかが他にあります)と違い，ファイルの変更を記録していくのではなく，対象ファイルの全体像のスナップショットを管理します．
    「どのファイルのどこを変更したか」というより，「どのファイルが編集されてこうなった」と記録していると考えるといいかもしれません．
- "ほとんど全ての操作がローカル"  
    リポジトリを各自が保持しているので，いちいちサーバーに問い合わせる必要がありません．履歴を確認したければ持っているデータベースから参照することが出来ます．一ヶ月前のファイルとの差分を計算するときも，一ヶ月前のものを調べてローカルで計算できます．
    インターネットに繋がっていない(オフライン)のときでも，アップロードするためにネットにつなぐまで，通常と変わらずコミット出来ます．
- Gitにおける3つの状態  
    Gitではファイルを3つの状態にわけて考えます．コミット済み，ステージ済み，修正済み の3つです．コミット済みの部分は，コミットされ，その後編集されていないファイルがあります．ステージ済みの部分は，編集され，次のコミットに含むファイルがあります．修正済みの部分は，コミットされたかファイルが作成された後，編集されたけれども，次のコミットに含むことにはなっていない状態です．  Gitでは，「ファイルを編集→編集されたファイルのスナップショットをステージ済みにする→ステージ済みのファイルをコミットする．」といった風に作業を進めていきます．
-----------
### Gitのインストール
- Windows  
[Git for Windows](http://git-scm.com/download/win)か，[GitHub Desktop](https://windows.github.com)からインストーラをダウンロードします．  あとはインストーラーの指示に従ってください．
- Mac  
XCodeを入れるのが一番いいと思います．Gitだけでなくたくさんできることあるので．  「それでもGitだけが欲しい」って人には[Git for OS X](https://git-scm.com/download/mac)があるみたいです．
- Linux  
こちらはかなり簡単です．使っているディストリビューションのパッケージ管理コマンドでインストールできます．たとえば, Ubuntu(などのDebian系)なら `$ sudo apt install git -y ` でインストールできます．

- GUI Tools  
GUI(マウスなどで操作)で使えるツールもあります．Windowsの項目のGithub DesktopはGUIでのものですが，オプションでCUI(コマンドを打って操作)が選べるそうです．GUIでもGitを使うことはできるので，いくつかツールが紹介してある[リンク](https://git-scm.com/downloads/guis)を貼っておきます．僕は使ったことが無いのでコレについては聞かれてもあんまり答えられないです．すみません．