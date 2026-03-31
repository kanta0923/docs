# AmiraでOrthoslice動画を作成する方法

AmiraでOrthosliceのアニメーションを作成し，動画として書き出すまでの流れ

## 1. Amiraの起動

1. デスクトップ上のAmiraアイコンをダブルクリックして起動する．

## 2. ファイルを読み込む

1. メニューバーから **File > Open Data** を選択する．
2. 読み込みたいデータを選択して開く．

## 3. Orthosliceを表示する

1. 読み込んだデータをProject Viewで選択する．右クリックでメニュー表示，Orthosliceを選択（オレンジ色）
2. Orthosliceが作成される．
3. Orthosliceのプロパティで，表示方向や `Slice Number` を調整する．


## 4. アニメーション編集画面を開く

1. 画面上部の **Animation** タブをクリックする．
2. ビューワ下部に **Animation Director** を表示する．

Animation Directorは，タイムライン上でイベントやキーフレームを追加しながらアニメーションを作成する画面である．ストップウォッチアイコンを使って，各モジュールやパラメータの変化を時間軸に登録できる．:contentReference[oaicite:3]{index=3}

## 5. キーフレームを挿入する

### 5.1 開始フレームを設定する

1. Animation Directorの時間カーソルを開始時刻に合わせる．
2. Orthosliceのプロパティで `Slice Number` を開始したい値に設定する．
3. `Slice Number` の左にあるストップウォッチアイコンをクリックして，開始キーフレームを登録する．

### 5.2 終了フレームを設定する

1. Animation Directorの時間カーソルを終了時刻に移動する．
2. `Slice Number` を終了したい値に変更する．
3. 再びストップウォッチアイコンをクリックして，終了キーフレームを登録する．

これにより，開始時刻から終了時刻までの間で `Slice Number` が連続的に変化し，断層が移動するアニメーションになる．AmiraのAnimation Directorでは，時間カーソルを動かしてイベントトラックにキーフレームを追加し，必要に応じて編集できる．:contentReference[oaicite:4]{index=4}

## 6. プレビューする

1. Animation Directorの再生ボタンを押す．
2. Orthosliceが意図した通りに切り替わるか確認する．
3. 必要に応じてキーフレームの時刻や `Slice Number` を調整する．

Animation Directorには，再生，前後のイベントへの移動，タイムラインのズームやパンなどの操作が用意されている．:contentReference[oaicite:5]{index=5}

## 7. 動画を書き出す

1. Animation Directorで書き出したい時間範囲を確認する．
2. **Movie Creation** ボタンをクリックして，Movie Maker画面を開く．
3. 出力形式，保存先，フレーム数，画像サイズなどを設定する．
4. `Create Movie` を実行して書き出す．

Thermo Fisherのリリースノートでは，Animation Directorから **Movie Creation** を切り替えてMovie Makerインターフェースを開き，ムービーを書き出す流れが案内されている．:contentReference[oaicite:6]{index=6}

## 8. まとめ

AmiraでOrthoslice動画を作る基本フローは，以下の通りである．

1. Amiraを起動する  
2. `File > Open Data` からデータを読み込む  
3. Orthosliceを表示する  
4. `Animation` タブを開いてAnimation Directorを表示する  
5. `Slice Number` に開始・終了のキーフレームを入れる  
6. 再生して確認する  
7. `Movie Creation` から動画を書き出す
