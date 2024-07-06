# TG_Parser

Базовый парсер, который позволяет получить список пользователей, а также сообщения из открытых чатов Телеграм.
Реализован на основе библиотеки Telethon

## Установите зависимости:

```bash
pip install telethon
pip install tqdm
```

## Настройка

1. Зарегистрируйте приложение Telegram

[Зарегистрируйте приложение Telegram](https://my.telegram.org), чтобы получить `api_id`
и `api_hash`.

2. Настройте файл конфигурации `config.ini`

   В корневой директории проекта создайте файл `config.ini` и добавьте в него следующие строки, заменив YOUR_API_ID,
   YOUR_API_HASH и YOUR_USERNAME на соответствующие значения:
    ```ini
    [Telegram]
    api_id = YOUR_API_ID
    api_hash = YOUR_API_HASH
    username = YOUR_USERNAME
    ```

3. Добавьте ссылки на чаты для парсинга.

В файле `links.txt` добавьте ссылки на чаты для парсинга.

   ```txt
   https://t.me/example_chat
   https://t.me/another_chat
   ```

(ВАЖНО! Спарсить канал не получится т.к. вы не являетесь его администратором. Для парсинга чата или группы нужно быть на
них подписаным.)

4. Запуск парсера

Запустите `python Update.py` для запуска парсера.

* При первом запуске введите ваш номер телефона в международном формате без «+» и код подтверждения, который придет в Telegram.

Оригинальный гайд создания парсера можно найти
здесь: [Часть 1](https://vk.com/@pythonparser-parsing-telegram-chatov), [Часть 2](https://vk.com/@pythonparser-parsing-telegram-chatov2), [Часть 3](https://vk.com/@pythonparser-parsing-telegram-chatov-chast-3-soobscheniya)
