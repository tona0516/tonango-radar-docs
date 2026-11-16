---
layout: default
title: インストール・アップデート
description: TonangoRadarの動作環境、Windows向け新規インストール手順、およびアプリ内自動アップデート手順を説明します。
permalink: /install/
nav_order: 2
---

## 💻 動作環境

| 項目 | 要件 |
|------|------|
| OS | Windows 11 x64 |
| World of Warships クライアント | Game Center もしくは Steam 経由でのインストール |
| その他 | インターネット接続 |

## 🚀 新規インストール手順

1. [ダウンロードページ（Google Drive）](https://drive.google.com/drive/folders/1CoVadYdK-zhtJcM2-O9qBCmRSSbC_dLm?usp=sharing){:target="_blank"}を開き、最新版のインストーラ（`TonangoRadar-vX.Y.Z-amd64-installer.exe`）をダウンロードします
2. ダウンロードしたインストーラを実行します
3. 画面の指示に従いインストールを完了してください
4. インストール完了後、デスクトップにショートカットが作成されます

![TonangoRadar ショートカット]({{ '/assets/img/shortcut.webp' | relative_url }})

## 🔄 アップデート手順

### アプリ内自動アップデート（推奨）

新しいバージョンが公開されると、アプリ起動時にバックグラウンドで確認が行われます。

![新バージョン通知バナー]({{ '/assets/img/new_release.webp' | relative_url }})

1. 左端サイドメニューの「**設定**」アイコンに赤い通知バッジが表示されます
2. 「設定」画面を開くと、上部に「**新しいバージョン X.Y.Z が利用可能です。**」という通知バナーが表示されます
3. 「**今すぐ更新**」ボタンをクリックします
4. 最新版のダウンロードおよびチェックサム（SHA-256）検証が完了すると、アプリが一度終了し、自動で最新版へ置き換わって再起動します

> 更新中にエラーが発生した場合や手動で入れ直したい場合は、バナー内の「ダウンロードページを開く」からインストーラを取得して上書きインストールすることも可能です。

---

インストールが完了したら、次は[⚙️ 初期設定]({{ site.baseurl }}/setup/)を行いましょう。
