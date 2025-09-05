# Arduino Library for LiquidCrystal displays with I2C PCF8574 adapter SoftWire



A library for driving LiquidCrystal displays (LCD) by using SoftWire I2C and an PCF8574 I2C adapter.

You can specify which SoftWire interface the display should use:
```
LiquidCrystal_PCF8574 lcd (0x27);
SoftWire sw(PA12, PA11);

void setup() {
  ...
  lcd.begin(16, 2, &sw);
  ...
}
```

Or do not specify the SoftWire interface and use a predefined interface (SCL: PA11, SDA: PA12).

This library is intended for use with an STM32 MCU and a BaseShield that does not have hardware I2C connected to the display. (For whatever reason...)



Original Library: <https://github.com/mathertel/LiquidCrystal_PCF8574>