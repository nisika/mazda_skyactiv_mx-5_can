# mazda_skyactive_mx-5_can

SSD1309 128x64 1.56 Transparent OLED
[RUN_img](https://imgur.com/gallery/8cYCE9L)

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

uno互換にするため、D11 D12 D13をSPI通信で使うように、variant.hの以下の部分を修正
Modified the following parts of variant.h to use D11 D12 D13 for SPI communication to 
be compatible with uno.

/* SPI Interfaces */
#define SPI_INTERFACES_COUNT 1

#define PIN_SPI_MISO         【(34u)】
#define PIN_SPI_MOSI         【(35u)】
#define PIN_SPI_SCK          【(37u)】
#define PERIPH_SPI           【sercom1】
#define PAD_SPI_TX           【SPI_PAD_0_SCK_1】
#define PAD_SPI_RX           【SERCOM_RX_PAD_3】
Mini-DIN cable 6-pin (PS/2 cable male-male)

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

CANデータの参考サイト
Reference site for CAN data

https://docs.google.com/spreadsheets/d/1uqwIMof9DdaEv0EkWHXe70XNGt0FGeDxpbMAgfKbbdk/edit#gid=0

https://github.com/majbthrd/MazdaCANbus
