# GooglePlaceAPIMock
これはGoogle Place APIを使用したサンプルのモックアプリです。
GooglePlaceAPIを実装してAPIの使用方法や使い勝手を確認するために作成したものです。
どなたかの参考になれば幸いです。

##使い方

1.pods installをしてGoogle MapsとPlaces APIのライブラリをインストールします。
2.workspaceファイルが作成されるので、Xcodeを開いている場合は、閉じてからworkspaceを開きます。
3.Google Maps APIのAPIキーをAppDelegateのAPI KEYの指定の箇所に設定します。
4.SearchResultsController.swiftのtableView didSelectRowAtの中で実行しているジオコードAPIのURLにもAPI KEYを設定します。
4.ビルド

実装している内容は下記です。

###マップ1
・現在地を取得して表示
・周辺のスポットをピンで表示

###検索1
・検索バーとオートコンプリートの表示
・検索結果をタップしてもマップは表示されません。
※GMSAutocompleteViewControllerをGoogle Maps APIのドキュメント通りに実装しています。
[詳細はこちら](https://developers.google.com/places/ios-sdk/reference/interface_g_m_s_autocomplete_view_controller)

###検索2
・地図の表示
・オートコンプリートの表示(自前)
・検索結果のリストタップで該当の位置にピン追加

こちらは※GMSAutocompleteViewControllerではなく、GMSAutocompleteFetcherを使用して、検索結果を表示しています。
また、位置の算出はジオコードAPIを使用して取得しています。




