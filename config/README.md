# 設定ファイル周りの備忘録

設定ファイルについての記録

## Issue

`.github/ISSUE_TEMPLATE/config.yml`に記載

下記の設定が可能

* テンプレートの利用を強制(`blank_issues_enabled`)
* Issue選択画面にテンプレートとは別のリンクを設置(例ではCommunityへのリンク)(`contact_links`)

## dependabot

[dependabot.yml](https://docs.github.com/ja/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file)
`.github/dependabot.yml`に記載

dependabotは、パッケージ(composer.jsonやpackage.jsonなど)のバージョン更新まわりを管理してくれるbot

デフォルトでは適宜更新を検知して最大5つのPRを作成するだけになる
dependabot.ymlを作成することで、各パッケージ単位で下記のような設定ができる

* PRを作成する間隔(スケジュール)
* 担当者やレビュワー
* ラベル付
* マージ先branch
* 更新対象・無視するパッケージ

本Repositoryではパッケージ管理ツールを入れていないため、コメントで個人的お薦めを追加しておく

dependabot.ymlを設定することでdependency graphで更新時のログも確認することができる

## コードオーナー

[CODEOWNERS](https://docs.github.com/ja/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)

レポジトリに書き込み権限を持っているユーザ・チームの設定が行える
コードオーナーに設定されると下記のような恩恵があります

* PR作成時に自動でレビュワーに追加される
* マージルールにコードオーナーの承認必須を有効化できる

設定するには`.github/CODEOWNERS`を追加する

記法としては下記

```
<ファイルを示す正規表現> <オーナーにするユーザー・チーム名>
```

## Github Actions

サードパーティAPIやインテグレーションを利用して、アクションを定義できる
多くはCI/CDで使われていたりする

ファイルの設置箇所は特にないらしいが、`.github`配下に置くことを推奨している
設置する際は`action.yml`の形式で設置する

今後整理した際に具体的に明記する
