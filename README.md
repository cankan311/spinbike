D66-35 Auto Follow Bearing

D66-34ベース。
自動追従ON時に、地図の向きも進行方向へ合わせる修正。

修正:
- routeHeadingAtDistance() を追加
- 現在位置から少し先のルート点を見て進行方向bearingを計算
- 追従ON中は center + bearing を更新
- 追従OFF中は中心も向きも勝手に動かさない
- 再センター「⌖」や追従ON復帰時も進行方向へ向きを合わせる
- 走行前もスタート方向へ向ける

検証:
- JS構文チェック済み
- bearing計算の東西南北セルフテスト済み
- D66-35追加ブロック内で保存/読込/編集系関数を上書きしていない

触っていない:
- normalizeSavedRoute
- loadMyRoutes
- editMyRoute
- useMyRoute
- saveDraftRoute

維持:
- 追従ON/OFFボタン
- 未走行=青 / 走行済み=緑
- スムーズ進行
- 記録保存
- チェックポイント表示/到達演出
- 診断ボタンなし
- 道に合わせる無し
- SVなし
- 初倉駅の固定文言なし
