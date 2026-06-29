D66-22 Route Data Diagnostics

D66-21ベース。
今回触ったのは「保存済みルートの診断表示」だけ。
- 保存済みルート一覧に「診断」ボタンを追加
- localStorage内のrawデータと正規化後データを比較表示
- points / waypoints / route / coords / coordinates / geometry など候補ごとの座標数を表示
- 診断内容をコピー可能
- ルート編集、走行、保存処理自体は変更しない
- 道に合わせる無し、SVなし状態は維持
- JS構文チェック済み
