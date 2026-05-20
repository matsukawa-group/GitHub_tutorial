# Step 1

Step 1 では Git/GitHub を実際に使う前の準備段階として，Git/GitHub の概念を知り，環境構築を行う．
この step では基本的に単独作業となるが，ペアの学生同士でチェックしながら進めるとよいだろう．
環境構築で失敗すると先に進めないので困ったら先輩に相談しよう．

## Git/GitHub の概念を知ろう

Git/GitHub の概念について知る．
詳細は [渡辺宙志先生のスライド](https://kaityo256.github.io/github/) を全員で見て学べばよい．

- 「バージョン管理とは」
- 「Git の仕組みと用語」

の二つを全員で見る．
その際，司会進行役が説明しながら進めればよい．
他のスライドを見ても構わないが，聞いているだけだと B4 が退屈してしまうのと，実感が湧かないのでこの二つくらいでよいと思う．

## 環境構築

### Git のインストール

Git のインストール前にコードエディター（VS Code）は入れておくように．

#### Windows

Windows ユーザーが Git を使うには WSL を使う方法と Git for Windows を使う方法がある．
どちらでもいいが，ここでは Git for Windows を使う場合の説明をする．

WinGet を使うとインストールが楽なので WinGet が入っているか確認しておこう．
`cmd.exe` で以下のように入力，`Enter`．

```
winget install --scope machine Git.Git
```

以下のような画面になったらインストール成功．

<img src="files/Step1/winget.png" width="80%" style="display: block; margin: auto;">

<details>
<summary>GUI でインストールする場合（WinGet を使用する人は読まなくていいです）</summary>

[このリンク](https://git-scm.com/downloads) から Windows に対応しているファイルをダウンロードしてインストールする．
最新版をインストールすればよい．

<img src="files/Step1/git-install.png" width="80%" style="display: block; margin: auto;">

インストール作業ではいくつか設定項目を聞かれる．

<img src="files/Step1/git-setup1.png" width="80%" style="display: block; margin: auto;">

Next をクリック．

<img src="files/Step1/git-setup2.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup3.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup4.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup5.png" width="80%" style="display: block; margin: auto;">

Git の編集に用いるコードエディターが標準だと Vim になっているので，VS Code にしておこう．
Use Visual Studio Code as Git's default editor を選択．
ここで間違えて他のエディターにしても後で修正可能．

<img src="files/Step1/git-setup6.png" width="80%" style="display: block; margin: auto;">

リポジトリ作成時の初期ブランチ名の設定．
デフォルトで `master` になっている場合は `main` に変更しておこう．
これは計算機で古くから用いられている master/slave によるものだが，用語の使い方に関して論争があるので近年は Git において `main` を使う風潮にある．
もし間違えて `master` のままインストールしても後で変更可能．

<img src="files/Step1/git-setup7.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup8.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup9.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup10.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup11.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup12.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup13.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup14.png" width="80%" style="display: block; margin: auto;">

特にこだわりが無ければこのまま Next．

<img src="files/Step1/git-setup15.png" width="80%" style="display: block; margin: auto;">

インストール中．

<img src="files/Step1/git-setup16.png" width="80%" style="display: block; margin: auto;">

インストールが完了するとこの画面になる．

</details>

インストールが完了したら Windows キーを押してアプリケーション一覧を確認．
Git 関連がインストールされているのを確認し，Git Bash を起動．
このとき，Git Bash をタスクバーに追加しておくとよいだろう．
Git Bash は Windows で Git を使う際に Linux コマンドで動作するターミナルとなる．
Git 使用時以外も普段から Linux コマンドで諸々の作業をして構わない．

確認のため

```bash
git --version
```

を実行し，バージョン情報が出てきたらインストール成功．


※基本的には問題はないが，Git Bash 上で日本語が文字化けすることがある．気になるようであれば [こちら](https://qiita.com/OharanD/items/616021c72f8890a429dd) を参照し，設定を変更すること．

#### Mac OS

Mac OS ユーザーが Git を導入する方法はさまざまあるが，Homebrew を導入するのが最も容易である．
Homebrew をインストールする手順は以下の通りである（Homebrew をインストール済みの人は「Homebrew をインストールしたら〜」に進む）．

1. [このリンク](https://brew.sh/ja/)からインストールコマンドをコピー
1. 「ターミナル」アプリを立ち上げる
1. 手順 1 でコピーしたリンクを貼り付けて，実行（インストールには時間がかかるので，ターミナルを閉じずに待つ）
1. 終わったらパスを通すように表示されるので，その 2 行をコピーしてターミナルに貼り付けて実行

Homebrew をインストールしたら，以下のインストールコマンド

```zsh
brew install git
```

を実行して，Git をインストールする．
終えたら，確認のため

```zsh
git --version
```

を実行する．
Git のバージョンが表示されれば，インストールが成功している．

