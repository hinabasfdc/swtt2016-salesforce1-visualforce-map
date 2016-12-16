# Salesforce World Tour Tokyo 2016 セッション9-5 「目から鱗のSalesforce1」 サンプルコード

セッション内で紹介・解説した"手法1: Visualforce:最寄りの取引先を検索し現在位置からのルートを地図で表示する"のサンプルコードです。

## 事前準備

### Salesforce 開発組織の取得

1. 次のリンク先から開発者組織を取得してください。(2016/12時点ではWinter'17)
    1. https://developer.salesforce.com/ja/

### 取引先オブジェクトへの項目追加

1. 取引先オブジェクト(Account)に、緯度経度情報を格納する項目(項目名: Location__c / データ型: 地理位置情報)を追加します。
2. 取引先をいくつか作成し、1.で作成した項目に、緯度・経度を設定します。

### Google MapS APIキーの取得

1. 次のリンク先に従い、キーを取得してください。(2016/12時点)
    1. https://developers.google.com/maps/documentation/javascript/?hl=ja

## 実装方法

1. 新規にAPEXクラス(クラス名: AccountLocation)を作成し、ファイル「AccountLocation.apxc」の内容をコピーペーストして保存してください。
2. 新規にVisualforceページ(表示ラベル&名前: DisplayAccountOnMap)を作成し、ファイル「DisplayAccountOnMap.vfp」の内容をコピーペーストしてください。
3. 123行目にある「[ここをGoogle API Keyに置き換え]」を、事前準備で取得したAPIキーに置き換えてください
4. 「Salesforce モバイルアプリケーションおよび Lightning ページでの使用が可能」オプションのチェックを入れて保存してください。
5. 作成したVisualforceページのタブを作成してください。
6. Salesforce1ナビゲーションで、作成したタブを選択済みにします。

Salesforce1から、この組織にログインし、動作を確認します。

## 免責事項

このサンプルコードは、あくまでSalesforce1における機能利用の1例を示すためのものであり、コードの書き方や特定ライブラリの利用を推奨したり、機能提供を保証するものではありません。
