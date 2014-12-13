# はじめに
こちらはQiita API V2 Hackathonで作ったツールです。

作成者: @naoto0822 & @fmy

# Qiita Buttonとは？
Heroku ButtonのようにGithubのREADME.mdに設置して使います。
ボタンを押して、QiitaにログインすることでQiitaにそのまま投稿できます。

# 使い方
こちらに記載してあります
[Github :point_right: Qiita](https://github2qiita.herokuapp.com/)

# 仕組み
Qiitaボタンを押して[Github :point_right: Qiita](https://github2qiita.herokuapp.com/)に遷移すると、リファラからレポジトリを割り出します。
レポジトリ内の`docs/`ディレクトリに含まれるmdファイルをGithub APIから取得し、投稿するmdファイルを選ぶ画面に行きます。
投稿するmdファイルが決定されると再度Github APIからファイルのblobを取得し、Qiita API v2を使ってQiitaに投稿します。
