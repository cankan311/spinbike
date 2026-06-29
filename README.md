D66-33 Split Route Colors

D66-32ベース。
青/緑の考え方を修正。
全体青の上に緑を重ねる方式ではなく、現在位置でルート座標を2分割する。

仕様:
- スタート → 現在位置: 緑
- 現在位置 → ゴール: 青
- 走行前: 全ルート青、緑なし
- 走行中: 後ろが緑、前が青
- 完走後: 全ルート緑、青は終点だけ

実装:
- routeSplitAtDistance() を追加
- app-route-future-source / app-route-passed-source を追加
- app-route-future-blue / app-route-passed-green を追加
- 旧 route / route-progress / D66-32の app-route-blue-line は非表示にして干渉防止

検証:
- JS構文チェック済み
- routeSplitAtDistance の分割テスト済み
- passed の終点と future の始点が一致することを確認
- self-test画像同梱

触っていない:
- normalizeSavedRoute
- loadMyRoutes
- editMyRoute
- useMyRoute
- saveDraftRoute

維持:
- スムーズ進行
- 自動追従
- 走行前スタート状態
- 記録保存
- チェックポイント表示/到達演出
- 診断ボタンなし
- 道に合わせる無し
- SVなし
- 初倉駅の固定文言なし
