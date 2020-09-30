# PROTECT
## 環境構築
- Rhinoceros
- ScandyPro

## 作り方
### 頭部の3Dスキャン
- ScandyProで頭部の3Dスキャンを行います
- データを書き出すときはmm OBJ形式で
### Rhinocerosを立ち上げる
- Faceshield.3dmを開く
- CommandのところでGrasshopperと入力しエンターを押すとGrasshopperがたちあがる
- Grasshopperの画面でFile > Open DocumentでFaceshield.ghを開く
### スキャンデータの読み込み
- Rhinocerosの`File > Import` でOBJ形式のスキャンデータを選択します
- ポップアップ画面の設定
### スキャンデータの位置調整
- 右クリック＆
困ったときはCtrl+Z
- `Transform > Move` や `Transform > Rotate` でおでこの中心が原点にくるように位置や向きを調整する
PerspectiveじゃなくてTop/ Front/ Rightで操作するのがおすすめ
### スライダーを調整
- スライダーをドラッグして頭部に合わせる
### STLデータを出力
- Grasshopper上でフレームをBake
- Rhinoceros上でBakeしたフレームを選択してから `File > Export Selected` でSTL形式で書き出し
ファイルの種類はSTL
### 3Dプリント
- CuraでSTLファイルを開く
- Support Blockerを使って前の部分だけInfill Densityを10%にする

## 使い方
