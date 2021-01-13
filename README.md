# mazda_skyactive_mx-5_can

SSD1309 128x64 1.56inch Transparent OLEDを使用したメーターです
[【RUN_img】](https://imgur.com/gallery/8cYCE9L)

Rev.1
準備する物
スパークファンRed Board Turbo
canシールドとarduino端子
透過型OLEDディスプレイ
Qwiicコネクタ
OBD2からDサブ9ピンにする故障診断器用ケーブル
OBD2コネクタが出っ張らない為のOBD2延長ケーブル
マイコンケースuno用
スマホ車載ホルダー
Mini-DINコネクタ 6ピン(PS/2コネクタ)
Mini-DINケーブル 6ピン(PS/2ケーブル オス-オス)

ライブラリの準備
olikraus氏のU8g2_libと、coryjfowler氏のMCP_CAN_libをダウンロード
全ての利用ライブラリを検索し、Serial.print()をSerial【USB】.print()に変更

ハードウェアの修正
OBD2コネクタのバッテリからのDC12VがRed board turboにかからないように、基盤間ピンを切る
NDロードスターのOBD2コネクタ内15番端子とCAN-BUSシールドとを繋がないように、OBD2延長ケーブルからピンを切る
Red board turboの充放電回路によるCAN-BUSシールド動作不良を無効にするため、DC5Vをカットし、端子にV-INを繋ぐ
SPI通信で使う配線(MISO、MOSI、SCLK、SS、INT)にレベルシフタを設置

Rev.2
準備する物
マイコン: Arduino MKR Zero I2S オーディオ/音楽 マイクロコントローラ
CANシールド: Arduino MKR CAN シールド
マイコンケース: Raspberry Pi 4Bケース RPI-4B-1F
表示部: SparkFun 128x64 透明グラフィカルOLEDブレイクアウト基板（Qwiic）
表示部土台: Emmabin スマホ車載ホルダー
OBD2ケーブル: uxcell ダイアグノスチック エクステンションコネクタケーブル OBD2 シリアル RS232 16ピン-9ピン 100cm
L型OBD2延長ケーブル: OBD2 延長ケーブル 60cm　フラットケーブル
I2C延長チップ: アナログデバイセズ製LTC4315IMS
I2C延長チップ基板: MSOP-12 TO DIP-16 SMT ADAPTER IPC0078

ライブラリの準備
Rev.1と同じ

ハードウェアの修正
無し

CANデータの参考サイト
Reference site for CAN data

https://docs.google.com/spreadsheets/d/1uqwIMof9DdaEv0EkWHXe70XNGt0FGeDxpbMAgfKbbdk/edit#gid=0

https://github.com/majbthrd/MazdaCANbus
