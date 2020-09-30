# PROTECT
## 概要
- 頭の形に合わせてカスタマイズできるフェイスシールド
- [note](https://note.com/fm_protect)

## 環境構築
- [Rhinoceros](https://www.rhino3d.co.jp/)
  - フェイスシールドのフレームの形状をカスタマイズするのに使うCADソフト
  - このソフトに搭載されているGrasshopperを用いてビジュアルプログラミングしている
- [ScandyPro](https://www.scandy.co/apps/scandy-pro)
  - iPhoneやiPadで頭部のスキャンをするときに使うアプリ

## 作り方
### 1. 頭部の3Dスキャン
- ScandyProで頭部の3Dスキャンを行う
- データを書き出すときはmm，OBJ形式で

### 2. ファイルを開く
- このGithubのリポジトリをダウンロードする
- Faceshield.3dmをダブルクリックして開くとRhinocerosが起動する
- 左上のCommandのところにGrasshopperと入力しエンターを押すとGrasshopperが起動する
- Grasshopperの画面で`File > Open Document`でFaceshield.ghを開く

### 3. スキャンデータの読み込み
- **Rhinoceros** `File > Import` でOBJ形式のスキャンデータを選択
  - ポップアップ画面（OBJ Import Options）の設定は
    - Import OBJ groups as: Object names
    - [x] Import OBJ objects
    - [ ] Import as morph target only
    - [ ] Reverse group order
    - [ ] Ignore textures
    - [x] Map OBJ Y to Rhino Z
    - [ ] Split 32-bit textures into separate files

### 4. スキャンデータの位置調整
- **Rhinoceros** `Transform > Move` や `Transform > Rotate` でおでこの中心が原点にくるように位置や向きを調整する
  - このときPerspectiveじゃなくてTop / Front / Rightの画面で操作するのがおすすめ

### 5. スライダーを調整
- スライダーをドラッグしてパラメータの値を変えるとフレームの形が変わる
- 頭部にフィットするまで調整する

### 6. STLデータを出力
- **Grasshopper** Allと書かれたBrepをBake
- **Rhinoceros** Bakeされたフレームを選択してから `File > Export Selected` で書き出し
  - ファイルの種類はSTLを選択

### 7. 3Dプリント
- CuraでSTLファイルを開く
- Support Blockerを使って前の部分だけInfill Densityを10%にする

## 使い方
- ゴムを2本取り付ける
