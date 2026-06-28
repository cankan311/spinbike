D72 Remove SV Restore Map View

D71の即時修正。
- SVを完全削除
- 余計な常時「詳細表示」ボタンを削除
- 表示切替は 詳細表示 → 簡易表示 → 地図ビュー → 詳細表示
- 詳細/簡易では上部の表示切替ボタンを維持
- 地図ビューでは地図操作パネル内の「詳細表示」で戻る
- 建物/地形ON/OFFは地図ビュー内に残す
- JS構文チェック済み
- HTML内に svBtn / SV OFF / SV ON / alwaysDetailBtn が残っていないことを確認
