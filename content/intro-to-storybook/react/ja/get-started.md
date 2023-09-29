---
title: 'React 向け Storybook のチュートリアル'
tocTitle: 'はじめに'
description: '開発環境に Storybook を導入しましょう'
commit: 'b3cfa66'
---

Storybook は開発時にアプリケーションと並行して動きます。Storybook を使用することで、UI コンポーネントをビジネスロジックやコンテキストから切り離して開発できるようになります。この文書は React 向けです。他にも [React Native](/intro-to-storybook/react-native/en/get-started)、[Vue](/intro-to-storybook/vue/en/get-started)、[Angular](/intro-to-storybook/angular/en/get-started)、[Svelte](/intro-to-storybook/svelte/en/get-started)、[Ember](/intro-to-storybook/ember/en/get-started) 向けのバージョンがあります。

![Storybook と開発中のアプリの関係](/intro-to-storybook/storybook-relationship.jpg)

## React 向けの Storybook を構築する

Storybook を開発プロセスに組み込むにあたり、いくつかの手順を踏む必要があります。まずは、[degit](https://github.com/Rich-Harris/degit) を使用してビルド環境をセットアップしましょう。このパッケージを利用することで、テンプレート（アプリケーションの一部をデフォルト設定で構築したもの）をダウンロードし、開発ワークフローの短縮に役立てることができます。

それでは、次のコマンドを実行してください:

```shell:clipboard=false
# Clone the template
npx degit chromaui/intro-storybook-react-template taskbox

cd taskbox

# Install dependencies
yarn
```

<div class="aside">
💡 このテンプレートには本バージョンのチュートリアルに必要なスタイル、アセット、最低限の設定が含まれています。
</div>

それでは、アプリケーションのさまざまな環境が問題なく動くことを次のコマンドで確認しましょう:

```shell:clipboard=false
# Start the component explorer on port 6006:
yarn storybook

# Run the frontend app proper on port 5173:
yarn dev
```

私たちの主なフロントエンドアプリの様式： コンポーネント開発（Storybook）とアプリケーション自体

![主な様式](/intro-to-storybook/app-main-modalities-react.png)

作業をする対象に応じて、これら両方を同時に実行したい場合もあります。現在フォーカスしているのは単一の UI コンポーネントを作成することなので、Storybook を実行することにこだわることにしましょう。

## 変更をコミットする

この段階で、ローカルリポジトリにファイルを追加しても大丈夫です。以下のコマンドを実行して、ローカルリポジトリを初期化し、これまでに行った変更を追加してコミットしてください。

```shell
git init
```

つづいて:

```shell
git add .
```

次に以下を実行します:

```shell
git commit -m "first commit"
```

最後に:

```shell
$ git branch -M main
```

それでは最初のコンポーネントを作り始めましょう！
