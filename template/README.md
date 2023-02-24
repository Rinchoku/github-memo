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
