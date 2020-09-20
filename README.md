# PROTECT
## 環境構築
- Rhinoceros
- ScandyPro

## 作り方
### 頭部の3Dスキャン
- ScandyProで頭部の3Dスキャンを行います
- データを書き出すときはmm OBJ形式で
### スキャンデータの読み込み
- `File > Import` でOBJ形式のスキャンデータを選択します
### スキャンデータの位置調整
- `Transform > Move` や `Transform > Rotate` でおでこの中心が原点にくるように位置や向きを調整する
### アプリを開く
- 別ウィンドウ
### スライダーを調整
- スライダーをドラッグして頭部に合わせる
### STLデータを出力
- Grasshopper上でフレームをBake
- Rhinoceros上でBakeしたフレームを選択してから `File > Export Selected` でSTL形式で書き出し
### 3Dプリント

## 使い方
