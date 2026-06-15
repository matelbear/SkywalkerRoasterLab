MAX6675_SO  = 4;
MAX6675_CS  = 5;
MAX6675_SCK = 6;

VCC -> 3.3V
GND -> GND

1.上電初始化 (Power On)： 黃燈恆亮 1秒 (表示系統啟動)。
2.未連接/廣播中 (Advertising)： 紅色呼吸燈 (尋找橋接器中)。
3.已連接 (Connected)： 藍色呼吸燈 (已連上橋接器，待機)。
4.傳送數據 (Sending)： 白光短閃 (每 500ms 讀取並發送溫度時閃一下，確認感測器運作中)。

_______________________________________________________________________________________

MAX6675_SO  = 4;
MAX6675_CS  = 5;
MAX6675_SCK = 6;

VCC -> 3.3V
GND -> GND

1. Power On: Yellow light stays on for 1 second (indicating system startup).

2. Not Connected/Advertising: Red breathing light (searching for bridge).

3. Connected: Blue breathing light (bridge connected, standby).

4. Sending Data: Short white flash (flashes once every 500ms when reading and sending temperature, confirming sensor operation).
