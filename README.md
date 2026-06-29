D66-40 State Aware Navigation

D66-39ベース。
日本一周/マイルート切替UIを状態別表示に修正。

修正:
- 日本一周/マイルート切替はルート未選択時だけ表示
- マイルート選択後、走行前、走行中、一時停止、完走では非表示
- 重複していたモード説明行を非表示
- 右上のルート終了とのかぶりを解消
- 切替ボタン自体も小さめに調整

触っていない:
- normalizeSavedRoute
- loadMyRoutes
- editMyRoute
- useMyRoute
- saveDraftRoute

維持:
- 追従ON=現在位置追従+進行方向bearing
- 未走行=青 / 走行済み=緑
- START/GOAL
- 追従ON/OFF
- 手入力スムーズ進行
- 記録保存
- 診断/SV/道に合わせるなし

検証:
- JS構文チェック済み
- headless Chromiumで疑似マイルート一時停止状態のスクリーンショット確認
