# mazda_skyactive_mx-5_can

Rev.1
SSD1309 128x64 1.56 Transparent OLED
[【RUN_img】](https://imgur.com/gallery/8cYCE9L)

準備する物
Things to prepare

スパークファン製品
sparkfun item

マイコンArduino
Red Board Turbo

canシールドとarduino端子
can-bus shield and arduino terminal

透過型OLEDディスプレイ
Transparent Graphical OLED Breakout (Qwiic)

Qwiicコネクタ
Connector(Qwiic)

汎用品
General-purpose products item

OBD2からDサブ9ピンにする故障診断器用ケーブル
OBD2-Dsub9pin cable

OBD2コネクタが出っ張らない為のOBD2延長ケーブル
OBD2 extension cable to prevent OBD2 connector 
from protruding

マイコンケースuno用
arduino uno case

スマホ車載ホルダー
Smartphone car holder

Mini-DINコネクタ 6ピン(PS/2コネクタ)
Mini-DIN connector 6-pin (PS/2 connector)

Mini-DINケーブル 6ピン(PS/2ケーブル オス-オス)
Mini-DIN cable 6-pin (PS/2 cable male-male)


ライブラリの準備
Library preparation

olikraus氏のU8g2_lib
olikraus's U8g2_lib

coryjfowler氏のMCP_CAN_lib
coryjfowler's MCP_CAN_lib

全ての利用ライブラリを検索し、Serial.print()をSerial【USB】.print()に変更
Search all used libraries and change Serial.print() to Serial[USB].print()

SPI通信で使う配線(MISO、MOSI、SCLK、SS、INT)にレベルシフタを設置
Install level shifters on the wiring used for SPI communication (MISO, MOSI, SCLK, SS, INT)

ハードウェアの修正
Hardware fix

OBD2コネクタのバッテリからのDC12VがRed board turboにかからないように、基盤間ピンを切る
Cut the pins between the boards so that DC12V from the battery of the OBD2 connector 
will not be applied to the Red board turbo

NDロードスターのOBD2コネクタ内15番端子とCAN-BUSシールドとを繋がないように、OBD2延長ケーブルからピンを切る
Cut the pin from the OBD2 extension cable so as not to connect the 15th terminal in the 
OBD2 connector of the ND Roadster and the CAN-BUS shield

Red board turboの充放電回路によるCAN-BUSシールド動作不良を無効にするため、DC5Vをカットし、端子にV-INを繋ぐ
To disable the CAN-BUS shield operation failure due to the charge/discharge circuit of the 
Red board turbo, cut DC5V and connect V-IN to the terminal

Rev.2
マイコン: Arduino MKR Zero I2S オーディオ/音楽 マイクロコントローラ
CANシールド: Arduino MKR CAN シールド
マイコンケース: Raspberry Pi 4Bケース RPI-4B-1F
表示部: SparkFun 128x64 透明グラフィカルOLEDブレイクアウト基板（Qwiic）
表示部土台: Emmabin スマホ車載ホルダー
OBD2ケーブル: uxcell ダイアグノスチック エクステンションコネクタケーブル OBD2 シリアル RS232 16ピン-9ピン 100cm
L型OBD2延長ケーブル: OBD2 延長ケーブル 60cm　フラットケーブル
I2C延長チップ: アナログデバイセズ製LTC4315IMS
I2C延長チップ基板: MSOP-12 TO DIP-16 SMT ADAPTER IPC0078

ハードウェアの修正Hardware fix
無し

CANデータの参考サイト
Reference site for CAN data

https://docs.google.com/spreadsheets/d/1uqwIMof9DdaEv0EkWHXe70XNGt0FGeDxpbMAgfKbbdk/edit#gid=0

https://github.com/majbthrd/MazdaCANbus
