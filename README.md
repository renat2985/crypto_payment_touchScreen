[🇷🇺 Русская версия документации здесь](https://github.com/renat2985/crypto_payment_touchScreen/blob/main/README_RU.md)

# Payment for Your Services via Toncoin and Solana

A convenient and fast way to implement paid services using TonCoin and Solana cryptocurrencies. The process is simple: You open any crypto wallet, scan the QR code displayed on the device, transfer the specified amount, and once the payment is received (the wallet balance is checked every 5 seconds), the relay activates and turns on your device for the time you have set. This can be any device, from a kettle, coffee machine, or light bulb to turning on electricity in a room or any other place.

You can build the device yourself or ask us to do it for you. To order a ready-made device, contact us via [Telegram](https://t.me/ESPiotDevice), [Skype](https://skype:renat2985?chat), or [Discord](https://discord.com/invite/zaGaDuGe).

We have a similar project with a display, [check it out](https://github.com/renat2985/toncoin_payment), and also based on [Sonoff](https://github.com/renat2985/toncoin_payment_sonoff).

If you want to see a new cryptocurrency that you need here, feel free to contact us, and we'll add it. :)

[![IMAGE ALT TEXT HERE](https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/intro.jpg)](https://www.youtube.com/watch?v=OLOO8hDeg5w&list=PL6NJTNxbvy-LpsI6D_1RM6v5YWDvsm5j4)

### Main Features:

1. **Connecting the Device:**
   - When the device is turned on for the first time, or if it cannot find a router, it will create a hotspot named "Crypto payments."
     
     <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/WiFi.png" width="200px">
   - Connect to this hotspot (no password required) and open a browser, then enter http://192.168.4.1. After connecting to Wi-Fi, the Captive Portal will usually open automatically, redirecting you to the required page.
     
     <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/AP2.png" width="300px">
   - Click "Configure WiFi" to set it up.

2. **Device Configuration:**
   - **Router and Password:** Enter your Wi-Fi credentials.
   - **Device Name:** Enter a device name, for example, "Buy coffee."
   - **Your TonCoin Wallet:** Enter your wallet address to receive payments.
   - **Your Solana Wallet:** Enter your wallet address to receive payments.
   - **CoinMarketCap API:** Used to get the current exchange rate of Solana and TonCoin in fiat currency.
   - **NowNodesAPI API:** Used to get information about your wallet balance.

   You can use built-in APIs for testing; however, for long-term use, it is highly recommended to register on the respective websites ([coinmarketcap.com](https://coinmarketcap.com/api/) and [nownodes.io](https://nownodes.io/)) and obtain your own API keys. Free plans allow up to 10,000 requests per month, enough for 10 devices. However, with an increased number of devices, there may be delays in getting up-to-date information, which could disrupt the payment process.

   - **Currency:** Choose the currency in which you want to receive payments (EUR, USD, RUB, BYN, BGN, GBP, etc.). This is necessary for automatic conversion of the amount into Solana or TonCoin based on the current exchange rate, which is updated hourly via coinmarketcap.com.
   - **Service Currency Price:** Set the price in the selected currency that the client must pay.
   - **Payment Tolerance:** Enter the allowable price deviation here. Since the value of Ton fluctuates constantly, you need to specify a tolerance range (as a single number) that you are willing to accept for payment.
   - **Relay Work Time:** Specify how many seconds the relay should remain active. This can range from one second (for simulating a button press, for example) to several minutes or hours.

     <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/APFull2.png" width="300px">



### Instructions for DIY Assembly:

For DIY assembly, you will need [ESP32 C3 MINI 1.69inch LCD TouchScreen Display ST7789](https://spotpear.com/shop/ESP32-C3-Ornament-Trinket-LVGL-Astronaut-Clock-Watch-MINI-TV-1.69inch-Round-LCD-TouchScreen-ST7789-240x280-Case.html)


Additionally, you'll need:
- Arduino Relay 5v module
- Soldering iron
- Wires

  <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/gpio.png" height="200px">
  <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/photo.jpg" height="200px">


Good luck! If you have any questions, don’t hesitate to contact us.

# Web Installer (Recommended)
You need to connect the device via Type-C to your computer and open the following website in your browser:

## [https://renat2985.github.io/crypto_payment_touchScreen/](https://renat2985.github.io/crypto_payment_touchScreen/)


### For Professionals: Instructions for Flashing via Programmer
### Specification 
```
{ "path": "./build/esp32.esp32.esp32c3/crypto_payment_touchScreen.ino.bootloader.bin", "offset": 0 },
{ "path": "./build/esp32.esp32.esp32c3/crypto_payment_touchScreen.ino.partitions.bin", "offset": 32768 },
{ "path": "./build/esp32.esp32.esp32c3/boot_app0.bin", "offset": 57344 },
{ "path": "./build/esp32.esp32.esp32c3/crypto_payment_touchScreen.ino.bin", "offset": 65536 }
```



## :battery: Donation

If you like this project, you can buy me a cup of coffee :coffee:

<img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/donate.png" width="700px">

- PayPal [https://www.paypal.me/RKevrels](https://www.paypal.me/RKevrels/5)