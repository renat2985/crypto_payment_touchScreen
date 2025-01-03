
# Оплата ваших услуг через Solana, Cosmos, Algorand, Toncoin

 Удобный и быстрый способ внедрения платных услуг с использованием криптовалюты Solana, Cosmos, Algorand, Toncoin. Процесс простой: Вы открываете любой крипто кошелек, сканируете QR-код который показывается на устройстве, переводите указанную сумму, и как только платеж будет получен (Баланс кошелька проверяется каждые 5 секунд), реле активируется и включит ваш прибор на заданное вами время. Это может быть любой прибор, от чайника, кофемашины и лампочки до включения электричества в помещение или любом другом месте.

Вы можете собрать устройство самостоятельно или попросить это сделать для вас. Для заказа готового устройства свяжитесь через [Telegram](https://t.me/ESPiotDevice), [Skype](https://skype:renat2985?chat), [Discord](https://discord.com/invite/zaGaDuGe).

У нас есть похожий проект с экраном, [посмотри](https://github.com/renat2985/toncoin_payment), и на базе Sonoff:

- [Sonoff for Toncoin (toncenter.com)](https://github.com/renat2985/toncoin_payment_sonoff)

- [Sonoff for Toncoin, Solana, Cosmos, Algorand (tatum.io)](https://github.com/renat2985/crypto_payment_sonoff)


Да и если вы хотите видеть здесь новую криптовалюту которая вам нужна, пишите, добавим. :)

[![IMAGE ALT TEXT HERE](https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/intro.jpg)](https://www.youtube.com/watch?v=OLOO8hDeg5w&list=PL6NJTNxbvy-LpsI6D_1RM6v5YWDvsm5j4)

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
   - **Your Cosmos Wallet:** Введите адрес вашего кошелька для приема платежей.
   - **Your Algorand Wallet:** Введите адрес вашего кошелька для приема платежей.
   - **CoinMarketCap API:** Используется для получения текущего курса Solana, Cosmos, Algorand, Toncoin в фиатной валюте.
   - **Tatum API:** Служит для получения информации о балансе вашего кошелька.

      _Для тестирования можно использовать встроенные API, однако для долгосрочного использования настоятельно рекомендуется зарегистрироваться на соответствующих сайтах ([coinmarketcap.com](https://coinmarketcap.com/api/) и [tatum.io](https://tatum.io/)) и получить собственные ключи API. Бесплатные тарифы позволяют выполнять до 10 000 запросов в месяц, чего достаточно для 10 устройств. Однако при увеличении количества устройств возможны перебои с получением актуальной информации, что может привести к сбоям в процессе оплаты._

   - **Сurrency:** Выберите валюту, в которой хотите получать оплату (EUR, USD, RUB, BYN, BGN, GBP и др.). Это необходимо для автоматической конвертации суммы в Solana, Cosmos, Algorand, Toncoin на основе текущего курса, который обновляется каждый час через coinmarketcap.com.
   - **Service Currency Price:** Укажите цену в выбранной валюте, которую клиент должен оплатить.
   - **Payment Tolerance:** В этой ячейке указывается допустимая погрешность в цене. Поскольку стоимость Ton постоянно колеблется, здесь нужно указать диапазон отклонений (одной цифрой), который вы готовы принять при оплате.
   - **Relay Work Time:** Укажите, на сколько секунд должно включиться реле. Это может быть от одной секунды (например, для имитации нажатия кнопки) до нескольких минут или часов.

      <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/APFull2.png" width="300px">

3. **Сброс настроек:**

      Чтобы сбросить устройство до заводских настроек, выполните следующие шаги:
      1.	Нажмите правую кнопку, расположенную на задней стороне корпуса. Устройство начнет перезагружаться. Или вместо этого можно отключить и снова подключить питание к устройству.
      2.	Когда устройство включится и вы увидите отображение версии прошивки и короткий звуковой сигнал, немедленно зажмите левую кнопку.
      3.	После этого вы услышите продолжительный низкий сигнал, а на экране появится сообщение о стирании данных.

      Теперь настройки устройства будут сброшены. И снова появится WiFi "Crypto payment".

### Инструкции для самостоятельной сборки:

Для самостоятельной сборки вам потребуется [ESP32 C3 MINI 1.69inch LCD TouchScreen Display ST7789](https://spotpear.com/shop/ESP32-C3-Ornament-Trinket-LVGL-Astronaut-Clock-Watch-MINI-TV-1.69inch-Round-LCD-TouchScreen-ST7789-240x280-Case.html)


Дополнительно вам понадобятся (AliExpress):

[USB Type A Connector Male](https://www.aliexpress.com/item/32924785370.html)

[5V Relay Module for Arduino Relay](https://www.aliexpress.com/item/1005006149703205.html)


### Схема подключения

  <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/connect.png" height="200px"> <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/gpio.png" height="200px"> <img src="https://github.com/renat2985/crypto_payment_touchScreen/blob/main/doc/photo.jpg" height="200px">


Удачи! Если у вас возникнут вопросы, не стесняйтесь обращаться к нам.

# Web installer (recommended)
Вам нужно подключить устройство через Type-C к копьютеру и открыть в браузере сайт:

## [https://renat2985.github.io/crypto_payment_touchScreen/](https://renat2985.github.io/crypto_payment_touchScreen/)


### Для совсем профи инструкция для прошивки через программатор
### Specification 
```
{ "path": "./build/esp32.esp32.esp32c3/crypto_payment_touchScreen.ino.bootloader.bin", "offset": 0 },
{ "path": "./build/esp32.esp32.esp32c3/crypto_payment_touchScreen.ino.partitions.bin", "offset": 32768 },
{ "path": "./build/esp32.esp32.esp32c3/boot_app0.bin", "offset": 57344 },
{ "path": "./build/esp32.esp32.esp32c3/crypto_payment_touchScreen.ino.bin", "offset": 65536 }
```



## :battery: Donation

If you like this project, you can give me a cup of coffee :coffee:

<img src="https://github.com/renat2985/renat2985/raw/main/donate/donate.png" width="100%">

- PayPal [https://www.paypal.me/RKevrels](https://www.paypal.me/RKevrels/5)