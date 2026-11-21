# AGENTS.md

このファイルは、AI エージェントが本リポジトリ（`tonango-radar-docs`）で作業する際のガイドラインです。

## プロジェクト概要

World of Warships 向け戦績レーダーアプリ「TonangoRadar」の公式ユーザマニュアルサイトです。

- **技術スタック**: Jekyll (`~> 4.4.1`) + [Just the Docs](https://just-the-docs.com/) テーマ + Ruby（CI 上は `4.0.1`、Bundler 管理）
- **使用プラグイン**: `jekyll-feed`, `jekyll-sitemap`, `jekyll-seo-tag`
- **デプロイ**: `main` ブランチへの push により `.github/workflows/jekyll.yml` が実行され、GitHub Pages へ自動ビルド・デプロイされます
- **公開 URL**: `https://tona0516.github.io/tonango-radar-docs/`（`baseurl: "/tonango-radar-docs"`）

## ディレクトリ・主要ファイル構成

- `index.markdown`: トップページ（`permalink: /`, `nav_order: 0`）。各マニュアルページへの目次を掲載
- `docs/`: マニュアル本文の Markdown ファイル群（番号プレフィックス付き: `01-about.md` 〜 `08-troubleshooting.md`）
- `assets/img/`: スクリーンショットやアイコン等の画像アセット（`.webp` 形式）
- `_data/lucide.yml`: ドキュメント内で使用する Lucide アイコンの SVG パス定義
- `_includes/icon.html`: Lucide アイコンをインライン SVG として描画するパーシャル
- `_includes/title.html`: サイトロゴとタイトル表示のカスタムパーシャル
- `_sass/custom/custom.scss`: Just the Docs 向けのカスタム SCSS
- `_config.yml`: サイト設定・テーマ設定・SEO/OGP デフォルト設定（※変更時はローカルサーバの再起動が必要）
- `Gemfile` / `Gemfile.lock`: Ruby gem の依存関係定義
- `.github/workflows/jekyll.yml`: GitHub Pages ビルド・デプロイ用ワークフロー
- `robots.txt` / `googlefce3fb66e7a7d359.html`: クローラ制御および Google Search Console 所有権確認ファイル（意図なく変更・削除しないこと）
- `_site/`, `.jekyll-cache/`, `.sass-cache/`: ビルド生成物およびキャッシュ（`.gitignore` 対象）

## コマンド・動作確認

```sh
# 依存関係のインストール
bundle install

# ローカル開発サーバ起動（プレビュー確認）
bundle exec jekyll serve

# 本番相当のビルド確認（CI と同等の環境変数）
JEKYLL_ENV=production bundle exec jekyll build
```

> CI と同じ `--baseurl` を明示して確認する場合:
> `JEKYLL_ENV=production bundle exec jekyll build --baseurl "/tonango-radar-docs"`

本リポジトリには自動テストやリンターは設定されていないため、変更後は以下を手動で確認してください。

1. `bundle exec jekyll build`（または `JEKYLL_ENV=production bundle exec jekyll build`）がエラー・致命的な警告なく完了すること
2. 変更・追加したページが `_site/` 配下に期待通りの URL で生成されていること
3. 画像パスや内部リンク・外部リンクに誤りがないこと

## ドキュメント執筆・編集規約

### Front Matter

`index.markdown` および `docs/*.md` の先頭には、以下の Front Matter を記述してください。

```yaml
---
layout: default
title: ページタイトル
description: ページ内容の簡潔な説明（jekyll-seo-tag のメタディスクリプションに使用）
permalink: /slug/
nav_order: 1
---
```

- `docs/` に新規ページを追加する場合は、連番ファイル名（例: `07-new-page.md`）と整合する `nav_order` を設定し、必要に応じて `index.markdown` の目次リストも更新してください。

### リンク・画像・記法

- **内部リンク**: `{{ site.baseurl }}` を使用します（例: `[{% include icon.html name="settings" %} 初期設定]({{ site.baseurl }}/setup/)`）。
- **外部リンク**: Kramdown 属性 `{:target="_blank"}` を付与します（例: `[World of Warships](https://worldofwarships.com/){:target="_blank"}`）。
- **画像**:
  - `assets/img/` 配下に **WebP 形式（`.webp`）** で配置します。
  - 参照時は `relative_url` フィルタを使用します（例: `![説明]({{ '/assets/img/example.webp' | relative_url }})`）。
  - スクリーンショットにプレイヤー名などの個人情報が含まれる場合は、モザイク等のマスキング処理を行ってください。
- **アイコン・文体・装飾**:
  - サイト言語は日本語（`lang: ja-JP`）です。
  - **絵文字は使用しないでください**。見出し（`##` / `###`）やリンク等にアイコンが必要な場合は、`_includes/icon.html` を使って **Lucide** アイコンを挿入します（例: `## {% include icon.html name="sparkles" %} 主な特徴`）。
  - 新しい Lucide アイコンを使う場合は、`_data/lucide.yml` に該当アイコンの SVG 要素を追記してください。
  - 補足や注意事項には Markdown の引用ブロック（`>`）を使用します。

## 変更時の注意事項

- `_site/` や `.jekyll-cache/` などの生成物を Git にコミットしないでください。
- `_config.yml` の `defaults`（デフォルト OGP 画像 `/assets/img/appicon.webp`）や `favicon.ico`、`googlefce3fb66e7a7d359.html`、`robots.txt` など SEO・運用に関わる設定を不用意に壊さないよう注意してください。
- `main` ブランチへの push で本番サイトが更新されます。レイアウトや SCSS（`_sass/custom/custom.scss`, `_includes/title.html`）を変更する場合は `bundle exec jekyll serve` で表示確認を行ってください。
