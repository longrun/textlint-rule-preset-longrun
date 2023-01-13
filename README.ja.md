# textlint-rule-preset-longrun

ロンランでさまざまな記事を執筆してゆくうえでの校正ルールです。

- 技術ブログ記事用の基本プリセット
- GitHub Actions / reviewdog による自動校正設定
- [prh/rules](https://github.com/prh/rules) を Git submodule として取り込んで直接利用しています

# How to setup

```
npm install
```

記事は `articles/` 配下に配置されることを想定しています。

# GitHub Actions / reviewdog による自動校正を有効にするには

ファイル名 `.github/workflows/lint.yml.sample` を `.github/workflows/lint.yml` に変更します。

上記設定では `articles/*` 配下のファイルを対象としていますが、必要に応じて適宜変更してください。

# Usage proofreading of text

特に何もしなくても、VScode エディタ上で自動校正されます。手動で実行したい場合は、次のコマンドで実行できます。

```
npx textlint articles/filename.md
```

# Reference

- https://github.com/prh/rules
- [テックブログの校正を支える技術 textlint とルール設定について](https://zenn.dev/offers/articles/20220512-awesome-texlint-correction)
- [【GitHub Actions】Markdown 執筆に textlint の自動校正を取り入れる](https://dev.classmethod.jp/articles/markdown-writing-with-textlint-ci/)
- [文章校正を行うための textlint 入門](https://ics.media/entry/220404/)
- [textlint を使っている企業の事例・ルールをまとめてみた](https://zenn.dev/kgsi/articles/a88273d293abe07c5acb)
