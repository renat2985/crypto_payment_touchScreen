
# Оплата ваших услуг через Toncoin, Solana

 Удобный и быстрый способ внедрения платных услуг с использованием криптовалюты TonCoin и Solana. Процесс простой: Вы открываете любой крипто кошелек, сканируете QR-код который показывается на устройстве, переводите указанную сумму, и как только платеж будет получен (Баланс кошелька проверяется каждые 5 секунд), реле активируется и включит ваш прибор на заданное вами время. Это может быть любой прибор, от чайника, кофемашины и лампочки до включения электричества в помещение или любом другом месте.

Вы можете собрать устройство самостоятельно или попросить это сделать для вас. Для заказа готового устройства свяжитесь через [Telegram](https://t.me/ESPiotDevice), [Skype](https://skype:renat2985?chat), [Discord](https://discord.com/invite/zaGaDuGe).

У нас есть похожий проект с экраном, [посмотри](https://github.com/renat2985/solana_payment), и на базе [Sonoff](https://github.com/renat2985/toncoin_payment_sonoff).

Да и если вы хотите видеть здесь новую криптовалюту которая вам нужна, пишите, добавим. :)


![IMAGE ALT TEXT HERE](https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/intro.jpg)

### Основные функции:

1. **Подключение устройства:**
   - При первом включении, или если устройство не находит роутер, оно создаст точку доступа с именем "Crypto payments".
     
     <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/WiFi.png" width="200px">
   - Подключитесь к этой точке (пароль не требуется) и откройте браузер, где введите http://192.168.4.1. Обычно после подключения к Wi-Fi автоматически откроется Activ portal, который перенаправит вас на нужную страницу.
     
     <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/AP2.png" width="300px">
   - Нажмите "Configure WiFi" для настройки.

2. **Настройка устройства:**
   - **Роутер и пароль:** Введите данные для подключения к вашему Wi-Fi.
   - **Device Name:** Укажите имя устройства, например, "Buy coffee".
   - **Your TonСoin Wallet:** Введите адрес вашего кошелька для приема платежей.
   - **Your Solana Wallet:** Введите адрес вашего кошелька для приема платежей.
   - **CoinMarketCap API:** Используется для получения текущего курса Solana, TonCoin в фиатной валюте.
   - **NowNodesAPI API:** Служит для получения информации о балансе вашего кошелька.

   Для тестирования можно использовать встроенные API, однако для долгосрочного использования настоятельно рекомендуется зарегистрироваться на соответствующих сайтах ([coinmarketcap.com](https://coinmarketcap.com/api/) и [nownodes.io](https://nownodes.io/)) и получить собственные ключи API. Бесплатные тарифы позволяют выполнять до 10 000 запросов в месяц, чего достаточно для 10 устройств. Однако при увеличении количества устройств возможны перебои с получением актуальной информации, что может привести к сбоям в процессе оплаты.

   - **Сurrency:** Выберите валюту, в которой хотите получать оплату (EUR, USD, RUB, BYN, BGN, GBP и др.). Это необходимо для автоматической конвертации суммы в Solana, TonCoin на основе текущего курса, который обновляется каждый час через coinmarketcap.com.
   - **Service Currency Price:** Укажите цену в выбранной валюте, которую клиент должен оплатить.
   - **Payment Tolerance:** В этой ячейке указывается допустимая погрешность в цене. Поскольку стоимость Ton постоянно колеблется, здесь нужно указать диапазон отклонений (одной цифрой), который вы готовы принять при оплате.
   - **Relay Work Time:** Укажите, на сколько секунд должно включиться реле. Это может быть от одной секунды (например, для имитации нажатия кнопки) до нескольких минут или часов.

   <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/APFull2.png" width="300px">


### Инструкции для самостоятельной сборки:

Для самостоятельной сборки вам потребуется [ESP32 C3 MINI 1.69inch LCD TouchScreen Display ST7789](https://spotpear.com/shop/ESP32-C3-Ornament-Trinket-LVGL-Astronaut-Clock-Watch-MINI-TV-1.69inch-Round-LCD-TouchScreen-ST7789-240x280-Case.html)


Дополнительно вам понадобятся:
- Arduino Relay 5v module
- Паяльник
- Провода

  <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/gpio.png" width="500px">
  <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/photo.jpg" width="500px">


Удачи! Если у вас возникнут вопросы, не стесняйтесь обращаться к нам.

# Web installer (recommended)
Вам нужно подключить устройство через Type-C к копьютеру и открыть в браузере сайт:

## [https://renat2985.github.io/crypto_payment_touchScreen/](https://renat2985.github.io/crypto_payment_touchScreen/)


### Для совсем профи инструкция для прошивки через программатор
### Specification 
```
        { "path": "./build/esp32.esp32.esp32c3/crypto_payment_touchScreen.ino.bootloader.bin", "offset": 4096 },
        { "path": "./build/esp32.esp32.esp32c3/crypto_payment_touchScreen.ino.partitions.bin", "offset": 32768 },
        { "path": "./build/esp32.esp32.esp32c3/boot_app0.bin", "offset": 57344 },
        { "path": "./build/esp32.esp32.esp32c3/crypto_payment_touchScreen.ino.bin", "offset": 65536 }
```



## :battery: Donation

If you like this project, you can give me a cup of coffee :coffee:

<img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/donate.png" width="700px">

- PayPal [https://www.paypal.me/RKevrels](https://www.paypal.me/RKevrels/5)