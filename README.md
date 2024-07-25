# Manul(Low profile GRIN layout keyboard based on Noraneko42GR)

## 概要

Manul（Noraneko42GR choc v2）は、[@darakuneko](https://github.com/darakuneko)さんの[Noranekoキーボード](https://github.com/darakuneko/Noraneko)の[Noraneko42gr v1.2](noraneko42gr/v1.2)を元にスイッチをChoc v2(Lofree Ghost switch)に変更したものです。

Manulは[Coffee License](LICENCE_JA.original)にしたがって作成しています。

このREADMEはNoraneko42GRとManulで書きました。

## バージョン

### v1.0

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">Keyboard: Noraneko42GR / choc v2 mod<br>Switch: いろいろ / Lofree Ghost<br>Keycap: OSA Profile Black Transparent PC Keycap / Maya Imprint nSA<a href="https://twitter.com/hashtag/KEEB_PD?src=hash&amp;ref_src=twsrc%5Etfw">#KEEB_PD</a> <a href="https://twitter.com/hashtag/KEEB_PD_R200?src=hash&amp;ref_src=twsrc%5Etfw">#KEEB_PD_R200</a> <a href="https://t.co/kMvqZM04f1">pic.twitter.com/kMvqZM04f1</a></p>&mdash; fujihito (@fu2hito) <a href="https://twitter.com/fu2hito/status/1797206774899945583?ref_src=twsrc%5Etfw">June 2, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

* PCB, Firmwareの動作確認済み
* PCBに設計ミスがあり、空中配線が必要
  * GP13(row0)が配線されていない
  * ソケットの干渉を避ける目的でパッドを削除する必要があり、キーマトリクスの変更とFirmwareの書き換えを含めた修正が必要
* Plateはネジ穴が不足、過度の切り抜きで剛性が不足

### v2.0

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">Keyboard: Manul(based on Noraneko42GR)<br>Switch: Haute42 Crystal<br>Keycap: Milky White Mist XSA Height<a href="https://twitter.com/hashtag/KEEB_PD?src=hash&amp;ref_src=twsrc%5Etfw">#KEEB_PD</a> <a href="https://twitter.com/hashtag/KEEB_PD_R207?src=hash&amp;ref_src=twsrc%5Etfw">#KEEB_PD_R207</a><br><br>基板、プレート修正して一応の完成です。名前は平べったい猫でマヌルに <a href="https://t.co/Jkr2DkHb3N">pic.twitter.com/Jkr2DkHb3N</a></p>&mdash; fujihito (@fu2hito) <a href="https://twitter.com/fu2hito/status/1814964786993754403?ref_src=twsrc%5Etfw">July 21, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

* PCBの設計変更
  * ピンアサインの変更を含めて、空中配線が不要になるように変更
  * キーマトリクスの変更
* Plateの設計変更
  * ネジ穴の追加
  * 切り抜きの変更

## ライセンス

* MIT License
  * [LICENSE](./LICENSE)
