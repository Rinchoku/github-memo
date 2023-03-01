# テンプレートファイル周りの備忘録

GitHubにはいろんなテンプレートが存在する
ただし私個人はどんなテンプレートが存在するのかわからないのでここに記していく

## Pull Request テンプレート

[Pull Request Template](https://docs.github.com/ja/communities/using-templates-to-encourage-useful-issues-and-pull-requests/creating-a-pull-request-template-for-your-repository)

「pull_request_template.md」というファイルを下記ディレクトリのいずれかに設置する

* ルートディレクトリ
* `docs/`ディレクトリ配下
* `.github/`ディレクトリ配下

複数のプルリクエストテンプレートを用いたい場合は上記のディレクトリのどこかに `PULL_REQUEST_TEMPLATE` を配置し、その中にテンプレートファイルを設置

複数のテンプレートファイルを扱う場合はクエリパラメータ(template=<利用するテンプレートファイル名>)を利用しないと活用ができない
[クエリパラメータを利用したPull Request作成方法](https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/using-query-parameters-to-create-a-pull-request)
例：https://github.com/Rinchoku/github-memo/compare/test?expand=1&template=pull_request_template_ver1.md

基本的には `docs`または`.github`のどちらかに設置するのが良いと考えられる
個人的には複数テンプレートは使いづらいイメージ

追記：commit順序の可能性もあるが、docsと.githubに両方ある場合は.githubが反映されるっぽい？

## Issue テンプレート

[Issue Templateについて](https://docs.github.com/ja/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates)
[Issue Templateの設定方法](https://docs.github.com/ja/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)

`.github/ISSUE_TEMPLATE`配下に設置する。
複数設置することで用途ごとのISSUEのテンプレートを作成時に選択可能にしてくれる

簡単にISSUEテンプレートを設置する場合GitHubの「Settings > General > Features」のIssue部分に「Set up templates」が存在する
それを押下すると、作成ができる

Issusに設定をかけるので、そちらは`config`内に記載

## Issue Form テンプレート

[Issue Form Template構文](https://docs.github.com/ja/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)

Issueテンプレートは各自が記入してもらう形式だが、Issue Formを利用するとpulldownなどの選択を利用してIssueを作成できるテンプレートができる

Issueテンプレートは自分でmarkdownを書いていくが、Issue FormテンプレートではWebフォームとなるため初心者はより入力がしやすい
また、IssueとIssue Formは共存できるので、命名ルールをしっかり決めて運用すると良さそう

## CONTRIBUTING

[Setting Contributing file](https://docs.github.com/ja/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)

プロジェクトにどのようにコントリビュートすべきかのガイドラインを示すためのファイル
`CONTRIBUTING`を下記ディレクトリのいずれかに記載する

* ルートディレクトリ
* `.github/`
* `docs/`
