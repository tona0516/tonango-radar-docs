---
layout: page
title: TonangoRadarとは
permalink: /about/
nav_order: 1
---

TonangoRadarは、[World of Warships](https://worldofwarships.com/){:target="_blank"}（WoWS）プレイヤー向けのデスクトップアプリケーションです。マッチ中のプレイヤー戦績をリアルタイムで確認でき、より戦略的なプレイを実現します。

![TonangoRadar メイン画面]({{ '/main_page_mosaicked.png' | relative_url }})

## ✨ 主な特徴

### 🔍 マッチ自動検出

マッチ開始時にリプレイファイルを自動検出し、参加プレイヤー全員の戦績を表示します。手動操作は不要で、ゲームの邪魔になりません。

### ⚡ 高速表示

マップ読み込み完了から**6~7秒**でプレイヤーの統計情報が表示されます。

> ※通信速度やデータ参照元であるWargaming API（以下WG API）のパフォーマンスに影響されます。

以下の技術で高速な読み込みを実現しています。

- **WG APIへの並列リクエスト** — 複数のAPIコールを同時に実行
- **非戦闘データのキャッシュ** — 取得済みデータを再利用
- **Go言語によるバックエンド実装** — 高い並行処理性能

### 📊 多彩な表示項目

そのプレイヤーの平均ダメージやK/Dなどはもちろん、[WoWS Stats & Numbers](https://asia.wows-numbers.com/){:target="_blank"} で採用されているPersonal Ratingや艦種使用割合などの表示に対応しています。

また、項目ごとの**表示/非表示**とそれらの**表示順**をカスタマイズすることが可能です。

### ⚔️ チーム比較

味方チームと敵チームの平均値を比較するチーム比較機能があります。PR、ダメージ、勝率、戦闘数をグラフで一目瞭然に確認できます。

![TonangoRadar チーム比較]({{ '/team_average.png' | relative_url }})

### 📈 艦艇別・全体の統計

艦艇別・全体の統計をそれぞれ確認できます。プレイヤーの得意な艦艇をすばやく把握できます。

### 🖥️ Windows対応

Windowsで動作します。
