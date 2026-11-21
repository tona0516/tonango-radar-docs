source "https://rubygems.org"
# ここでは実行に使用する Jekyll のバージョンを管理します。
# 別のバージョンを使いたい場合は、以下の指定を変更してファイルを保存し、
# `bundle install` を実行してください。Jekyll は次のように `bundle exec` 経由で実行します:
#
#     bundle exec jekyll serve
#
# これにより、適切なバージョンの Jekyll が確実に実行されます。
gem "jekyll", "~> 4.4.1"
# ドキュメント用テーマ
gem "just-the-docs"
# GitHub Pages 用 gem を使う場合は、上の `gem "jekyll"` を削除して
# 次の行のコメントアウトを解除してください。アップグレードするには `bundle update github-pages` を実行します。
# gem "github-pages", group: :jekyll_plugins
# プラグインを追加する場合はここに記述してください
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

# Windows および JRuby には zoneinfo ファイルが含まれないため、
# tzinfo-data gem と関連ライブラリをバンドルします。
platforms :windows, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Windows 環境でのディレクトリ監視を高速化する gem
gem 'wdm', '>= 0.1.0', platforms: [:windows, :jruby]

# JRuby ビルドでは `http_parser.rb` の新しいバージョンに Java 版が存在しないため、
# `v0.6.x` に固定します。
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
