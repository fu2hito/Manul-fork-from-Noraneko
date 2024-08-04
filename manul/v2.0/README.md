# Manul

![Manul v2 image](https://github.com/user-attachments/assets/2e5e5e20-1b11-458e-8fc0-289e18aa9af1)

ManulはNoraneko42GRをベースにした42キーのGRINレイアウトキーボードです。Lofree Ghostスイッチの利用を前提としたChoc v2ソケット対応です。

## パーツ

* PCB --- 1枚
* アクリルプレート トップ --- 1枚
  * PCBより上
  * 2 mm
* アクリルプレート ボトム1 --- 2枚
  * PCBより下
  * 2 mm
* アクリルプレート ボトム2 --- 1枚
  * PCBより下
  * 2 mm
* M2スペーサー 3mmまたは3.5mm --- 7個
* M2ネジ 3mm --- 14個
* RP2040-Zero --- 1個
* コンスルー --- 18ピン（MAC8 XB-3 高さ3mm以上）
  * ピンヘッダ
  * 干渉を避けるためカットします
* 1N4148W --- 42個
* WS2812B --- 6個
* SK6812MINI-E --- 42個
* Choc V2スイッチ --- 42個
  * アクリルプレート ボトム1が干渉するため、一部のピンの多いChoc V2スイッチは利用できません
* MXキーキャップ（ロープロファイルがおすすめ） --- 42個
* ゴム足 --- 任意の数

## ファームウェア

手順はNoraneko42GRと[同様](./README.original.md)です。Manulには抵抗はありません。

* [ファームウェア](./firmware/manul/)
  * WIP: ビルド済みファイルはアップロードしていません。
* [Vialサポート](https://get.vial.today/)

## はんだ付け

はんだ付けはNoraneko42GRと[同様](./README.original.md)です。Manulには抵抗がありません。

RP2040-Zero、ダイオード、LED、ソケットをはんだ付けします。
いずれもはんだ付けの向きに注意してください。

## 組み立て

1. アクリルプレート トップと一緒にスイッチをPCBに取り付けます。
2. M2スペーサーを取り付けます。まずトップ側にネジ止めします。
3. アクリルプレート ボトム1を取り付けます。ボトム1は2枚使用します。
4. アクリルプレート ボトム2を取り付けます。
5. ネジを取り付けます。
6. アクリルプレート ボトム2にゴム足を取り付けます。

## PCB、アクリルプレートの発注について

PCBは[JLCPCB](https://jlcpcb.com/jp)、アクリルプレートは[Elecrow](https://www.elecrow.com/)で製造したもので動作確認しました。

[PCB](./pcb/)の発注方法は[JLCPCBのFAQ](https://jlcpcb.com/help/article/how-to-generate-gerber-and-drill-files-in-kicad-7)を参考にしてください。

アクリルプレートは[plate](./plate/)のpdfとsvgをzipファイルにしてElecrowにアップロードして発注できます。
