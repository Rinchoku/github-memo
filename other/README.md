# 概要

このページには設定やテンプレートではない、特殊なファイルについてまとめている

## FUNDING

[スポンサーボタンの設置](https://docs.github.com/ja/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/displaying-a-sponsor-button-in-your-repository)

スポンサーボタンを追加するための設定
`.github`内に`FUNDING.yml`を設置する

ボタンには下記を含めることができる

* GitHub Sponsors のスポンサード開発者
* 外部の資金獲得プラットフォーム
* カスタムの資金獲得 URL

このレポジトリでは役割としておかしいと感じるため設置はしていない

## CITATION

[CITATIONファイルとは](https://docs.github.com/ja/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files)
[What is a CITATION.cff file](https://citation-file-format.github.io/)

自身のレポジトリが別の論文やデータセットを引用していることを知らせるためのファイル
ルートディレクトリに`CITATION.cff`ファイルを設置することで、ランディングページから自動的にリンクされる

別に出典がある場合はしっかり記述をして、引用元を知らせてあげよう
