# Japan Ride D36 Mapillary Button Fix

D36変更点:
- D35で「画面中央を検索」ボタンが反応しない問題への対処
- ボタンに inline onclick を追加して、Android Chromeでも確実に関数を呼ぶ
- 「保存して検索」と「画面中央を検索」は同じ処理に統一
- Token欄が空なら、必ず「Token未入力」と画面に反応表示
- Token入力済みなら保存して検索
- window関数として mlySaveTokenAndSearch / jumpAndSearch / nextMly を公開

注意:
- スクショの状態ではToken欄が空なので、Mapillary画像は取得できません。
- ただしD36ではToken未入力でもボタン反応が画面に出ます。
