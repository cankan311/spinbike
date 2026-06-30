D66-56 BLE Sensor Diagnostic

D66-55ベース。
設定画面にケイデンス/スマートバイク用のBluetooth診断画面を追加。

目的:
- 本番走行に組み込む前に、センサーがどんな形式でデータを出しているか確認する
- メーカー差・機種差でアプリが落ちないように、読めるものだけ読む
- まだ走行速度/RPMには反映しない

対応診断:
- Cycling Speed and Cadence Service
  - service 0x1816
  - CSC Measurement 0x2A5B
  - 累計クランク回転数とイベント時刻差分からRPM計算
  - wheelデータがあれば速度も参考計算
- Fitness Machine Service / Indoor Bike Data
  - service 0x1826
  - Indoor Bike Data 0x2AD2
  - rpm / speed / power / heart rateを読める範囲で表示
- Cycling Power
  - service 0x1818
  - Cycling Power Measurement 0x2A63
  - power / crank revolution dataがあればRPM計算
- Battery
  - service 0x180F
  - Battery Level 0x2A19
- Device Information
  - service 0x180A
  - Manufacturer / Model
- 未知の形式
  - エラーにせずRaw HEXログに表示

UI:
- 設定 > ケイデンス診断
- センサー接続
- 切断
- ログ消去
- RPM / 速度 / Power / HR / 電池 / 最終受信
- 接続デバイス
- 検出サービス
- Raw HEXログ最新20件

安全策:
- 本番走行にはまだ反映しない
- st.rpmへ代入しない
- 走行ロジック・保存/読込/編集・追従・地図描画には触らない
- D66-48/D66-49の失敗CSSは含めない

検証済み:
- JS構文チェック
- 診断UI存在
- CSC / FTMS / Cycling Power / Battery / Device Info UUID存在
- Raw HEX表示ロジック存在
- D66-56追加部で保存/読込/編集系関数を上書きしていない
- st.rpmへ代入しない
- D66-55の丸みフォント維持
- 追従bearing仕様、青/緑split仕様、追従ON/OFF、START/GOAL仕様が残っている

未検証:
- 実機Android Chrome + センサー接続
- センサーごとの通知データ実測
