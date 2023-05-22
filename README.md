# kanno-release
作成したソースコードの例です。研究に直接関わるものの掲載はしていません。

## 1. music_box_firmware

### Description
マイクロプロセッサによるオルゴール用ファームウェアです。


大学の講義のTAとして学生向けに電子工作の例を紹介する目的で製作しました。


このオルゴールは2曲収録しており、スイッチやボリューム抵抗によって曲の種類、速度、音量を変えることができます。


#### 〇　Function
・PWM制御

周波数を制御し、音色を変更します。


・外部入力割り込み

使用しているマイクロプロセッサ(ATtiny84A)の入力仕様は、外部から信号を入力されると、進行中の動作を一度中断して関数を実行するようになっています。その特殊な特性に合わせて曲の種類変更に利用しています。


・AD変換、タイマ割り込み

AD変換を利用するとボリューム抵抗の回し具合に応じた数値を返すため、この機能を曲の速度変更に使用しています。また、タイマ割り込み内でAD変換を行うことで、リアルタイムで曲の速度を変更できます。


・ボリューム抵抗（ブレッドボード上）

圧電サウンダ（スピーカー）に加わる電圧を変化させ、音量を変更します。


### Demo
準備中です。

音量調整
https://github.com/Kanno-LSI/kanno-release/assets/131650927/8eaa8c73-3d9e-4ef3-b4d6-91fff8f74cb6


速度調整
https://github.com/Kanno-LSI/kanno-release/assets/131650927/58037388-fdc6-450d-95a9-b53e3a0a6726


曲予約、変更
https://github.com/Kanno-LSI/kanno-release/assets/131650927/a263887f-693c-444d-96b4-806dcab2a359
https://github.com/Kanno-LSI/kanno-release/assets/131650927/40f91f39-8c6b-44e0-9feb-79c86b48d94d


収録曲(Happy Birthday以外)
https://github.com/Kanno-LSI/kanno-release/assets/131650927/0baf7a6d-76ae-4c9c-8d1d-dd3c03da5f61
https://github.com/Kanno-LSI/kanno-release/assets/131650927/e12033a2-61d4-4cd9-8f6e-64920026864c




### Requirement
マイクロプロセッサ(ATtiny84A)のファームウェア作成・書き込み環境

電子回路設計


### References
ATtiny84Aデータシート(参照：2023,05,21)

https://ww1.microchip.com/downloads/en/DeviceDoc/ATtiny24A-44A-84A-DataSheet-DS40002269A.pdf
