D66-37 Pre Ride Preview UI

D66-36ベース。
今回の修正対象:
- マイルート選択直後の走行前プレビューUI整理。

追加:
- 「これから走るルート」カード
- ルート名
- 総距離
- チェックポイント数
- 青=これから走る道
- 緑=走った道
- 追従ON=進行方向に地図が向く
- START/GOAL確認後にスタートする案内

表示条件:
- my-route-active + my-route-ready の走行前だけ表示
- 走行中/一時停止/完走/地図ビュー/簡易表示では非表示

仕様台帳で守ったこと:
- 追従ON = 現在位置を追う + 進行方向に地図を向ける
- 追従OFF = 中心も向きも勝手に動かさない
- 未走行区間 = 青
- 走行済み区間 = 緑
- ペダル+/- = RPM変更。距離追加ではない
- マイルート選択直後は走行前
- 走行前にルート全体を確認できる
- START/GOAL表示は維持
- 診断UI、SV、道に合わせるボタンを戻さない

触っていない:
- normalizeSavedRoute
- loadMyRoutes
- editMyRoute
- useMyRoute
- saveDraftRoute

検証済み:
- JS構文チェック
- 走行前カードDOM存在
- 走行前ready時だけ表示するCSS存在
- ルート名/距離/CP数更新関数存在
- D66-37追加ブロック内で保存/読込/編集系関数を上書きしていない
- 追従bearing仕様、青/緑split仕様、追従ON/OFFボタン、START/GOAL仕様が残っていること
- 表示値生成の簡易セルフテスト

未検証:
- 実機Galaxy + GitHub Pages上でのMapLibre実描画
