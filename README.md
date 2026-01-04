# packeage.yml
dbt における packages.yml は、
他の dbt プロジェクト（パッケージ）を自分のプロジェクトに取り込むための設定ファイルです。  
簡単に言うと、**dbt版の「依存ライブラリ管理ファイル」** です

# dbt deps コマンド
packageをインストールするコマンド  
https://docs.getdbt.com/reference/commands/deps

## pinning
dbt deps を実行すると`package-lock.yml`を更新、作成する。  
https://docs.getdbt.com/docs/build/packages#pinning-packages

# デフォルトパス
packaged-install-pathは、dbt_packages
https://docs.getdbt.com/docs/build/packages#how-do-i-add-a-package-to-my-project


# packaged-install-path
dbt-project.yml に以下のような記載がある
`packages-install-path: directorypath`
https://docs.getdbt.com/reference/project-configs/packages-install-path


# dbt elementaryバージョン確認方法
## pip
pipでインストールした場合
pip show dbt-elementary

## edr
Elementary は edr という CLI を提供しています。
edr --version



# 確認する
- どうインストールしたか？
- dbt_project.ymlのpackages-install-pathを確認
- package-lock.ymlでelementaryのバージョン確認
- edr --version でelementaryのバージョン確認
- package.ymlでelementaryの記述削除し動作確認
