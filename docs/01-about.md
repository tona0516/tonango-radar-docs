---
layout: page
title: TonangoRadarとは
permalink: /about/
nav_order: 1
---

TonangoRadarは、[World of Warships](https://worldofwarships.com/){:target="_blank"}（WoWS）プレイヤー向けのデスクトップアプリケーションです。

![TonangoRadar メイン画面]({{ '/main_page_mosaicked.png' | relative_url }})

## 主な特徴

### マッチ自動検出

マッチ開始時にリプレイファイルを自動検出し、参加プレイヤー全員の戦績を表示します。

### 高速表示

マップ読み込み完了から約5秒でプレイヤーの統計情報が表示されます。

<div class="note" markdown="1">
通信速度やデータ参照元であるWargaming API（以下WG API）のパフォーマンスに影響されます。
</div>

以下の方法で高速な読み込みを実現しています。

- WG APIへの並列リクエスト
- 非戦闘データのキャッシュ
- Go言語によるバックエンド実装

### 多彩な表示項目

そのプレイヤーの平均ダメージやK/Dなどはもちろん、[WoWS Stats & Numbers](https://asia.wows-numbers.com/){:target="_blank"} で採用されているPersonal Ratingや艦種使用割合などの表示に対応しています。

また、項目ごとの表示/非表示とそれらの表示順をカスタマイズすることが可能です。

### チーム比較

味方チームと敵チームの平均値を比較するチーム比較機能があります。

### 艦艇別・全体の統計

艦艇別・全体の統計をそれぞれ確認できます。

### Windows対応

Windowsで動作します。
