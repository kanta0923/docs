# AmiraでOrthoslice動画を作成する方法

AmiraでOrthosliceのアニメーションを作成し，動画として書き出すまでの流れ

## 1. 起動とデータの読み込み

1. Amiraを起動する．  
2. File > Open Data からデータを読み込む．  

---

## 2. 表示設定（VolrenとOrthoslice）

1. データを選択してVolrenを追加する．  
2. Orthosliceを追加する．  
3. Orthosliceのプロパティで以下を設定する  
   - X / Y / Z のどの断面を表示するか  
   - Slice Number  

4. Volrenと併用している場合  
   - スライスの前後どちらのボリュームを表示するか切り替え可能  

---

## 3. Animation Directorを開く

1. 上部のAnimationタブを開く  
2. 下部にタイムライン（Animation Director）を表示する  

---

## 4. 動画全体の範囲を設定する

1. タイムライン右端のスライダーを調整  
2. 開始フレームと終了フレームを決める  

---

## 5. キーフレームの設定（Orthoslice）

1. 開始位置に移動  
2. Slice Numberを設定  
3. プロパティ項目名の左にある時計マークをクリック  

4. 終了位置に移動  
5. Slice Numberを変更  
6. 同様に時計マークをクリック  

→ スライスが連続的に移動する  

---

## 6. プレビュー

再生ボタンで動作確認  

---

## 7. 画像として書き出す

1. Movie Creationを開く  
2. 画像シーケンス（PNG / TIFF）で出力  
3. 書き出し実行  

※動画として直接出力せず，画像で出す方が良い  

---

## 8. 動画化（Desktop / Yeti）

DesktopにあるYetiアプリから画像列を動画に変換する  

---

# 応用

## 複数スライスの組み合わせ

1つのOrthosliceだけでなく，複数を組み合わせてアニメーション可能  

例  
- 前からスライス → 横からスライス  
- X断面 → Z断面  

方法  
- Orthosliceを複数追加  
- それぞれにキーフレームを設定  
- 表示ON/OFFやSlice Numberを時間で切り替える  

---

## カメラとアニメーションの考え方

ビューワ上でマウス操作しただけではアニメーションには反映されない  

表示されているのは「カメラを通した映像」と考える  

- カメラを動かす  
- または物体を動かす  

ことでアニメーションを作る  

---

## カメラ回転（Camera Orbit）

1. Project Viewで右クリック → Create Object  
2. Camera-Orbitを追加  
3. Timeスライダーで回転を確認  
4. 必要に応じて回転軸を変更  
5. 設定後はrecomputeを押す  
6. Timeスライダーの値で時計マークを押し，開始・終了を登録  

---

## カメラ移動（Camera Path）

1. Create Object → Camera Path  
2. カメラボタンを押す  
3. 始点を決めてadd  
4. 次の位置を決めてadd  
5. これを繰り返す  
6. Time値をタイムラインに追加  

※時間の配置で移動速度を調整できる  

---

## 物体の回転

1. データを右クリック → Geometry Transforms > Rotate  
2. Timeスライダーで回転を確認  
3. Axisで回転軸を設定（100=X, 010=Y, 001=Z）  
4. Centerで回転中心を設定  
5. 時計マークでキーフレーム登録  

---

## 物体の移動

1. Geometry Transforms > Translate  
2. Start Point / End Pointを設定  
3. Timeスライダーで確認  
4. 時計マークでキーフレーム登録  

---
