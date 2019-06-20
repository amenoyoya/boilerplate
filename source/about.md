---
title: About this Blog
date: 2019-06-20
tags: ['blog', 'GitPress']
excerpt: このブログは、筆者がエンジニアなる生物へと進化するためにコードを書き殴るブログである
---

# 3H Code Work｜yoyablog by GitPress

## What's this Blog?

31歳未経験からプログラマに転職した筆者が、エンジニアなる生物へと進化するためにコードを書き殴るブログ

基本的に頭は悪いので、量質転化の法則に従って、ひたすらコードを書くだけの脳筋プログラマです

### 量質転化の法則
- 量が質に転化するまでは量をこなす必要がある
- 途中でやめると積み上げたものは戻ってしまう

### 3H Code Work
あらゆるプログラムを3時間以内に試作することを至上命題とする

なぜ3時間か？

- 素早いフィードバックを重視するから
- 長い時間をかけようとすると挫折するから
- プライベートで捻出できる時間がそのくらいだから

### 5つの掟
1. 3時間以内に試作せよ
    - いきなり完成形を目指さない
2. 完成度のいかんに関わらず必ずアウトプットせよ
    - アウトプットしないとフィードバックは得られない
    - 結局は、行動力とコミュ力のあるやつが成功する
3. 自動化できるものは絶対に自動化せよ
    - 繰り返し作業であるかどうかに関わらず、自動化できるものは自動化する
        - 絶対にいつか使うタイミングがある
    - 自動化することで、3時間で試作できるものの規模を拡大できる
4. 使えるものは使え
    - 自分で実装する必要がないものは実装しない
    - 3時間で試作するために必要なものは何でも使う
5. 依存するな
    - 4と矛盾するようだが、特定のツールやサービスに依存しないように、極力標準化された技術を使うようにする
    - 依存関係はやっかいなので、なるべく独立させる
        - プログラムでも仕事でも人間関係でも、こじれる前に独立させる

***

## GitPress

このブログは[GitPress](https://gitpress.io/)を使って運営されている

理由は以下の通り

- 新しいものが好きだから
- Markdownで書いてGitHubで管理できるから（Markdown大好き）
- 自分でブログシステムを作るのに3時間以上かかりそうだったから

### Get started (所要時間: 1H)
参考: [paiza開発日誌](https://paiza.hatenablog.com/entry/2019/06/19/Push%E3%81%99%E3%82%8B%E3%81%A0%E3%81%91%EF%BC%81GitHub%E3%81%AE%E3%83%AA%E3%83%9D%E3%82%B8%E3%83%88%E3%83%AA%E3%82%92%E5%80%8B%E4%BA%BA%E3%83%96%E3%83%AD%E3%82%B0%E3%81%AB%E5%A4%89%E3%81%88%E3%81%A6)

#### 前提
以下の事項をクリアしていることを前提とする

- Gitコマンドを使える
- [GitHub](https://github.com)アカウントを持っている

#### 工数
- GitPress公式テンプレートのFork: `0.25H`
- サンプル記事の作成: `0.5H`
- GitPressとGitHubアカウントの連携: `0.25H`

#### GitPress公式テンプレートのFork (所要時間: 0.25H)
- [GitPress公式テンプレート](https://github.com/gitpress-io/boilerplate)のページを訪問
    - 画面右上にある`Fork`ボタンを押す
        - => Forkされたリポジトリが自分のGitHub上に作成される
            - `https://github.com/<アカウント名>/boilerplate`
- ローカル環境にリポジトリをClone
    ```bash
    # プロジェクトディレクトリに移動
    $ cd /path/to/myblog

    # GitリポジトリClone
    $ git init
    $ git remote add origin https://github.com/<アカウント名>/boilerplate.git
    $ git pull origin master
    ```

#### サンプル記事の作成 (所要時間: 0.5H)
- GitPressで記事を投稿するには、`source`ディレクトリにMarkdownファイルを配置すれば良い
    ```markdown: source/sample.md
    ---
    title: サンプル記事
    date: 2019-06-20
    tags: ["sample", "GitPress"]
    excerpt: サンプル記事の抜粋
    ---
    # GitPressサンプル記事

    ## GitPressのMarkdownで使えるFront Matter

    GitPressでは、Markdownファイルの冒頭に以下のような設定項目（Front Matter）を記述することが可能

    - `title`: 記事タイトル
    - `date`: 記事作成日（`yyyy-mm-dd`）
    - `tags`: タグ（配列指定可能）
    - `excerpt`: 抜粋
    ```
- 記事を作成したらGitHubにPushする
    ```bash
    $ git add source/sample.md
    $ git commit -m 'Add｜サンプル記事'
    $ git push -u origin master
    ```

#### GitPressとGitHubアカウントの連携: `0.25H`
- [GitPress公式ページ](https://gitpress.io/)を訪問
    - 画面右上の`Login`ボタンをクリック
    - GitHubアカウントで`Authorize gitpress-io`
        - Select a repository: ForkしたGitPressテンプレート(`boilerplate`)を選択
        - Select a directory: `/source`
    - `Save and next`ボタンをクリック
    - GitHubリポジトリとの同期のためにWebhook接続を`Allow`
- GitPress上に自分のブログが作成される
    - `https://gitpress.io/u/<アカウントID>`
- ブログトップページにPushしたサンプル記事が載っていることを確認できれば完了
