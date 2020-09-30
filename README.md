# PROTECT
## 環境構築
- Rhinoceros
- ScandyPro

## 作り方
### 1. 頭部の3Dスキャン
- ScandyProで頭部の3Dスキャンを行います
- データを書き出すときはmm OBJ形式で

### 2. RhinocerosとGrasshopperを立ち上げる
- Faceshield.3dmを開く
- CommandのところでGrasshopperと入力しエンターを押すとGrasshopperがたちあがる
- Grasshopperの画面で`File > Open Document`でFaceshield.ghを開く

### 3. スキャンデータの読み込み
- Rhinocerosの`File > Import` でOBJ形式のスキャンデータを選択します
- ポップアップ画面の設定

### 4. スキャンデータの位置調整
- `Transform > Move` や `Transform > Rotate` でおでこの中心が原点にくるように位置や向きを調整する
  - このときPerspectiveじゃなくてTop / Front / Rightの画面で操作するのがおすすめ
- 基本的な操作
  - 右クリック＆ドラッグで3D回転
  - Shift+右クリックで移動
  - マウスホイールで拡大縮小
  - 困ったときはCtrl+Z

### 5. スライダーを調整
- スライダーをドラッグしてパラメータの値を変えるとフレームの形が変わる
- 頭部にフィットするまで調整する

### 6. STLデータを出力
- Grasshopper上でAllと書かれたBrepをBake
- Rhinoceros上でBakeされたフレームを選択してから `File > Export Selected` で書き出し
  - ファイルの種類はSTL

### 7. 3Dプリント
- CuraでSTLファイルを開く
- Support Blockerを使って前の部分だけInfill Densityを10%にする

## 使い方
