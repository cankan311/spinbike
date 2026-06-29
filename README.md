D66-32 Dedicated Blue Route Layer

D66-31ベース。
D66-31で青線が見えなかったため、汎用ID route を信用せず、
アプリ専用の route source/layer を追加して確実に描画する修正版。

修正:
- app-route-source / app-route-progress-source を追加
- app-route-blue-glow / app-route-blue-line を追加
- app-route-progress-green を追加
- これから走る全体ルートは青
- 走った区間は緑
- 旧 route / route-progress は互換用に残すが、表示は app-route-* を使う
- 緑線は青線より細くして、重なっても青線の存在が見えるように調整

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
- JS構文チェック済み
