## スキッドステアリングロボット(SSR)のBody data

[inkscape](https://inkscape.org/ja/)で作成したSSR2のsvgファイルです．
inkscapeで開けば編集できます．

線は1.5mmのエンドミルで切り出すことを考えて，1.5mmの太さで描かれています．
svgファイルからpycamなどでngcファイルに変換すると，CNCにかけることができます．

## 材料
部材は5.5mm厚のシナベニアなどがちょうど良いでしょう．
高価ですが，カーボンやアルミの板でも作成可能だと思います．

<img src='https://github.com/HondaLab/2D_OVTurning/blob/main/SSR2.JPG' width=600>

あとは，4mmΦの長ネジで２枚のサイドパネルを連結するだけです．
上部：98mm x 4mmΦ x2本
下部: 135mm x 4mmΦ x2本

## 組み立て
基本構造は，4本の4mmΦ長ネジで左右のサイドパネルを連結するだけです．
底面とインターフェイス基盤の幅が77mmですので，サイドパネルの内ー内間隔を77mmになるように
底面と，インターフェイス基盤を挟み込みます．

下部の２本の長ネジは，ホイールの軸も兼ねます．
軸は固定し回転しません．
18Tギアを通して，ホイールが回転します．

18Tギアは24Tメインギアと勘合しているので，前後のホイールが同時に同じ方向に回転する構造です．

メインギアは連続回転サーボで回転させています．
サーボは直接かんたんにラズパイのGPIOからPWM制御できるので，楽です．
サーボの代わりに，ステッピングモーターなどを用いても良いでしょう．

## インターフェイス基盤にラズパイ
を搭載して，カメラ，センサー，サーボを制御します．
電源はDC-DCコンバータを使って5Vをラズパイに供給します．

サーボには，比較的大きな電流が流れる可能性があるので，ラズパイとは別に5V供給します．

## 旋回機構
左右別々に回転することで，スキッドステアリングする仕組みです．
戦車やバックホウのキャタピラと同じ原理で旋回します．


