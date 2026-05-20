# Step 2

Step 2 では実際に Git/GitHub を触って基本的な使用方法を身につける．
この step では基本的に単独作業となるが，ペアの学生同士でチェックしながら進めるとよいだろう．

## GitHub でリモートリポジトリを作成する

1. GitHub 個人ページにアクセス．
2. 上部の Repositories を選択し，右上の New から新しいリポジトリを作成．
3. Owner を確認．
   - もし研究室の Organization で共有する場合は Owner を変更する．
   - ここでは練習のため，自分のアカウントを選択．
4. リポジトリ名を入力する（Repository name）．
   - ある Owner が同じ名前のリポジトリ名を持つことはできない．
   - 何のファイルを管理しているかわかるような名称にしよう．
   - ここでは練習のため，`github_tutorial_***` のようにする．`***` は自分の名前のアルファベット．後で共同編集の練習をするため，誰が管理しているリポジトリかわかるようにしておく．
5. リポジトリの概要を入力する（Description）．
   - ここでは練習のため，「GitHub チュートリアル」にでもしておこう．
6. リポジトリの可視性を確認する．
   - **Public を選択すると全世界にソースコードが公開されてしまうので，研究で使用するものは基本的に Private で作成すること．**
   - リポジトリの可視性については [GitHub ドキュメント | リポジトリの可視性を設定する](https://docs.github.com/ja/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility) も参照するように．
   - ここでは練習のため，Private で作成する．
7. Initialize this repository with: Add a README file
   - チェックを入れるとリポジトリ内の説明事項を記入する `README.md` を作成できる．
   - ここでは練習のため，チェックを入れる．
8. Add .gitignore で `.gitignore` を作成する．
   - `.gitignore` は Git で管理しないファイル一覧を記載するファイル．
   - 各言語ごとに `.gitignore` のテンプレートが用意されている．
   - ここでは練習のため，Python を選択する．この後 Python を使用するわけではない．ただの練習．
9. Choose a license
   - ライセンスを選択できる．
   - 練習時は何も選択しなくてよい．
10. Create repositories を選択．
11. リポジトリを作成できたらリポジトリ名の隣に錠のマークがついていることを確認（private リポジトリになっているか確認）．


