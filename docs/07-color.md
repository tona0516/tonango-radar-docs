---
layout: default
title: 表示色について
description: Personal Rating（PR）・ダメージ・勝率・プレイヤー名のレーティング別カラーコードとしきい値、およびクランタグ・バーチャートの配色ルールを掲載します。
permalink: /color/
nav_order: 7
---

# 表示色について

## {% include icon.html name="target" %} レーティング別の文字色・しきい値

以下の項目は、しきい値に基づいて8段階のレーティングカラーで色分け表示されます。

- [Personal Rating - WoWS Stats & Numbers](https://asia.wows-numbers.com/personal/rating){:target="_blank"}（艦成績・総合成績）
- ダメージ（**艦成績のみ**。サーバー期待値ダメージに対する比率で判定）
- 勝率（艦成績・総合成績）
- プレイヤー名（[{% include icon.html name="sliders-horizontal" %} 表示設定]({{ site.baseurl }}/settings/) で「文字色タイプ」を `艦成績のPR` または `総合成績のPR` に設定した場合）
- 艦艇詳細モーダルの「目安ダメージ一覧表」（各艦のサーバー期待値から算出した基準ダメージ）

### レーティング・文字色・しきい値の対応表

各値がしきい値**以上**であれば、そのレーティングに分類されます。

| レーティング | 色 | 基準カラーコード | PR | 平均ダメージ比 | 勝率 (%) |
|:---|:---:|:---:|---:|---:|---:|
| Super Unicum | <span style="color: #A00DC5">■</span> | `#A00DC5` | 2450 | 1.6 | 65 |
| Unicum | <span style="color: #D042F3">■</span> | `#D042F3` | 2100 | 1.5 | 60 |
| Great | <span style="color: #02C9B3">■</span> | `#02C9B3` | 1750 | 1.4 | 56 |
| Very Good | <span style="color: #318000">■</span> | `#318000` | 1550 | 1.2 | 54 |
| Good | <span style="color: #44B300">■</span> | `#44B300` | 1350 | 1.0 | 52 |
| Average | <span style="color: #FFC71F">■</span> | `#FFC71F` | 1100 | 0.8 | 50 |
| Below Average | <span style="color: #FE7903">■</span> | `#FE7903` | 750 | 0.6 | 47 |
| Bad | <span style="color: #FE0E00">■</span> | `#FE0E00` | 0 | 0 | 0 |

> **{% include icon.html name="sun-moon" %} テーマに応じた自動明暗調整について**  
> 実際のアプリ画面では、選択中の配色テーマ（`dark` / `light`）の背景に対して文字が読みやすくなるよう、上記の基準カラーコードから自動で明るさ（`dark`時は明るく、`light`時は暗く）が調整されて表示されます。

## {% include icon.html name="tag" %} クランタグ・バーチャートの配色

- **クランタグ**：クラン戦の所属リーグに基づく色（ゲーム内表示準拠）が適用されます（テーマに応じた明暗調整あり）。
- **艦種比バーチャート**：左から以下の色で割合を表示します。
  - <span style="color: #233B8B">■</span> 潜水艦（`#233B8B`） / <span style="color: #D9760F">■</span> 駆逐艦（`#D9760F`） / <span style="color: #27853F">■</span> 巡洋艦（`#27853F`） / <span style="color: #CA1028">■</span> 戦艦（`#CA1028`） / <span style="color: #5E2883">■</span> 空母（`#5E2883`）
- **Tier帯比バーチャート**：左から以下の色で割合を表示します。
  - <span style="color: #8CA113">■</span> Tier 1〜4（`#8CA113`） / <span style="color: #205B85">■</span> Tier 5〜7（`#205B85`） / <span style="color: #990F4F">■</span> Tier 8〜★（`#990F4F`）
