# AE-NIIHAMA-ver2_asm_programs

秋月電子通商で販売されている新居浜高専PICマイコン学習キットVer.2(AE-NIIHAMA-ver2)(販売コード 106971)をアセンブリ言語で動かしてみました。

PIC16F886にPickitなどで書き込みます。

作りかけの機能がある中途半端なプログラムです。1500行くらいあります。

Custom linker options
<pre>
  -presetVec=0h
</pre>


## 操作と機能

起動後しばらくするとSEL0が表示されます。

SW1とSW2でSEL(機能選択)できます。SEL0-SELFまであります。

SW3でSEL0に戻ります。

SW4は決定ボタンです。

### SEL0 
<pre>
時計機能です。
SW4を押しながら設定します。
SW3と同時押しで、hourをインクリメント
SW2と同時押しで、minuteをインクリメント
SW1と同時押しで、12h,24h,30hモードの切り替えができます。
D13,D16のLEDで午前午後を表現してます。
</pre>

### SEL1
<pre>
16進数でカウントする変わったカウンタ
SW1でインクリメント
SW2でデクリメント
SW3でリセット
SW4で一定時間たったらインクリメント/STOP  
</pre>

### SEL2
以降、未実装
### SEL3
### SEL4
### SEL5
### SEL6
### SELD
VR1をADCした値をD4-D11のLEDに表示します。
### SELE
### SELF
テスト用。現在、シリアル通信の機能が実装されています。外部回路（AE-FT234Xと抵抗器）が必要です。未完成。


















