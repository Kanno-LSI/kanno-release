# kanno-release
作成したソースコードの例です。研究に直接関わるものの掲載はしていません。

## 1. music_box_hardware

### 〇Description
マイクロプロセッサによるオルゴール用ファームウェアです。


大学の講義のTAとして学生向けに電子工作の例を紹介する目的で製作しました。


このオルゴールは2曲収録しており、スイッチやボリューム抵抗によって曲の種類、速度、音量を変えることができます。

#### Function
・PWM制御

周波数を制御し、音色を変更します。


・外部入力割り込み

使用しているマイクロプロセッサ(ATtiny84A)の入力仕様は、外部から信号を入力されると、進行中の動作を一度中断して関数を実行するようになっています。その特殊な特性に合わせて曲の種類変更に利用しています。


・AD変換、タイマ割り込み

AD変換を利用するとボリューム抵抗の回し具合に応じた数値を返すため、この機能を曲の速度変更に使用しています。また、タイマ割り込み内でAD変換を行うことで、リアルタイムで曲の速度を変更できます。


・ボリューム抵抗（ブレッドボード上）

圧電サウンダ（スピーカー）に加わる電圧を変化させ、音量を変更します。

### 〇Demo
準備中です。

### 〇Requirement
マイクロプロセッサ(ATtiny84A)のファームウェア作成・書き込み環境

電子回路設計

### 〇References
ATtiny84Aデータシート(参照：2023,05,21)

https://ww1.microchip.com/downloads/en/DeviceDoc/ATtiny24A-44A-84A-DataSheet-DS40002269A.pdf
