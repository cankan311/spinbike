D66-21 Saved Route Normalize Fix

D66-20ベース。
今回触ったのは「保存済みルートの読み込み・保存データ正規化」だけ。
- 編集時に保存済みルートの点列を確実に復元
- points / waypoints / route / coords / coordinates / geometry など複数形式から座標を拾う
- 既存保存データを loadMyRoutes 側で正規化
- 一覧の地点数も正規化後の点数で表示
- 編集保存時は既存ルートを上書き
- このルートを走る側も正規化済み points を使う
- 道に合わせる無し、SVなし状態は維持
- JS構文チェック済み
