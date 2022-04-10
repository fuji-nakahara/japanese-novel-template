# 日本語小説プロジェクトテンプレート

TODO: タイトルを変更し、ここに小説の説明を書く。

## 使い方

[`src`](src) 以下にマークダウンで小説を書きます。

電子書籍の作成に [makimono](https://github.com/fuji-nakahara/makimono) を、校正に [textlint](https://github.com/textlint/textlint) を使用します。

### セットアップ

    $ bundle install
    $ npm install
    $ git grep TODO # and fix them

### 電子書籍のリリース

    $ git tag v1.0.0
    $ git push --tags

自動的に [Ebook ワークフロー](.github/workflows/ebook.yml)が起動し、makimonoを使ってビルドした電子書籍のリリースが行われます。

### 校正の自動レビュー

Pull Requestを作成すると、[reviewdog ワークフロー](.github/workflows/reviewdog.yml)が起動し、textlintによる指摘が行われます。

## ライセンス

TODO
