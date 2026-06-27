# Japan Ride D34 Mapillary Center Search

D34変更点:
- D33の「どこへ行っても画像が出ない」問題への対処版
- 検索対象を仮想自転車位置ではなく、画面中央に変更
- 地図を富士山・箱根・都市部などに動かしてから「画面中央を検索」できる
- 検索範囲を 約1km / 約3km / 約6km から選択
- Mapillary APIの取得フィールドを thumb_original_url に変更
- エラー時のメッセージを詳しく表示

注意:
- Mapillary Client Access Tokenが必要です。
- GitHub Pagesなどhttps配信で検証してください。
- Mapillary画像が少ない場所では約6kmでも出ないことがあります。
