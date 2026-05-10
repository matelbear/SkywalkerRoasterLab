1.加入 謝天 PWM 馬達改裝

2.此版本BLE可同時連線3部裝置.

Instructions for Adding Motor Speed PWM to Skywalker v1 ESP32 S3 Controller:
1. Regardless of whether the machine has been modified to add motor speed control, the ESP32 S3 controller will operate normally.
2. Original motors, worm motors, and brushless motors (Hall encoders) can all be speed controlled.
The ESP32 S3 uses pins 9, 10, and 11 for control.
Pin 9: PWM speed control
Pin 10: High (forward rotation)
Pin 11: Low (reverse rotation)

Original motors and worm motors can use D4284 and L298N.
D4184 Connection:
PWM -> Esp32 Pin 9
GND -> Esp32 GND
VIN+ -> Skywalker CN7 +
VIN- -> Skywalker CN7 -
OUT+ -> motor -
OUT- -> motor +
If the motor direction is incorrect, swap the motor's positive and negative wires at OUT.

L298N Connection:
ENA -> Esp32 Pin 9
IN1 -> Esp32 Pin 10
IN2 -> Esp32 Pin 11
+12V -> Skywalker CN7 +
GND -> Skywalker CN7 -
GND -> Esp32 GND
OUT1 -> motor -
OUT2 -> motor +
If the motor direction is incorrect, swap the positive and negative motor wires at OUT.

Brushless Motor (Hall Encoder) Wiring
Pin9: PWM Speed Control
Pin10: High Forward Rotation

Volunteer Efforts & Legal Disclaimer 
This codebase and firmware are volunteer efforts provided "AS IS", without warranty of any kind, express or implied. Please understand that you are using this software entirely at your own risk. 

The developer assumes no legal liability or responsibility for any direct, indirect, special, incidental, or consequential damages (including but not limited to hardware damage, property damage, data loss, or personal injury) resulting from the use, inability to use, or modification of this firmware. 

You are welcome to log issues against this codebase. The developer may review and address them as personal time permits, but there is absolutely no obligation to provide technical support, bug fixes, or updates. 


志願開發與免責聲明 
本專案的程式碼與韌體均為志願性質的開發成果，並按「現狀（AS IS）」提供，不附帶任何明示或暗示的擔保。請理解，您必須完全自行承擔使用此軟體的風險。 

對於因使用、無法使用或修改本韌體所導致的任何直接、間接、特殊、附帶或衍生性損害（包括但不限於硬體損壞、財產損失、資料遺失或人身傷害），開發者概不承擔任何法律責任。 

歡迎您在本專案中提交 Issue。開發者會在個人時間允許的情況下查看並處理，但不承擔任何提供技術支援、修復 Bug 或更新的義務。