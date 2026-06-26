# Japan Ride D31 Terrain Terrarium Fix

D31変更点:
- D30の地形3Dが真っ平らに見える問題を修正
- 地理院 dem_png + encoding:gsi をやめる
- MapLibreが直接読める Mapzen Terrarium DEM を raster-dem source として使用
- 地形ON: map.setTerrain({ source: 'terrain-dem', exaggeration: 1.8 })
- 地形OFF: map.setTerrain(null)
- 建物OFF/ONはD29/D30のまま維持
- 初期状態は 建物OFF / 地形OFF

GitHub Pagesでは `index.html` を公開してください。
