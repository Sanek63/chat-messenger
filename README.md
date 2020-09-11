# Приложение мини-чат на Python

В данном репозитории находятся материалы и примеры кода  по разработке на **Python**

## Структура репозитория
- **messenger.py** - исполняемый файл приложения. При инициализации объекта Messenger передается адрес хоста. По умолчанию http://127.0.0.1:5000 (локальный сервер)
- **server.py** - серверная часть приложения
    - **sender.py** - скрипт для отправки сообщения на сервер
    - **receiver.py** -  скрипт для получения сообщений из сервера
- **clientui.py** - интерфейс приложения, преобразованный в Python код
- **messenger.ui** - Интерфейс Qt. Открывать в Qt Designer
- **test.pu** - условная работа приложения, реализованная в консольном виде

## Установка

#### Для установки зависимостей проекта необходимо выполнить

```
pip install -r requirements.txt
```

#### Для просмотра списка установленных пакетов

```
pip list
```

## Запуск приложения на глобальном сервере

Для запуска приложения на глобальном сервере, в моем случае,
можно использовать утилиту [ngrok](https://ngrok.com). Утилита
более предназначена для тестирования приложений на глобальном сервере.

Для запуска глобального сервера в консоли пропишите
```
ngrok http 5000
```
Структура команды ngrok http 5000
- **ngrok** - утилита, которую необходимо запустить
- **http** - протокол, по которому будут проходить запросы
- **5000** - порт, на котором ваш **ЛОКАЛЬНЫЙ** сервер запущен

После запуска команды у вас появистя данное окно.
![2020-09-11_23-09](https://user-images.githubusercontent.com/46131081/92963675-e817fa00-f483-11ea-9698-a30a730fa542.png)

В поле **Forwarding** есть тот глобальный ip-шник, который необходимо будет
передать в файле messenger.py при инициализации объекта **Messenger**.
![2020-09-11_23-16](https://user-images.githubusercontent.com/46131081/92964276-e3077a80-f484-11ea-97a9-e6d704e5f9ec.png)

Запускаем проект и радуемся