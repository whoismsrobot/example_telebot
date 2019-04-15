# Как сделать бота для телеграма. 
Каждый шаг этой инструкции соответствует одному из коммитов в данном репозитории.
1. Бот, работающий локально (первый коммит)
   1. Создадим пустого бота с помощью @BotFather - зададим ему имя и получим токен (ключ доступа)
   1. Установим питоновскую библиотеку `pytelegrambotapi`, с удобной обёрткой для телеграма. Это можно сделать, 
      например, с помощью пакетного менеджера `pip`. Все установленные библиотеки будем записывать в `requirements.txt`,
      чтобы потом они автоматически устанавливались на сервере. 
   1. Создадим файл `main.py` с примитивным ботом-повторюшкой. При запуске файла пароль от бота читается из переменных
      среды (чтобы не палить его в репозитории), создаются функции для ответа на сообщения, и бот запускается в режиме
      `polling` (когда ваша программа постоянно спрашивает Телеграм, нет ли обновлений)
   1. Чтобы протестировать его, надо вписать пароль в переменные среды (вбить в командной строке`set TOKEN=...` на винде 
      или `export TOKEN=...` на маке и линуксе), а дальше запустить в командной строке `python main.py` (предварительно
      перейдя в с помощью `cd` в папку с кодом) - и бот заработает!