# schfeslog

スマートフォンゲーム「ラブライブ! スクールアイドルフェスティバル」のログを取るためのHTTPプロキシです。

ライブの戦績を読み取って、自動でログ出力したりツイートしたりします。他の機能も追加予定。

(**自己責任で使用してください。**)

## バージョン

v1.1.4

## 注意点

1. 曲情報はそのIDでしか推測できないため、そのIDに該当する曲の曲名をdata.jsonで管理しています。まだ登録されていない場合は、そのままのIDが出力されます。もしdata.jsonをそれなりに埋めてくださったなら、Pull Requestを出してくれると喜びます。

2. スクフェス利用以外の通信も全て通るようにしてありますので、非推奨ですが、常時接続でも(エラーが出て停止しなければ)問題ない作りになっています。

3. 何の認証も用意していませんので、プロキシサーバーと同一ネットワークにいる他の人がこのプロキシサーバーに接続してスクフェスをプレイした時も、同様にツイートされます。自分しか利用しないことが確実なネットワーク上で走らせ、その外で利用したい場合は適宜VPNを挟むなどしてください。

## 使い方

### 初期設定

1. `npm install`
2. `cp settings-sample.json settings.json`
3. settings.json内のTwitterの項目を適する形で上書きします。
4. ポート番号を変更したい場合、settings.json内のportの値を上書きします。デフォルトは25252になっています。

### プレイ時

1. `node main.js`
2. nodeを走らせているサーバーのアドレスとポート番号をスクフェス端末のOSのプロキシ設定に指定。
3. スクフェスをプレイ!

## 追加予定機能

* 認証機能
* ツイートへのリプライによる手動曲名登録
* ストーリーの保存
* 部員勧誘の結果の取得
* LPの状態の取得

## 連絡先

* E-mail: contact@hideo54.com
* Twitter: @hideo54
