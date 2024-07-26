# Manul(Low profile GRIN layout keyboard based on Noraneko42GR)

## 概要

Manul（Noraneko42GR choc v2）は、[@darakuneko](https://github.com/darakuneko)さんの[Noranekoキーボード](https://github.com/darakuneko/Noraneko)の[Noraneko42gr v1.2](noraneko42gr/v1.2)を元にスイッチをChoc v2(Lofree Ghost switch)に変更したものです。

Manulは[Coffee License](LICENCE_JA.original)にしたがって作成しています。

このREADMEはNoraneko42GRとManul v1.0, 2.0で書きました。

## バージョン

### v1.0

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">Keyboard: Noraneko42GR / choc v2 mod<br>Switch: いろいろ / Lofree Ghost<br>Keycap: OSA Profile Black Transparent PC Keycap / Maya Imprint nSA<a href="https://twitter.com/hashtag/KEEB_PD?src=hash&amp;ref_src=twsrc%5Etfw">#KEEB_PD</a> <a href="https://twitter.com/hashtag/KEEB_PD_R200?src=hash&amp;ref_src=twsrc%5Etfw">#KEEB_PD_R200</a> <a href="https://t.co/kMvqZM04f1">pic.twitter.com/kMvqZM04f1</a></p>&mdash; fujihito (@fu2hito) <a href="https://twitter.com/fu2hito/status/1797206774899945583?ref_src=twsrc%5Etfw">June 2, 2024</a></blockquote> 

* PCB, Firmwareの動作確認済み
* PCBに設計ミスがあり、空中配線が必要
  * GP13(row0)が配線されていない
  * ソケットの干渉を避ける目的でパッドを削除する必要があり、キーマトリクスの変更とFirmwareの書き換えを含めた修正が必要
* Plateはネジ穴が不足、過度の切り抜きで剛性が不足

### v2.0

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">Keyboard: Manul(based on Noraneko42GR)<br>Switch: Haute42 Crystal<br>Keycap: Milky White Mist XSA Height<a href="https://twitter.com/hashtag/KEEB_PD?src=hash&amp;ref_src=twsrc%5Etfw">#KEEB_PD</a> <a href="https://twitter.com/hashtag/KEEB_PD_R207?src=hash&amp;ref_src=twsrc%5Etfw">#KEEB_PD_R207</a><br><br>基板、プレート修正して一応の完成です。名前は平べったい猫でマヌルに <a href="https://t.co/Jkr2DkHb3N">pic.twitter.com/Jkr2DkHb3N</a></p>&mdash; fujihito (@fu2hito) <a href="https://twitter.com/fu2hito/status/1814964786993754403?ref_src=twsrc%5Etfw">July 21, 2024</a></blockquote>

* PCBの設計変更
  * ピンアサインの変更を含めて、空中配線が不要になるように変更
  * キーマトリクスの変更
* Plateの設計変更
  * ネジ穴の追加
  * 切り抜きの変更

## Acknowledgement

Manulは直接的には以下の方々のおかげで作成されました。ありがとうございます。

### Noraneko42GR

Manulは[@darakuneko](https://github.com/darakuneko)さんの[Noraneko42gr v1.2](https://github.com/darakuneko/Noraneko/tree/main/noraneko42gr/v1.2)をベースに作成されました。

Noranekoキーボードシリーズは、[Coffee License](https://github.com/darakuneko/Noraneko/blob/main/LICENSE_JA)です。

KiCADファイルやFirmware、プレートファイルは、Noraneko42GRのものを使用しています。

### Choc v2スイッチのフットプリント

Choc v2スイッチのフットプリントは、[サリチル酸](https://github.com/Salicylic-acid3)さんの[KiCAD_FootPrint](https://github.com/Salicylic-acid3/KiCAD_FootPrint)を[フォークしたもの](https://github.com/fu2hito/KiCAD_FootPrint)を使用しました。1.5u等のフットプリントを追加しています。

KiCAD_FootPrintは、[MIT License](https://github.com/Salicylic-acid3/KiCAD_FootPrint/blob/master/Licence.txt)です。

その他[サリチル酸](https://x.com/Salicylic_acid3)さんにはdiscordや書籍などでお世話になっております。

### GPK FWBuilder

Firmwareのビルドは再び[@darakuneko](https://github.com/darakuneko)さんの[GPK FWBuilder](https://github.com/darakuneko/gpk_fwbuilder)を使用しています。
これなしでは私の自キ活は成り立ちません。

Intel Macだと10.1以降動かなくなっているので、Macの更新に迫られています。

### シリアルLEDについて

[monksoffunkJP](https://x.com/monksoffunkJP)さんの[記事](https://25keys.com/2022/05/28/rp2040_sk6812mini/)の下記引用部分を参考に配線しました。きれいに光っております。アドバイスなどあればIssueにてお願いします。

```
もうひとつ解決法があります。しかも面倒なパーツは一切要らない方法です。
それは、WS2812B V5とSK6812mini(-e)を併用するというものです。WS2812Bは3.3VのDINを受けてもDOUTは5Vレベルですので、先にWS2812Bをアンダーグロウとして使い、そのあとにSK6812mini-eをバックライトとして使えば仕様上は動作すると思います。あるいはWS2812Bをレベル変換のために1個だけ載せるという手もあるかもしれませんね。どちらも試したことはないので動かなかったらごめんなさい。
```

### スイッチ裏のRP2040 Zeroの配置について

スイッチのLEDまどを下向きにしたため、RP2040 Zeroのフットプリントはスイッチに干渉します。そのため、使用しないピンのパッドを削除しました。

この配線しないピンのパッドを削除するアイデアは、参考URLを失念しております。申し訳ございません。
たしかTwitterかdiscordで見たものだったかと思います。ありがとうございます。

## ライセンス

* MIT License
  * [LICENSE](./LICENSE)
