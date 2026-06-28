D66-2 Real 3D Building/Terrain

D66-1ベース。
今回の修正対象は「地図操作内の建物/地形ON/OFFを、過去版と同じ本物の3D処理に戻す」だけ。
- D30-D32で使っていた MapLibre + OpenFreeMap fill-extrusion を復元
- D30-D32で使っていた raster-dem + map.setTerrain を復元
- D66-1のCSSオーバーレイ式の偽物は廃止
- 地図操作パネル内の「建物 ON/OFF」「地形 ON/OFF」で実行
- SVは地図操作パネルに追加していない
- JS構文チェック済み
