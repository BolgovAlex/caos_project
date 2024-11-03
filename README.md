# Терминальный мессенджер
Участники - Болгов Александр, Зодоров Адам, Багдасарян Эдуард
## Задача 

Создание простого мессенджера, работающего в терминале, который позволяет пользователям обмениваться текстовыми сообщениями в режиме реального времени. Проект поможет понять основы сетевого программирования, взаимодействие через протокол TCP/IP и обработку клиентских соединений.

## Принцип работы

Мессенджер будет состоять из двух основных компонентов: сервера и клиента. Сервер будет принимать соединения от клиентов и пересылать сообщения между ними. Клиенты смогут отправлять и получать сообщения через терминал.

### Архитектура

1. **Сервер**:
    - Создает сокет и слушает входящие соединения.
    - Обрабатывает каждое соединение. 
    - Пересылает сообщения от одного клиента к другим.
    - Логирование сообщений — возможность сохранять историю сообщений.


2. **Клиент**:
    - Подключается к серверу.
    - Отправляет текстовые сообщения.
    - Получает и отображает сообщения от других клиентов.

## Требуемый функционал

- Сервер:
    - Поддержка нескольких клиентов одновременно.
    - Пересылка сообщений между клиентами.
    - Отображение информации о подключенных клиентах.

- Клиент:
    - Ввод сообщения с клавиатуры. Отправка через терминал
    - Отображение полученных сообщений в терминале.
    - Возможность выхода из чата.

## Требуемый функционал

### Сервер

1. **Создание и настройка сокета**:
    - Инициализация сокета для приема входящих соединений.
    - Настройка параметров (например, адреса и порта) для прослушивания.

2. **Обработка подключений**:
    - Поддержка одновременных соединений: сервер должен уметь принимать несколько клиентов и обрабатывать их параллельно.

3. **Пересылка сообщений**:
    - Получение сообщений от одного клиента и их пересылка всем остальным подключенным клиентам.
    - Форматирование сообщений для отображения информации о том, кто отправил сообщение (например, "User1: Привет!").

4. **Информация о подключенных клиентах**:
    - Поддержка списка активных клиентов, отображение их имен или идентификаторов.
    - Возможность отправки системных сообщений (например, о том, что клиент подключился или отключился).

5. **Обработка ошибок**:
    - Логирование ошибок и управление исключениями (например, что делать, если клиент отключается).
    - Ведение журнала активности (например, запись входящих и исходящих сообщений).
### Клиент

1. **Подключение к серверу**:
    - Ввод адреса и порта сервера для подключения.
    - Отображение сообщений об успешном или неудачном подключении.

2. **Интерфейс для ввода сообщений**:
    - Поддержка ввода текстовых сообщений с клавиатуры.
    - Возможность отправки сообщения по нажатию клавиши (например, Enter).

3. **Отображение полученных сообщений**:
    - Вывод сообщений от других клиентов в терминале в реальном времени.

4. **Выход из чата**:
    - Команда для выхода из мессенджера (например, `exit` или `quit`).
    - Обработка отключения от сервера и уведомление других клиентов о выходе.

5. **Обработка ошибок**:
    - Сообщения об ошибках, таких как потеря соединения или ошибка отправки.
    - Предоставление пользователю информации о текущем состоянии соединения (например, подключен или отключен).

## На подумать

- Какие дополнительные функции можно добавить в мессенджер? Например, поддержку групповых чатов или отправку файлов.

Язык программирования C++

Участник 1: разработка сервера, обработка подключений и сообщений.
Участник 2: разработка клиентской части и логики взаимодействия с сервером.
Участник 3: тестирование, проверка безопасности, отладка многопользовательских сессий.


